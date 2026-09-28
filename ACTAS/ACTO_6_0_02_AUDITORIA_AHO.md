════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON AHO 2007
DOCUMENTO: ACTAS/ACTO_6_0_02_AUDITORIA_AHO.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Alfred V. Aho · Monica S. Lam · Ravi Sethi · Jeffrey D. Ullman
Obra: Compilers: Principles, Techniques, and Tools
Raw: ~/.aho_compilers_raw.txt · 55.830 líneas · 2.156.010 bytes
Naturaleza: canon de lenguajes formales, análisis léxico/sintáctico/AST

Loci invocados:
  L108-109   · capítulo 3 · lexical analysis
  L117-120   · capítulos 4-5 · parsing · syntax-directed
  L1055-1056 · intérprete · ejecución directa
  L1150-1156 · análisis/síntesis · front-end / back-end
  L1199-1222 · lexemas y tokens
  L1314-1319 · sintaxis y árbol de sintaxis
  L1336      · gramáticas libres de contexto
  L1344-1348 · análisis semántico · type checking
  L2836-2838 · abstract syntax trees
  L3037-3048 · parse tree
  L3435      · syntax-directed definitions
  L3693      · syntax-directed translation scheme

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Análisis léxico
  El lexer lee caracteres, agrupa en lexemas, produce tokens
  ⟨token-name, attribute-value⟩ — L1199-1207.

C2 · Análisis sintáctico
  El parser usa gramáticas libres de contexto para imponer
  estructura gramatical — L1314, L1336.

C3 · Árbol de sintaxis abstracta (AST)
  Representación jerárquica del programa fuente. El parser
  produce un AST que el análisis semántico y la generación
  de código consumen — L1317-1319, L2836-2838.

C4 · Traducción dirigida por sintaxis
  Asocia fragmentos de programa a producciones gramaticales
  — L3435, L3693.

C5 · Compilador vs intérprete
  Compilador traduce a target program. Intérprete ejecuta
  directamente. Front-end / back-end separados por
  representación intermedia — L1055-1056, L1150-1156.

C6 · Análisis semántico
  Usa el AST + symbol table. Type checking verifica
  compatibilidad de operandos — L1344-1348.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · ANÁLISIS LÉXICO

  C1-E1 · grammar.lark define terminales NAME, NUMBER, STRING, BOOLEAN
    Resultado: resiste
    Cita: L1205-1207 "groups the characters into meaningful sequences
          called lexemes... produces as output a token"
    Ubicación: scfv_dsr/dsl/grammar.lark · líneas 54-59

  C1-E2 · Lark produce tokens con nombre y valor
    Resultado: resiste
    Cita: L1206-1207 "token of the form ⟨token-name, attribute-value⟩"
    Ubicación: scfv_dsr/dsl/parser.py

  C1-E3 · Los tokens se pierden al convertirse a string plano
    Resultado: falla
    Cita: L1207-1208 "that it passes on to the subsequent phase"
    Ubicación: scfv_dsr/dsl/parser.py · _expr_to_str

C2 · ANÁLISIS SINTÁCTICO

  C2-E1 · lark.Lark(grammar, parser="lalr") · parser LALR correcto
    Resultado: resiste
    Cita: L117 "Chapter 4 covers the major parsing methods"
    Ubicación: scfv_dsr/dsl/parser.py · línea 14

  C2-E2 · Gramática CFG completa con precedencia y alternancia
    Resultado: resiste
    Cita: L1336 "we shall use context-free grammars"
    Ubicación: scfv_dsr/dsl/grammar.lark · líneas 20-50

  C2-E3 · El AST se aplana a texto en _extract_condition y _extract_actions
    Resultado: falla
    Cita: L1314 "The parser uses the... structure"
    Ubicación: scfv_dsr/dsl/parser.py · _extract_condition

C3 · ÁRBOL DE SINTAXIS ABSTRACTA (AST)

  C3-E1 · Lark produce lark.Tree (AST nominal interno)
    Resultado: resiste
    Cita: L1317-1319 "A typical representation is a syntax tree"
    Ubicación: interno de lark

  C3-E2 · _expr_to_str destruye el AST transformándolo a string
    Resultado: falla crítica
    Cita: L2836-2838 "abstract syntax trees... represents the
          hierarchical syntactic structure of the source program"
    Ubicación: scfv_dsr/dsl/parser.py · _expr_to_str

  C3-E3 · evaluador.parsear_accion re-construye con regex
    Resultado: falla crítica
    Cita: L2838 "the parser produces a syntax tree, that"
    Ubicación: scfv_dsr/evaluador.py · parsear_accion

C4 · TRADUCCIÓN DIRIGIDA POR SINTAXIS

  C4-E1 · El E3 no usa traducción dirigida por sintaxis
    Resultado: no aplica
    Cita: L3435 "attaching program fragments to productions"
    Ubicación: global

  C4-E2 · El pipeline fragmenta: parser → string → regex → dict
    Resultado: parcial
    Cita: L3693 "order of evaluation of the semantic rules is
          explicitly specified"
    Ubicación: scfv_dsr/dsl/parser.py + evaluador.py

C5 · COMPILADOR VS INTÉRPRETE

  C5-E1 · E3 es intérprete (ejecuta en runtime)
    Resultado: resiste como intérprete
    Cita: L1055-1056 "an interpreter appears to directly execute"
    Ubicación: scfv_dsr/cli.py + integrador.py

  C5-E2 · No hay separación front-end / back-end clara
    Resultado: parcial
    Cita: L1150-1156 "analysis part is often called the front end...
          the synthesis part is the back end"
    Ubicación: parser.py vs evaluador.py · frontera difusa

C6 · ANÁLISIS SEMÁNTICO

  C6-E1 · Validación semántica en Motor (XNOR, I1-I6)
    Resultado: resiste
    Cita: L1344-1346 "The semantic analyzer uses the syntax tree"
    Ubicación: scfv_dsr/contable/motor.py

  C6-E2 · No hay symbol table explícita
    Resultado: parcial
    Cita: L1153 "stores it in a data structure called a symbol table"
    Ubicación: kernel/*.json cumple rol informal

  C6-E3 · Type checking delegado a Python runtime
    Resultado: no aplica
    Cita: L1348 "An important part of semantic analysis is
          type checking"
    Ubicación: global

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Léxico                   2        0       1       0
  C2 · Sintáctico               2        0       1       0
  C3 · AST                      1        0       2       0
  C4 · Traducción dirigida      0        1       0       1
  C5 · Compilador/intérprete    1        1       0       0
  C6 · Semántico                1        1       0       1
  ──────────────────────────────────────────────────────────────
  Total                         7        3       4       2

  Emergencias registradas: 16

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  El E3 usa LALR y gramática libre de contexto correctamente.
  La elección de Lark como herramienta de parsing es técnicamente
  sólida. La gramática cubre precedencia, alternancia y tipos de
  token. Coherente con la Fase 1-2 del compilador descrita por Aho.

D · Divergencia
  Aho exige que el AST preserve la estructura jerárquica para el
  análisis semántico. El E3 lo produce con Lark pero lo destruye
  inmediatamente convirtiéndolo a string. El evaluador re-construye
  estructura con regex. Es la antítesis del principio de Aho.

E · Emergencia
  El parser y el evaluador no comparten representación intermedia.
  Aho llama a esto "front end" y "back end" — deberían compartir el
  AST. El E3 los separa con un cuello de botella de texto.
  La deuda heredada H175 queda confirmada y amplificada desde un
  segundo canon independiente.

E · Enriquecimiento
  Aho da terminología técnica precisa a la deuda: no es "el parser
  devuelve strings" — es que no hay intermediate representation
  compartida entre front-end y back-end. Convierte la observación
  en una deuda arquitectónica nombrable con literatura.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Aho 2007 (Compilers) × SCFV_DSR E3.
No emite veredicto global de aptitud del artefacto.
No anticipa el diagnóstico L4/L5.
El diagnóstico es competencia exclusiva de ACTO 6.0.CONV.

────────────────────────────────────────────────────────────────────────

§8 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: DEDN · C.P.C. Nº 183594
  Fecha: 2026-09-26

IA-1 · Constructor · constancia de interpretación arquitectónica
  Firma: IA-1 · Constructor
  Constancia: acta 6.0.02 redactada conforme al protocolo 6.0 §5,
  con emergencias ancladas a loci del raw y a ubicaciones del E3.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

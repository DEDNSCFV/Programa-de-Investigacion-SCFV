════════════════════════════════════════════════════════════════════════
ACTA DE MATERIALIZACIÓN DEL MÓDULO DE GRAMÁTICA EXTENDIDA Y PARSER ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 14
Documento: GIRO_04/14_materializacion_dsl_adl.md
Versión: C
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN BLOQUEANTES.

Correcciones aplicadas sobre Versión B:
  O-378: §8.3 reformulado — igualdad por == sin exigir orden de claves.
  O-379: §11.16 fusionado en la lista numerada como punto 16.
  O-380: §7.4 precisa heredar SyntaxError con el mismo patrón de S0.

Estatuto: ejecuta D-12.2 y D-13.1. No modifica S0.
No escribe .scfv extendidos (eso es Acto 15). No cierra Giro 04.

Hash previo al registro: cb63154a5c34626524ffe6d810861c410182fdd3d327bb049d1ae626a6e88269
Hash final registrado:   8309e2fc0b31716579653f7d2cab2c9d49ad2a05f9e1bcf6a946b60839619869
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

Materializar el módulo ~/SCFV_DSR/dsl/ conforme al Acto 13, en dos fases
ADR-003: Fase A (README) y Fase B (código + pruebas).

Cierra D-12.2 y D-13.1, sujeto a verificación efectiva.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES Y BASELINES
────────────────────────────────────────────────────────────────────────

- Acto 12 — declarado: 3e284483460a9d0cfd5506984e12b7027ce9f822417e0ec67d74cfae4018e49c
            en disco:  7182cb2892ce34cf54494494fc92fa00bff5910b22a34b84e44d6c775e86a844
- Acto 13 — declarado: 3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee
            en disco:  e140099c9ea6d63661dd4a15f4d75374cc8a6b1c0a7bbd14536ab8d7cc853be0
- grammar.lark S0: 3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850
- parser.py S0:    eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

Baselines .scfv históricos:
  ventas     ba647a58f9e210bed46109bf52c2247d971ae5c7e91e8a663c8a826c08cde16f
  compras    9e834aa220d94945c617ec3f2e9be7999dcbfcb57d121c6ec161d2cc55cdd339
  inventario 016fb0d2123efbfcbd0e3185b4544200e437b837c21fd84d9749542f15b1d058
  fiscal     f7e37f713f178dba9b7d03623dfbb3211e3e011ad929986205972d4cfdad8d1a


────────────────────────────────────────────────────────────────────────
§3. ESTATUTO Y SECUENCIA INTERNA — ADR-003
────────────────────────────────────────────────────────────────────────

§3.1 Fase A: README.md del módulo (artefacto especificativo aprobable).
§3.2 Fase B: grammar.lark + parser.py + __init__.py + tests/, tras aprobación
     del README.
§3.3 Falsación IA-2 puede ocurrir en dos tiempos: sobre el README y sobre
     el código.


────────────────────────────────────────────────────────────────────────
§4. ESTRUCTURA FÍSICA DEL MÓDULO
────────────────────────────────────────────────────────────────────────

~/SCFV_DSR/dsl/
├── README.md
├── grammar.lark
├── parser.py
├── __init__.py        (archivo vacío, coherente con S0)
└── tests/
    ├── test_grammar_lalr.py
    ├── test_compatibilidad_s0.py
    ├── test_contract_def.py
    ├── test_invariant_def.py
    └── test_asiento_declarado_def.py

Divergencia deliberada respecto de S0: S0 no tiene tests/ dentro de dsl/;
los coloca en ~/scfv_v6/TESTS/. El Acto 14 adopta ~/SCFV_DSR/dsl/tests/
por el principio de módulo autocontenido.


────────────────────────────────────────────────────────────────────────
§5. README DEL MÓDULO — FASE A
────────────────────────────────────────────────────────────────────────

Declarará, como mínimo: propósito; autoridad y límites (parser no decide,
no contabiliza, no modifica); entradas y salidas (Dict[str, Any] con las
cinco claves históricas más contratos, invariantes, asientos_declarados);
invariantes del módulo; dependencias permitidas y prohibidas; pruebas
requeridas; bloques PRE/POST/INVARIANTE por producción.


────────────────────────────────────────────────────────────────────────
§6. GRAMMAR.LARK EXTENDIDO — FASE B
────────────────────────────────────────────────────────────────────────

Copia local de S0 más extensión aditiva. Una producción por línea (Acto
13 §11.4). Sin %import. No modifica S0 salvo start.


────────────────────────────────────────────────────────────────────────
§7. PARSER.PY EXTENDIDO — FASE B
────────────────────────────────────────────────────────────────────────

Copia local del parser S0 con extensión en _transform_tree para
contract_def, invariant_def, asiento_declarado_def. Conserva las cinco
claves históricas y añade contratos, invariantes, asientos_declarados.

§7.4 Errores: hereda el patrón de S0 —SyntaxError con mensaje
"Error de sintaxis en {filepath}: {e}" y "Error de sintaxis: {e}"—.
No silencia, no convierte entrada inválida en salida aparentemente válida,
no produce estructura parcial como sustituto silencioso.


────────────────────────────────────────────────────────────────────────
§8. PRUEBAS — FASE B
────────────────────────────────────────────────────────────────────────

§8.1 construcción LALR; §8.2 ausencia de conflictos registrada;
§8.3 compatibilidad S0 (equivalencia = igualdad por == de los Dict
limitados a las cinco claves históricas, sin exigir orden de claves);
§8.4 casos positivos (contract e invariant heredan ejemplos del Acto 13;
asiento se construye in-acto); §8.5 casos negativos; §8.6 caso integrado.


────────────────────────────────────────────────────────────────────────
§9. VERIFICACIÓN LALR EFECTIVA
────────────────────────────────────────────────────────────────────────

Construcción por éxito/falla de lark.Lark(grammar, start="start",
parser="lalr"). El número de estados del autómata no es expuesto por Lark
1.3.1 en la interfaz pública. Cuando la métrica no sea observable, se
registra la ausencia de observación, no se inventa métrica.


────────────────────────────────────────────────────────────────────────
§10. COMPATIBILIDAD CON LOS CUATRO .scfv HISTÓRICOS
────────────────────────────────────────────────────────────────────────

Reproducción de baseline. Comparación contra salida de S0 conforme §8.3.


────────────────────────────────────────────────────────────────────────
§11. FALSACIÓN IA-2
────────────────────────────────────────────────────────────────────────

Checklist de 16 puntos, incluyendo:

16. ejecución efectiva de la suite de pruebas declarada en §8. La mera
    existencia de archivos no constituye evidencia de ejecución.


────────────────────────────────────────────────────────────────────────
§12. CONDICIONES DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

§12.1 Fase A: emisión y aprobación del README.
§12.2 Fase B: materialización del código y ejecución de pruebas.

Régimen de §19.3-bis del Protocolo de Revisión de Actos, incorporado por
ACTAS/ACTA_ENMIENDA_PROTOCOLO_19_3_BIS.md.


────────────────────────────────────────────────────────────────────────
§13. LÍMITES
────────────────────────────────────────────────────────────────────────

No cierra I-3, D-12.3, H-EMG-1, H-EMG-2, D-13.2. No modifica S0. No
escribe .scfv extendidos (Acto 15).


────────────────────────────────────────────────────────────────────────
§14. DEUDAS Y REGISTRO DE CIERRE
────────────────────────────────────────────────────────────────────────

D-12.2 cerrada cuando materialización verificada y aceptada.
D-13.1 cerrada cuando construcción LALR efectiva verificada y aceptada.
El cierre se registra en el acta de materialización del Acto 14.
D-12.3 y D-13.2 permanecen abiertas.


────────────────────────────────────────────────────────────────────────
§15. CADENA DE ACTOS
────────────────────────────────────────────────────────────────────────

Acto 11 → 12 → 13 → 14 → 15 → 16. Acto 14 es el paso entre
especificación sintáctica cerrada y materialización verificable.


────────────────────────────────────────────────────────────────────────
§16. ESTADO
────────────────────────────────────────────────────────────────────────

VERSIÓN C — MATERIALIZADA.

§17. FIRMAS
IA-1: Versión C materializada.
IA-2: APTO SIN BLOQUEANTES.
OPERADOR: Materializado y firmado.

────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: cb63154a5c34626524ffe6d810861c410182fdd3d327bb049d1ae626a6e88269
Acta de referencia:      ACTA_MATERIALIZACION_14_DSL_ADL_2026-09-22
Hash final:              8309e2fc0b31716579653f7d2cab2c9d49ad2a05f9e1bcf6a946b60839619869

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 14 — MATERIALIZACIÓN DEL MÓDULO DSL ADL-SCFV — Versión C
════════════════════════════════════════════════════════════════════════

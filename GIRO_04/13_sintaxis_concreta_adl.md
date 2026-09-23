════════════════════════════════════════════════════════════════════════
ACTA DE ESPECIFICACIÓN DE LA SINTAXIS CONCRETA ADL-SCFV
Y README DEL MÓDULO DE GRAMÁTICA EXTENDIDA

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 13
Documento: GIRO_04/13_sintaxis_concreta_adl.md
Versión: E
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN BLOQUEANTES.

Estatuto: este acto declara la especificación de la sintaxis concreta
ADL-SCFV. No modifica S0. No materializa código. No cierra I-3.
No cierra D-12.2 ni D-12.3. No cierra Giro 04.

Hash previo al registro: 5bfda4c9f9726d3b84fe79eb34c62aaaa7c54aaca26fe79844fa537c56dd17da
Hash final registrado:   3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

El presente Acto declara la especificación concreta de la sintaxis ADL-SCFV
que deberá materializarse posteriormente en el módulo de gramática
extendida.

La especificación comprende:

1. "contract_def";
2. "invariant_def";
3. "asiento_declarado_def";
4. la extensión de "start";
5. el contenido mínimo del "README" del módulo "~/SCFV_DSR/dsl/";
6. las condiciones PRE, POST e INVARIANTE de las nuevas producciones;
7. los criterios de compatibilidad con la gramática S0.

Este Acto no materializa código.

Su función es declarar la especificación que permitirá cerrar, previa
falsación y materialización, las deudas declaradas en los Actos anteriores,
particularmente las derivadas del Acto 10 §5.12 y §6.2.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES
────────────────────────────────────────────────────────────────────────

La especificación se deriva de:

- Acto 10, especialmente §5.0-bis, §5.4, §5.12 y §6.2;
- Acto 11 §5-bis;
- Acto 12, extensión de la gramática ".scfv";
- ADR-003: especificación antes de implementación;
- gramática "grammar.lark" de S0;
- "parser.py" de S0;
- Aho, Lam, Sethi y Ullman, §§4.5.4, 4.7.4, 4.7.5 y 4.8.1;
- Thain, §4.4.5.

La gramática S0 de referencia mantiene:

    fractal_def: "FRACTAL" NAME "DOMINIO" "CONTABLE" ":" rule+

y constituye el precedente estructural inmediato para la extensión.

El Acto 12 estableció, además, que la extensión deberá mantener
compatibilidad hacia atrás con los ".scfv" válidos de S0.


────────────────────────────────────────────────────────────────────────
§3. NATURALEZA DE LA ESPECIFICACIÓN
────────────────────────────────────────────────────────────────────────

La presente Acta define una especificación, no una implementación.

Por tanto:

- no crea todavía "~/SCFV_DSR/dsl/";
- no modifica "grammar.lark";
- no modifica "parser.py";
- no declara materializado el módulo;
- no declara verificada la construcción LALR;
- no declara cerrada la correspondencia entre declaración y ejecución.

La materialización corresponde al Acto 14, previa aprobación de esta
especificación.


────────────────────────────────────────────────────────────────────────
§4. MODELO ESTRUCTURAL
────────────────────────────────────────────────────────────────────────

El modelo inmediato para las nuevas producciones es el patrón ya presente
en S0:

    KEYWORD + NAME + campos/literales fijos + ":" + cuerpo

En particular:

    fractal_def: "FRACTAL" NAME "DOMINIO" "CONTABLE" ":" rule+

La extensión conserva este principio, pero introduce campos declarativos
adicionales.

La especificación no presume que la nueva gramática sea libre de conflictos.
La ausencia efectiva de conflictos deberá verificarse mediante la
construcción real del parser en el Acto 14.


────────────────────────────────────────────────────────────────────────
§5. SINTAXIS DE "contract_def"
────────────────────────────────────────────────────────────────────────

§5.1 Producción

    contract_def: "CONTRATO" NAME "OBJETO" ":" NAME ["PRE" ":" expr] ["POST" ":" expr] "INVARIANTE" ":" NAME+ "ELEMENTO" ":" NAME+ ["EVIDENCIA" ":" NAME+]

§5.2 Correspondencia con Acto 10

La producción conserva la distinción establecida en Acto 10 §5.4.

Obligatorios:

1. nombre;
2. objeto;
3. invariantes asociadas;
4. elementos del sistema a los que aplica.

Condicionales:

5. precondiciones, cuando correspondan;
6. postcondiciones, cuando correspondan;
7. evidencia o referencia documental, cuando el contrato pretenda sostener
   una afirmación verificable.

Por tanto, "PRE", "POST" y "EVIDENCIA" son sintácticamente opcionales.

No se interpreta la ausencia de alguno de ellos como una afirmación semántica
sobre el contrato; únicamente significa que ese componente no fue declarado
en esa instancia.

§5.3 Referencia a invariantes

La forma:

    "INVARIANTE" ":" NAME+

declara referencias nominales a invariantes.

La gramática no verifica la existencia de los "invariant_def"
correspondientes.

La resolución de referencias, si corresponde, pertenece a una capa posterior
y no a esta producción sintáctica.

§5.4 Sobrecarga del literal "INVARIANTE"

"INVARIANTE" cumple dos funciones sintácticas:

1. literal inicial de "invariant_def";
2. literal de campo dentro de "contract_def".

No debe tratarse como un "NAME" disponible para identificadores en esos
contextos.

Esta situación se declara expresamente como parte de la gestión del espacio
de nombres reservado.

La misma regla general se aplica a los restantes literales de la gramática.

§5.5 Valores "NAME"

Los valores utilizados como:

    VENTA
    MONTO
    CUENTA_CAJA
    VALIDADA
    CONFIRMADA
    CONTABILIZADA

son "NAME" desde el punto de vista sintáctico.

No constituyen, por esta sola condición, declaraciones de variables, estados
formalizados ni tipos.

Su interpretación semántica queda fuera del alcance de esta producción.

§5.6 Ejemplos

Ejemplo 1:

    CONTRATO REGISTRO_VENTA
    OBJETO: VENTA
    PRE: monto > 0
    POST: estado == VALIDADA
    INVARIANTE: BALANCE_CONTABLE
    ELEMENTO: VENTA MONTO CUENTA_CAJA
    EVIDENCIA: FACTURA

Ejemplo 2, con los campos condicionales omitidos:

    CONTRATO REGISTRO_VENTA
    OBJETO: VENTA
    INVARIANTE: BALANCE_CONTABLE
    ELEMENTO: VENTA MONTO CUENTA_CAJA

La gramática no decide cuándo corresponde declarar PRE, POST o EVIDENCIA;
únicamente permite su presencia o ausencia conforme a la especificación.


────────────────────────────────────────────────────────────────────────
§6. SINTAXIS DE "invariant_def"
────────────────────────────────────────────────────────────────────────

§6.1 Producción

    invariant_def: "INVARIANTE" NAME "OBJETO" ":" NAME "EXPRESION" ":" expr "DOMINIO" ":" NAME "SATISFACCION" ":" expr "VERIFICACION" ":" NAME "EVIDENCIA" ":" NAME+

"DOMINIO" no es un token nuevo.

Ya existe como literal en la gramática S0, dentro de "fractal_def". Su
utilización en "invariant_def" constituye reutilización del mismo terminal.

Los literales nuevos específicos de esta producción son:

    EXPRESION
    SATISFACCION
    VERIFICACION

§6.2 Expresiones

"EXPRESION" y "SATISFACCION" utilizan "expr", no "condition".

La razón es estructural: la producción S0 "condition" incorpora la forma:

    "SI" expr

mientras que los campos declarativos de esta extensión requieren expresiones
directamente.

§6.3 Dominio

El valor situado después de:

    "DOMINIO" ":"

debe ser "NAME".

No se introduce mediante esta Acta una lista cerrada de dominios.

En consecuencia, los valores que coincidan con literales reservados
existentes no son automáticamente utilizables como "NAME".

§6.4 Ejemplo

    INVARIANTE BALANCE_CONTABLE
    OBJETO: VENTA
    EXPRESION: total_debe == total_haber
    DOMINIO: REGISTRO
    SATISFACCION: total_debe == total_haber
    VERIFICACION: MOTOR_CONTABLE
    EVIDENCIA: MAYOR

Se evita deliberadamente:

    DOMINIO: CONTABLE

porque "CONTABLE" ya es un literal reservado en la gramática S0, dentro de
"fractal_def", y no puede ocupar esta posición de "NAME".

El ejemplo anterior se sustituye por un "NAME" no reservado, como "REGISTRO".

§6.5 Valores de dominio

Los nombres utilizados como valores de "DOMINIO" no adquieren por ello una
ontología adicional.

La producción únicamente exige un "NAME".


────────────────────────────────────────────────────────────────────────
§7. SINTAXIS DE "asiento_declarado_def"
────────────────────────────────────────────────────────────────────────

La producción propuesta es:

    asiento_declarado_def: "ASIENTO_DECLARADO" NAME ":" NAME+

La producción establece un marcador declarativo mínimo.

No introduce todavía una sintaxis específica para:

    DEBE
    HABER
    CUENTA
    MONTO

ni transforma estos conceptos en terminales nuevos del lenguaje.

La profundización semántica o estructural de esta producción queda diferida
a los actos posteriores cuando exista respaldo suficiente en el corpus y en
la falsación.

El presente acto no incluye ejemplos ilustrativos de "asiento_declarado_def".
La omisión es deliberada: la producción mínima de este §7 no requiere
ejemplos para su comprensión; los ejemplos se reservan para el acto que
profundice la semántica del constructo.


────────────────────────────────────────────────────────────────────────
§8. EXTENSIÓN DE "start"
────────────────────────────────────────────────────────────────────────

La producción "start" queda conceptualmente extendida a:

    start: (contexto_def | mandante_def | booleano_def | tetrada_def | fractal_def | contract_def | invariant_def | asiento_declarado_def)*

La modificación incorpora las tres nuevas familias declarativas.

No elimina ni altera las producciones S0 existentes.


────────────────────────────────────────────────────────────────────────
§9. README DEL MÓDULO
────────────────────────────────────────────────────────────────────────

El "README" de "~/SCFV_DSR/dsl/" deberá declarar, como mínimo:

§9.1 Propósito

El módulo implementa la gramática extendida ADL-SCFV y su parser
correspondiente.

§9.2 Autoridad

La autoridad normativa del módulo deriva de la especificación formal
aprobada por el Programa de Investigación SCFV.

El código no constituye por sí mismo autoridad normativa.

La autoridad sobre la decisión profesional permanece fuera del parser. La
autoridad de escritura sobre Diario y Mayor permanece en el Motor Contable.
El parser no decide, no contabiliza y no modifica datos contables.

§9.3 Entrada

La entrada será un documento ".scfv" conforme a la gramática declarada.

§9.4 Salida

La salida del parser es una estructura "Dict[str, Any]". En la implementación
de S0, las claves observadas son: "fractales", "contexto", "mandante",
"tetrada", "booleano".

La extensión del parser en SCFV_DSR añadirá las claves correspondientes a
los nuevos constructos —contratos, invariantes, asientos_declarados o
nombres equivalentes— manteniendo las claves existentes.

La salida sintáctica no constituye por sí misma una decisión profesional ni
una escritura contable.

§9.5 Invariantes

El módulo deberá conservar:

- compatibilidad con los ".scfv" S0 válidos;
- correspondencia entre gramática y parser;
- ausencia de modificación silenciosa de la semántica S0;
- trazabilidad de las extensiones introducidas.

§9.6 Dependencias permitidas

Deberán declararse expresamente las dependencias utilizadas por el módulo.

§9.7 Dependencias prohibidas

No podrá introducirse una dependencia que modifique silenciosamente la
autoridad de la especificación o convierta una capa posterior en autoridad
normativa del lenguaje.

§9.8 Verificación

El README deberá identificar la suite de pruebas que demuestre:

1. compatibilidad histórica;
2. aceptación de las nuevas producciones;
3. rechazo de entradas sintácticamente inválidas;
4. comportamiento del parser frente a las construcciones extendidas;
5. correspondencia entre la especificación y la implementación.


────────────────────────────────────────────────────────────────────────
§10. PRE, POST E INVARIANTE DE LAS PRODUCCIONES
────────────────────────────────────────────────────────────────────────

PRE

Antes de materializar:

- la especificación deberá estar aprobada;
- las producciones deberán ser sintácticamente definidas;
- la compatibilidad S0 deberá estar declarada;
- los casos de uso ilustrativos deberán ser compatibles con los terminales
  existentes.

POST

Después de materializar:

- los ".scfv" históricos deberán continuar siendo aceptados;
- las nuevas producciones deberán ser reconocidas;
- la implementación deberá corresponder a esta especificación;
- la construcción LALR efectiva deberá haber sido verificada.

INVARIANTE

Durante la extensión:

    S0 válido → válido bajo SCFV_DSR

La extensión no podrá convertir retrospectivamente un documento S0 válido en
inválido.


────────────────────────────────────────────────────────────────────────
§11. ANÁLISIS LALR
────────────────────────────────────────────────────────────────────────

§11.1 Hipótesis

No se anticipan conflictos inevitables derivados únicamente de las
producciones declaradas.

Esta afirmación constituye una hipótesis de diseño, no una verificación.

§11.2 Verificación pendiente

La ausencia efectiva de conflictos deberá verificarse mediante la
construcción LALR real en el Acto 14.

La estabilidad de las nuevas producciones no se considera demostrada por
inspección textual de la gramática.

§11.3 Fundamento

El análisis toma como referencias:

- Aho et al., §4.5.4, relativo a conflictos durante el análisis sintáctico
  shift-reduce;
- Aho et al., §4.7.4 y §4.7.5, para la construcción de tablas LALR;
- Aho et al., §4.8.1, para el tratamiento de conflictos mediante precedencia
  y asociatividad;
- Thain, §4.4.5, para el procedimiento práctico de construcción/fusión
  utilizado en el análisis de parsers.

§11.4 Verificación de conflictos y notación

Conforme a Aho et al. §4.7.4, la construcción LALR fusiona estados con el
mismo núcleo. Esa fusión no puede introducir conflictos shift/reduce nuevos
(porque las acciones de shift dependen del núcleo, no del lookahead), pero
sí puede introducir conflictos reduce/reduce que no estaban presentes en el
autómata LR(1) original.

En consecuencia, la verificación efectiva de ausencia de ambos tipos de
conflicto corresponde al Acto 14. Thain §4.4.5 describe el procedimiento de
fusión pero no desarrolla el argumento sobre conflictos emergentes.

La notación "[" "]" para campos opcionales es notación del meta-lenguaje
Lark, no del lenguaje ".scfv" especificado. Lark 1.3.1 la admite; S0 la usa
en "list_value" con la misma función sobre el meta-lenguaje.

La notación gramatical del presente acto se escribe con una producción por
línea, conforme al estilo de S0. Lark 1.3.1 no admite continuaciones de regla
con indentación sin prefijo "|" ni paréntesis envolventes. La verificación
empírica de la construcción LALR con este formato corresponde al Acto 14.

Los usos de "NAME+" en posición media, seguidos de literales:

    "INVARIANTE" ":" NAME+
    "ELEMENTO" ":" NAME+
    "EVIDENCIA" ":" NAME+

no tienen precedente equivalente en las producciones S0 examinadas.

Su estabilidad bajo LALR depende, entre otros factores, del comportamiento
efectivo del lexer contextual utilizado por Lark y deberá verificarse
empíricamente en el Acto 14.


────────────────────────────────────────────────────────────────────────
§12. COMPATIBILIDAD HISTÓRICA
────────────────────────────────────────────────────────────────────────

La extensión deberá preservar los cuatro ".scfv" históricos utilizados como
baseline del S0.

La incorporación de:

    contract_def
    invariant_def
    asiento_declarado_def

no podrá exigir modificaciones a esos documentos históricos.

La extensión se agrega al lenguaje; no sustituye las producciones S0
existentes.


────────────────────────────────────────────────────────────────────────
§13. MATERIALIZACIÓN DIFERIDA
────────────────────────────────────────────────────────────────────────

La materialización de:

- "grammar.lark";
- "parser.py";
- "README";
- pruebas correspondientes;

queda expresamente diferida al Acto 14.

No existe autorización implícita de escritura de código derivada de esta
Acta.


────────────────────────────────────────────────────────────────────────
§14. FALSACIÓN PREVISTA POR IA-2
────────────────────────────────────────────────────────────────────────

IA-2 deberá verificar, como mínimo:

1. correspondencia exacta entre las producciones declaradas y la gramática
   S0;
2. compatibilidad de "expr" con los ejemplos;
3. tratamiento de literales reservados;
4. compatibilidad de los campos opcionales con Acto 10 §5.4;
5. reutilización de "DOMINIO";
6. comportamiento de "NAME+" en posición media;
7. compatibilidad histórica;
8. consistencia del modelo "start";
9. coherencia con ADR-003;
10. ausencia de afirmaciones de verificación anticipada.


────────────────────────────────────────────────────────────────────────
§15. LÍMITES
────────────────────────────────────────────────────────────────────────

Este Acto no establece:

- resolución semántica de referencias;
- tabla de símbolos;
- tipado;
- validación de existencia de invariantes;
- semántica completa de contratos;
- semántica contable del asiento declarado;
- generación automática de asientos;
- correspondencia completa entre declaración ADL-SCFV y runtime.

Estas materias podrán constituir actos posteriores únicamente si son
justificadas por falsación y corpus.


────────────────────────────────────────────────────────────────────────
§16. DEUDAS
────────────────────────────────────────────────────────────────────────

D-12.1 — Sintaxis concreta. Cerrada por el presente Acto, sujeta a decisión
del Operador.

D-12.2 — Implementación del parser extendido.
Responsable del tratamiento: Acto 14.

D-12.3 — Correspondencia arquitectónica entre declaración y ejecución.
Responsable del tratamiento: Acto 16.

D-13.1 — Verificación efectiva de la construcción LALR.
Responsable del tratamiento: Acto 14.

D-13.2 — Determinación posterior de la semántica de "asiento_declarado_def",
si la falsación demuestra que la forma mínima resulta insuficiente.
Responsable del tratamiento: acto posterior, no presupuestado como
modificación automática.


────────────────────────────────────────────────────────────────────────
§17. CADENA DE ACTOS
────────────────────────────────────────────────────────────────────────

    Acto 10
       ↓
    Acto 11
       ↓
    Acto 12 — extensión especificada
       ↓
    Acto 13 — sintaxis concreta especificada
       ↓
    Acto 14 — materialización + verificación LALR
       ↓
    Acto 15 — verificación de comportamiento/corpus
       ↓
    Acto 16 — correspondencia arquitectura ↔ ejecución

La cadena no implica aprobación anticipada de los actos posteriores.


────────────────────────────────────────────────────────────────────────
§18. ESTADO DEL DOCUMENTO
────────────────────────────────────────────────────────────────────────

VERSIÓN E — MATERIALIZADA.

Esta versión incorpora las correcciones derivadas de O-355, O-356, O-357,
O-358, O-359, O-360, O-361, O-363 y O-364, así como las observaciones no
bloqueantes O-365, O-366 y O-367.

O-355 queda registrada como retirada: la notación "[" "]" posee precedente
en Lark y en S0.

La construcción efectiva de la gramática extendida completa, en formato una
línea por producción, no ha sido verificada empíricamente en este Acto. La
verificación es responsabilidad del Acto 14.

El presente Acto no declara demostrada la ausencia de conflictos LALR ni la
aceptación efectiva de todos los ejemplos contra la gramática completa. Esas
verificaciones pertenecen al Acto 14.

No se mantienen bloqueantes conocidos.

El documento queda:

- materializado;
- sin autorización de escritura de código (diferida al Acto 14).


────────────────────────────────────────────────────────────────────────
§19. FIRMAS
────────────────────────────────────────────────────────────────────────

IA-1 — Constructor / extensión cognitiva
Estado: Versión E materializada.

IA-2 — Falsador
Estado: APTO SIN BLOQUEANTES.

OPERADOR — Humano / autoridad final
Estado: Materializado y firmado.
Firma: [Operador]


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 5bfda4c9f9726d3b84fe79eb34c62aaaa7c54aaca26fe79844fa537c56dd17da
Acta de referencia:      ACTA_MATERIALIZACION_13_SINTAXIS_CONCRETA_2026-09-22
Hash final:              3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 13 — SINTAXIS CONCRETA ADL-SCFV — Versión E
════════════════════════════════════════════════════════════════════════

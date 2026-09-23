════════════════════════════════════════════════════════════════════════
DOCUMENTO 10 — ADL-SCFV
Extensión del lenguaje ".scfv" como formato declarativo de contratos
arquitectónicos para SCFV_DSR

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 10
Versión: A
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada sin bloqueantes activos.

Decisiones operativas incorporadas:
  A — Referente de FRACTAL: Fractalidad Acotada.
  B — Régimen gramatical: α, extensión compatible.

Estatuto: este documento es una especificación de la extensión.
No modifica S0, ni grammar.lark, ni parser.py.
No valida SCFV_DSR.
No demuestra Fractalidad Acotada ni H-EMG-1.

Deudas internas declaradas (§5.12, §6.2, §9.2, §16.2) preservadas
como trazables. La firma certifica el texto con sus deudas, no su
resolución.

Hash previo al registro: 20989db3f08a04aa86abdedac295422071a80cdeb4fb7bc60f76048fdff2fd88
Hash final registrado:   22996478933e948ef190ee88b1d22a9c000052e36f7a4db7fa6911eed32ac5b4
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§0. TRAZABILIDAD
────────────────────────────────────────────────────────────────────────

§0.1–§0.3 — [Texto cerrado en Bloque 1 del ciclo. No disponible
textualmente en esta ventana. Se conserva por referencia al bloque 1
firmado del ciclo bilateral.]

§0.4 — Forma de argumentación externa

Cuando se invoque una fuente externa para justificar una decisión
concreta, se utilizará, cuando corresponda, la siguiente trazabilidad:

fuente externa → problema concreto → concepto invocado → contraste →
decisión de diseño.

La fuente externa se clasifica en una de tres categorías:

- extracto literal;
- paráfrasis;
- sustrato conceptual.

No constituye un nuevo canon del Programa.


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

[Texto cerrado en Bloque 1. No disponible textualmente en esta ventana.
Se conserva por referencia.]


────────────────────────────────────────────────────────────────────────
§2. NATURALEZA Y ALCANCE
────────────────────────────────────────────────────────────────────────

[Texto cerrado en Bloque 1. No disponible textualmente en esta ventana.
Se conserva por referencia.]


────────────────────────────────────────────────────────────────────────
§3. NIVEL DE FORMALIDAD
────────────────────────────────────────────────────────────────────────

§3.1 Los tres niveles de formalidad

Por analogía estructural con la distinción de niveles de formalidad
que Cervantes aplica a notaciones arquitectónicas, se distinguen:

1. informal;
2. semiformal;
3. formal.

La analogía se utiliza como instrumento para caracterizar el estado de
".scfv".

No se afirma que Cervantes haya clasificado específicamente ".scfv" ni
que su taxonomía sea directamente una taxonomía de lenguajes contables.

§3.2 Situación actual de ".scfv"

En su estado actual, ".scfv" presenta simultáneamente tres
características:

a) Formalidad sintáctica.
Existe una estructura sintáctica que permite reconocer construcciones
declarativas mediante una gramática definida.

b) Semiformalidad semántica.
La interpretación completa de determinadas construcciones depende
todavía de reglas, componentes y lógica de ejecución que no están
íntegramente expresados en el propio formato.

c) Base formal parcial.
El formato puede representar relaciones cuya estructura lógica es
susceptible de formulación y comprobación formal.

En el caso de la regla de cargo y abono:

- una formulación tabular expresa la regla contable;
- una formulación booleana expresa la misma regla;
- una formulación GF(2) expresa la misma regla;
- una formulación mediante signos expresa la misma regla.

Las formulaciones constituyen representaciones equivalentes de la
relación XNOR.

La función "ubicacion_booleana" determina la ubicación correspondiente.

La comparación:

"b == g == sig"

verifica la consistencia interna entre las formulaciones.

Determinar la ubicación y verificar la equivalencia entre las
formulaciones son operaciones distintas.

§3.3 Categoría propuesta

Para el alcance específico de esta extensión se propone utilizar la
categoría:

«semiformal contable con base formal parcial».

La categoría describe el estado del formato.

No constituye una valoración de calidad ni una afirmación de
insuficiencia global.

§3.4 Consecuencia metodológica

La categoría anterior obliga a distinguir al menos tres planos:

sintaxis declarada → semántica contable → formalización/verificación.

Una declaración sintácticamente correcta no demuestra por sí misma:

- corrección contable;
- cumplimiento de una regla;
- satisfacción de un invariante;
- comportamiento correcto del runtime.

Estas propiedades deberán ser evaluadas mediante los mecanismos
correspondientes.


────────────────────────────────────────────────────────────────────────
§4. DIRECCIÓN DUAL
────────────────────────────────────────────────────────────────────────

§4.1 Decisión D-6

La extensión adopta una dirección dual por capas:

sustancia contable ↔ formalización lógica

La dualidad no implica dos contratos independientes.

Ambas dimensiones pueden formar parte de una misma declaración
contractual.

§4.2 Capa contable declarativa

La primera capa expresa la regla contable que determina el significado
de la operación.

En el caso del asiento, la regla relaciona:

- naturaleza de la cuenta;
- movimiento;
- ubicación contable.

La representación tabular constituye la expresión declarativa de la
regla del cargo y del abono.

La fuente contable invocada para esta capa es:

Principios de Contabilidad, 4ta ed., Cap. 8.

§4.3 Capa lógica formal

La segunda capa expresa formalmente la misma regla contable.

En el caso estudiado, la regla puede representarse mediante tres
formulaciones equivalentes:

1. tabla booleana;
2. formulación GF(2);
3. formulación mediante signos.

La expresión XNOR constituye, por tanto, una forma lógica de la regla
contable, no una regla adicional.

La función:

"ubicacion_booleana(naturaleza, movimiento)"

determina la ubicación.

Las funciones equivalentes "ubicacion_booleana", "ubicacion_gf2" y
"ubicacion_signos" permiten representar la misma relación desde tres
formulaciones.

§4.4 Invariante formal

El invariante propiamente dicho no es XNOR.

El invariante es la condición de equivalencia entre las tres
formulaciones:

«"b == g == sig"»

para todas las combinaciones válidas de naturaleza y movimiento
contempladas por la regla.

Estructura conceptual:

CAPA CONTABLE
regla de cargo/abono expresada declarativamente

↕

CAPA LÓGICA FORMAL
XNOR / tabla / GF(2) / signos como formulaciones equivalentes de la
misma regla

↓

INVARIANTE
equivalencia entre las tres formulaciones

La relación no representa una secuencia causal:

«regla → invariante.»

Representa una correspondencia entre una regla sustantiva, sus
formalizaciones y una condición de consistencia entre esas
formalizaciones.

§4.5 Precedente estructural: Armani

Como antecedente externo se invoca el patrón de Armani documentado por
Reynoso, donde una declaración de tipo de componente incorpora
elementos estructurales y una declaración de "Invariant".

La utilidad del precedente para ".scfv" no consiste en copiar su
sintaxis, sino en mostrar que una unidad arquitectónica puede declarar
estructuralmente propiedades e invariantes asociados.

La adaptación al SCFV conserva una diferencia fundamental:

«Armani constituye antecedente arquitectónico; ".scfv" incorpora además
una semántica contable específica y una formalización lógica de la
regla contable.»

La notación "Component Type → Ports / Properties / Invariant" empleada
en este documento es paráfrasis de IA-1, no formulación textual de
Reynoso.

La invocación de Armani no constituye adopción ni conformidad con
Armani.

§4.6 Dirección dual y contrato único

Las dos capas pueden coexistir dentro de un mismo "CONTRATO":

CONTRATO

→ regla contable declarativa
→ formalización lógica de la regla
→ invariante de consistencia de las formalizaciones

Esto permite que el contrato exprese simultáneamente:

- qué relación contable declara;
- cómo puede formalizarse esa relación;
- qué condición debe mantenerse entre sus representaciones formales.

§4.7 Límites de la dirección dual

La dualidad propuesta no permite inferir:

«invariante satisfecho → contrato contable válido.»

Tampoco permite inferir:

«regla contable declarada → implementación correcta.»

La validez del contrato requiere mantener separadas:

- declaración;
- interpretación;
- ejecución;
- verificación;
- evidencia.

§4.8 Estado de O-191

La cuestión sobre la sintaxis concreta de "REGLA" queda delimitada por
la nueva separación:

REGLA contable ≠ formalización lógica ≠ invariante de equivalencia.


────────────────────────────────────────────────────────────────────────
§5. SINTAXIS EXTENDIDA COMPATIBLE — ADL-SCFV
────────────────────────────────────────────────────────────────────────

§5.0. Decisión arquitectónica de partida

El presente bloque se formula después de las decisiones del Operador:

- A — Referente de "FRACTAL": Fractalidad Acotada.
- B — Régimen gramatical: α, extensión compatible de la gramática
  ".scfv" existente.

En consecuencia, "SCFV_DSR" no crea una gramática ".scfv" paralela ni
redefine los constructos ya materializados en S0.

La extensión propuesta deberá conservar la sintaxis y semántica
vigentes de los constructos existentes y añadir únicamente los
elementos necesarios para expresar contratos e invariantes
arquitectónicos de "SCFV_DSR".

La implementación de cualquier modificación de "grammar.lark" o
"parser.py" queda fuera de este bloque. Conforme a ADR-003, la
especificación debe preceder a la modificación del parser.

§5.0-bis. Relación con los constructos ".scfv" existentes

El corpus existente materializa, entre otros, los siguientes
constructos:

| Constructo | Estatuto en S0 | Tratamiento en ADL-SCFV |
|---|---|---|
| CONTEXTO | existente | se conserva |
| MANDANTE | existente | se conserva |
| BOOLEANO | existente | se conserva |
| TETRADA | existente | se conserva |
| FRACTAL | existente | se conserva; referente declarado: Fractalidad Acotada |
| REGLA | existente | se conserva sin redefinición |
| CONTRATO | nuevo | extensión propuesta |
| INVARIANTE | nuevo | extensión propuesta |
| ASIENTO_DECLARADO | nuevo | extensión propuesta |

La tabla no es exhaustiva.

También se conservan los tokens estructurales del lenguaje ".scfv"
que participan en las producciones existentes, entre ellos:

SI
ENTONCES
GENERAR
CONSECUENCIA
DOMINIO
CONTABLE
Y
O
VERDADERO
FALSO

La tabla y esta enumeración no constituyen todavía una modificación de
la gramática.

Su función es declarar la relación arquitectónica entre el lenguaje
existente y la extensión propuesta.

§5.1. Principio de compatibilidad

La extensión ADL-SCFV se construirá sobre la gramática ".scfv" ya
materializada.

Por tanto:

1. un documento ".scfv" existente no deberá requerir una
   reinterpretación para conservar su significado;
2. "FRACTAL" conservará la forma materializada:

   FRACTAL <NOMBRE> DOMINIO CONTABLE:

3. "REGLA" conservará la estructura materializada:

   REGLA <NOMBRE>:
     SI <condición> ENTONCES
       <acciones>

4. la semántica imperativa-ejecutable de "REGLA" no será sustituida
   por una semántica declarativa-tabular;
5. la extensión arquitectónica se expresará mediante constructos
   nuevos, principalmente "CONTRATO" e "INVARIANTE".

La compatibilidad aquí declarada es una especificación de diseño
pendiente de verificación contra el parser activo.

§5.2. "FRACTAL"

"FRACTAL" permanece como constructo existente del lenguaje ".scfv".

La extensión no introduce una nueva sintaxis para "FRACTAL".

La forma de referencia será:

FRACTAL <NOMBRE> DOMINIO CONTABLE:

seguida de las "REGLA" correspondientes.

Dentro de "SCFV_DSR", "FRACTAL" referencia el objeto conceptual
denominado Fractalidad Acotada.

La referencia no significa que toda instancia material de "FRACTAL"
satisfaga automáticamente la conjetura.

En consecuencia:

- la Fractalidad Acotada permanece como conjetura estructural acotada
  a las transformaciones y condiciones documentadas en su corpus;
- cada instancia material de "FRACTAL" podrá o no satisfacer dicha
  conjetura;
- la satisfacción deberá determinarse mediante la evaluación
  correspondiente.

Tampoco se establece:

FRACTAL = H-EMG-1

"H-EMG-1" permanece como hipótesis de emergencia independiente:

«posibilidad de reensamblaje de los dominios históricos sobre el
Motor 9.0.0.»

Por tanto:

Fractalidad Acotada = referente estructural declarado.

H-EMG-1 = hipótesis experimental.

"FRACTAL" = constructo sintáctico/material existente mediante el cual
el diseño puede representar una estructura que se contrasta con el
referente Fractalidad Acotada.

La relación entre estos niveles permanece sometida a evaluación.

§5.3. "REGLA"

"REGLA" conserva su sintaxis y semántica existentes.

Ejemplo materializado:

REGLA VENTA_NACIONAL:
  SI monto > 0 Y tipo == "venta" ENTONCES
    GENERAR CONSECUENCIA (...)

No se adopta la forma previamente propuesta:

REGLA <n> {
  tabla
}

porque esa forma implicaría redefinir un constructo ya existente.

La representación declarativa de contratos e invariantes se desplaza a
los constructos nuevos definidos en las secciones siguientes.

§5.4. "CONTRATO"

"CONTRATO" constituye una extensión propuesta para "SCFV_DSR".

Nivel estructural propuesto: bloque de nivel superior del documento
".scfv", paralelo a los bloques de nivel superior existentes.

Su finalidad es expresar declarativamente un contrato arquitectónico
entre componentes, reglas, datos o representaciones del sistema.

Relación con "INVARIANTE": "CONTRATO" e "INVARIANTE" son ambos bloques
de nivel superior. La relación entre ellos es de referencia nominal:
un "CONTRATO" podrá citar por nombre las invariantes que le sean
aplicables, sin anidarlas dentro del bloque "CONTRATO".

Las "INVARIANTE" coexisten, por tanto, como bloques independientes.

La producción LALR concreta y la forma textual de esa referencia se
determinarán en §6.

La sintaxis concreta queda pendiente de §6.

Un contrato deberá identificar, como mínimo:

1. nombre;
2. objeto;
3. precondiciones, cuando correspondan;
4. postcondiciones, cuando correspondan;
5. invariantes asociadas;
6. elementos del sistema a los que aplica;
7. evidencia o referencia documental cuando el contrato pretenda
   sostener una afirmación verificable.

§5.5. "INVARIANTE"

"INVARIANTE" constituye una extensión propuesta para "SCFV_DSR".

Nivel estructural propuesto: bloque de nivel superior, paralelo a
"CONTRATO" y a los demás bloques de nivel superior existentes.

"INVARIANTE" no constituye un sub-bloque sintáctico de "CONTRATO".

Su relación con "CONTRATO" es referencial y nominal, no de contención.

Su finalidad es expresar propiedades que deben conservarse dentro del
objeto arquitectónico al que se vinculan.

La sintaxis concreta y la producción LALR quedan pendientes de §6.

La extensión distingue dos niveles:

Nivel contable: reglas y condiciones sobre estados y movimientos.

Nivel formal: condiciones lógicas que permitan verificar la
equivalencia o conservación declarada.

La especificación concreta de cada invariante deberá identificar:

- objeto;
- expresión;
- dominio;
- condición de satisfacción;
- procedimiento de verificación;
- evidencia.

La presencia de una declaración "INVARIANTE" no constituye por sí misma
demostración de su satisfacción.

§5.6. "ASIENTO_DECLARADO"

Nivel estructural propuesto: bloque de nivel superior, paralelo a
"CONTRATO", "INVARIANTE" y los bloques existentes.

El nombre "ASIENTO_REGISTRADO" se retira como constructo sintáctico
propuesto.

La razón es que "ASIENTO_REGISTRADO" ya posee un estatuto material
dentro del flujo de eventos del Motor S0.

Para evitar la colisión entre:

1. el evento "ASIENTO_REGISTRADO" del Motor S0; y
2. una eventual representación textual de un asiento dentro de
   ADL-SCFV,

la extensión propone el nombre:

«"ASIENTO_DECLARADO"»

"ASIENTO_DECLARADO" constituye, por tanto, un constructo nuevo
propuesto para representar declarativamente una estructura de asiento.

Ejemplo conceptual:

ASIENTO_DECLARADO:
  DEBE  110101  1000.00 VES
  HABER 410101  1000.00 VES

En este ejemplo, "DEBE" y "HABER" son convenciones expositivas del
ejemplo, no se declaran todavía como nuevos constructos o keywords de
la gramática.

El ejemplo anterior es pseudocódigo expositivo y no constituye un
documento ".scfv" parseable en el estado actual del lenguaje.

La estructura formal de "ASIENTO_DECLARADO", sus campos obligatorios,
tipos y relación con el Motor Contable deberán especificarse antes de
incorporarse al parser.

"ASIENTO_DECLARADO" tampoco sustituye al Motor Contable como autoridad
de escritura del Diario/Mayor.

§5.7. Relación entre contratos, invariantes y "REGLA"

La extensión establece una separación de responsabilidades.

Para el régimen existente:

FRACTAL
  ↓
REGLA
  ↓
ejecución de consecuencias

Para la extensión arquitectónica:

CONTRATO ↔ INVARIANTE

La segunda relación es referencial y semántica, no de anidamiento
sintáctico:

- "CONTRATO" puede referenciar una "INVARIANTE" por nombre;
- "INVARIANTE" permanece como bloque de nivel superior independiente;
- ninguna flecha de este esquema implica contención gramatical.

La primera cadena conserva el régimen existente de ".scfv".

La segunda constituye la extensión propuesta para ADL-SCFV.

No se permite utilizar "CONTRATO" o "INVARIANTE" para alterar
silenciosamente la semántica de "REGLA".

Los símbolos "↓" y "↔" utilizados en este apartado son expositivos; no
constituyen operadores gramaticales del lenguaje.

§5.8. Conservación de la representación contable

La extensión no sustituye la representación contable materializada en
S0.

Cuando una "REGLA" produzca consecuencias contables, la representación
deberá continuar expresándose mediante los elementos ya reconocidos
por el lenguaje, incluyendo:

GENERAR CONSECUENCIA (...)

Las relaciones entre naturaleza, movimiento y ubicación contable podrán
ser declaradas como invariantes o contratos de "SCFV_DSR", pero su
declaración no sustituye la semántica ejecutable de las reglas
existentes.

§5.9. XNOR como invariante formal

La extensión podrá representar la conservación del principio XNOR ya
reconocido por el Programa como un invariante formal.

La especificación deberá distinguir:

1. la regla contable que determina la ubicación;
2. la representación booleana;
3. la representación algebraica;
4. el procedimiento de verificación.

La equivalencia entre las representaciones constituye la condición
formal de consistencia.

La declaración de dicha equivalencia no constituye evidencia de que
una instancia concreta la satisfaga.

La verificación deberá permanecer separada de la declaración.

§5.10. Restricción de no redefinición

La extensión ADL-SCFV no podrá:

- redefinir "FRACTAL";
- redefinir "REGLA";
- cambiar el significado de "SI...ENTONCES";
- sustituir "GENERAR CONSECUENCIA";
- eliminar los constructos existentes;
- introducir una gramática paralela bajo el mismo régimen α;
- convertir automáticamente una declaración en evidencia;
- convertir una declaración de invariante en demostración de su
  cumplimiento.

Toda incompatibilidad detectada contra el parser activo deberá ser
tratada como deuda de diseño antes de la modificación material.

§5.11. Compatibilidad con los ".scfv" poblados

Los cuatro dominios:

ventas
compras
inventario
fiscal

aparecen materializados en el corpus histórico pre-release,
específicamente en los árboles "scfv_v6/DOMINIOS/" y
"scfv_entregable/DOMINIOS/".

Estos archivos preceden al release público S0 y se encuentran
vinculados documentalmente con la construcción de los dominios
asociados a "H-EMG-1".

Por tanto, en este documento se denominan:

«material histórico pre-release vinculado a H-EMG-1.»

No se los presenta como archivos pertenecientes al release público S0.

Su existencia constituye una condición histórica de compatibilidad que
deberá ser considerada en la evaluación de la extensión.

La extensión deberá poder coexistir con ellos sin exigir su reescritura
para conservar su significado histórico.

La eventual incorporación de contratos e invariantes sobre estos
dominios será objeto de construcción y evaluación posterior.

§5.12. Límite entre especificación y materialización

Este bloque especifica la arquitectura sintáctica propuesta.

No modifica:

- "grammar.lark";
- "parser.py";
- los ".scfv" existentes;
- S0.

No se atribuye estatuto activo a componentes legacy únicamente por su
presencia histórica en el corpus.

En particular, "verificador_booleano.py" no constituye en este
documento una dependencia normativa de la extensión. Cualquier
eventual utilización futura deberá justificarse por su relación
efectiva con la ruta de ejecución vigente.

Deuda explícita de §6: deberá analizarse la extensión de la producción
"start" de "grammar.lark" para admitir las nuevas producciones
correspondientes a "CONTRATO" e "INVARIANTE" y, si el diseño finalmente
las materializa como bloques de nivel superior, "ASIENTO_DECLARADO".

La forma exacta de esas producciones y su interacción con el análisis
LALR quedan sujetas a §6.

La modificación material del lenguaje requerirá:

1. especificación previa;
2. revisión bilateral IA-1 ↔ IA-2;
3. decisión correspondiente del Operador;
4. materialización;
5. evaluación.

§5.13. Condición de falsabilidad del bloque

§5.13.1. Verificable en el estado actual

IA-2 podrá verificar inmediatamente:

1. compatibilidad declarada de "FRACTAL" con la sintaxis existente;
2. compatibilidad declarada de "REGLA" con la sintaxis existente;
3. correspondencia de los cuatro dominios históricos pre-release;
4. ausencia de redefinición silenciosa de constructos S0;
5. preservación de la semántica imperativo-ejecutable de "REGLA"
   bajo la extensión.

Estas verificaciones pertenecen al estado actual de especificación y
corpus.

§5.13.2. Verificable después de la materialización de §6

Las siguientes verificaciones requieren que exista una especificación
formal de §6 y, cuando corresponda, su materialización:

6. coherencia de la incorporación de "CONTRATO";
7. coherencia de la incorporación de "INVARIANTE";
8. suficiencia de la definición de "ASIENTO_DECLARADO";
9. compatibilidad efectiva con el parser y con LALR;
10. separación efectiva entre declaración, verificación y evidencia;
11. comportamiento de la extensión sobre el lenguaje materializado.

La distinción evita atribuir a la especificación resultados que
únicamente pueden obtenerse mediante construcción y prueba.

§5.14. Estado

BLOQUE 3 — BORRADOR REVISADO — PENDIENTE DE FALSACIÓN DE IA-2.

No constituye modificación de la gramática ".scfv".

No constituye modificación de S0.

No constituye validación de "SCFV_DSR".

No constituye demostración de Fractalidad Acotada ni de H-EMG-1.

§5.15. Trazabilidad de decisiones

Este bloque incorpora las decisiones:

A: "FRACTAL" → referencia a Fractalidad Acotada, sin equivalencia
automática ni demostración.

B: α → extensión compatible sobre la gramática ".scfv" existente.

"CONTRATO", "INVARIANTE" y "ASIENTO_DECLARADO" se declaran como bloques
de nivel superior.

"CONTRATO" e "INVARIANTE" mantienen una relación referencial nominal,
no una relación de anidamiento sintáctico.

La producción sintáctica concreta, la extensión de "start" y su
validación LALR quedan como objeto de §6.

La materialización técnica permanece pendiente de la especificación,
falsación y decisión documental correspondientes.


────────────────────────────────────────────────────────────────────────
§6. GRAMÁTICA EXTENDIDA Y ANÁLISIS LALR
────────────────────────────────────────────────────────────────────────

La extensión propuesta para ".scfv" se formula como una extensión
compatible sobre la gramática existente, conforme a la decisión B = α.

No se propone sustituir la gramática existente ni crear un lenguaje
alternativo.

La gramática vigente constituye el sustrato de compatibilidad y
conserva, como mínimo, los constructos ya materializados:

- "CONTEXTO";
- "MANDANTE";
- "BOOLEANO";
- "TETRADA";
- "FRACTAL";
- "REGLA".

Asimismo, se conservan los elementos sintácticos asociados al régimen
existente, incluyendo:

- "DOMINIO";
- "CONTABLE";
- "SI";
- "ENTONCES";
- "GENERAR";
- "CONSECUENCIA";
- "Y";
- "O";
- "VERDADERO";
- "FALSO".

La extensión propuesta incorpora nuevos bloques de nivel superior:

- "CONTRATO";
- "INVARIANTE";
- "ASIENTO_DECLARADO".

Estos bloques no sustituyen los existentes.

§6.1 Regla de compatibilidad

La regla fundamental de la extensión es:

«Todo constructo actualmente válido del régimen ".scfv" deberá conservar
su significado y forma sintáctica bajo la extensión, salvo que un acto
posterior declare expresamente una modificación compatible y
verificable.»

En particular:

"FRACTAL <NOMBRE> DOMINIO CONTABLE:"

permanece como forma sintáctica de "FRACTAL".

Asimismo:

"REGLA <NOMBRE>: SI ... ENTONCES ..."

permanece como forma sintáctica de "REGLA".

La extensión no redefine "REGLA" como tabla declarativa.

§6.2 Extensión del símbolo inicial

La deuda declarada en §5.12 consiste en extender el símbolo inicial
("start") de la gramática para admitir los nuevos bloques, conservando
la cardinalidad heredada (cero o más bloques por documento).

La extensión conceptual prevista es:

start
  → (constructo_existente
    | contract_def
    | invariant_def
    | asiento_declarado_def)*

La forma exacta de producción deberá ajustarse a la gramática LALR
existente.

Los nuevos bloques participan de la cardinalidad repetible de "start",
salvo restricciones posteriores que sean especificadas y falsadas.

No se autoriza inferir que esta producción ya existe en "grammar.lark".

Su incorporación constituye trabajo posterior de materialización.

§6.3 Relación con LALR

La extensión deberá analizarse contra el parser LALR actualmente
utilizado por el Programa.

§6.3.1 Verificable en especificación

Criterios verificables contra el corpus vigente:

- compatibilidad de los constructos existentes;
- conservación del reconocimiento de "FRACTAL";
- conservación del reconocimiento de "REGLA";
- conservación de la semántica imperativo-ejecutable de "REGLA".

§6.3.2 Verificable tras materialización

Criterios que requieren parser extendido:

- ausencia de conflictos léxicos introducidos por los nuevos tokens;
- ausencia de conflictos shift/reduce no resueltos;
- ausencia de conflictos reduce/reduce;
- reconocimiento inequívoco de "CONTRATO";
- reconocimiento inequívoco de "INVARIANTE";
- reconocimiento inequívoco de "ASIENTO_DECLARADO".

La expresión de estos criterios constituye especificación de
evaluación; no constituye todavía evidencia de que la extensión los
satisfaga.

§6.4 Separación sintáctica

Los nuevos bloques deberán poseer delimitación suficiente para evitar
que un documento existente pueda ser reinterpretado accidentalmente
como un documento extendido.

En particular, la presencia de:

CONTRATO
INVARIANTE
ASIENTO_DECLARADO

deberá ser inequívocamente reconocible por el parser.

No se utilizarán como alias de palabras reservadas existentes.

§6.5 Compatibilidad retrospectiva

La extensión no modifica retroactivamente los documentos ".scfv"
existentes.

Los documentos históricos deberán continuar siendo interpretables bajo
la gramática que les correspondía.

La coexistencia temporal de documentos históricos y documentos
extendidos deberá distinguir:

- régimen histórico;
- régimen extendido;
- versión de gramática;
- parser utilizado;
- resultado de validación.

§6.6 Estado de §6

La presente sección constituye especificación propuesta pendiente de
falsación.

No declara que "grammar.lark" haya sido modificado.

No declara que "parser.py" haya sido modificado.

No declara que el parser LALR haya aceptado la extensión.


────────────────────────────────────────────────────────────────────────
§7. SEMÁNTICA CONTABLE DECLARATIVA
────────────────────────────────────────────────────────────────────────

La extensión ".scfv" incorpora una capa declarativa destinada a
expresar contratos, invariantes y asientos declarados sin confundir
dicha declaración con su ejecución o verificación.

La semántica se organiza en tres niveles:

1. declaración;
2. verificación;
3. evidencia.

La declaración expresa lo que el artefacto afirma.

La verificación comprueba una propiedad contra una representación o
ejecución.

La evidencia documenta el resultado observado.

Ninguno de estos niveles sustituye a los otros.

§7.1 Regla Debe/Haber

En el contexto contable, la representación declarativa podrá expresar
las correspondencias entre:

- naturaleza;
- movimiento;
- ubicación contable.

Los términos naturaleza, movimiento y ubicación constituyen
terminología interna del Programa, introducida en §4.2 y pendiente del
locus externo preciso (O-216, diferida).

La convención expositiva utilizada en §5 no constituye por sí misma una
nueva regla contable del S0.

La regla material continúa siendo la correspondiente al régimen
contable y al Motor vigente.

§7.2 XNOR como invariante formal

La extensión puede expresar la conservación lógica entre distintas
representaciones de una misma regla.

La equivalencia entre:

- representación tabular;
- representación booleana;
- representación algebraica sobre GF(2);
- representación mediante signos;

podrá constituir una propiedad formal verificable.

La declaración de esa equivalencia no demuestra que una implementación
concreta la satisfaga.

§7.3 No confusión entre regla e invariante

Una "REGLA" existente expresa una operación imperativo-ejecutable.

Un "INVARIANTE" expresa una propiedad que debe conservarse o
verificarse.

Por tanto:

«"REGLA ≠ INVARIANTE".»

La extensión mantiene esta distinción.

§7.4 No confusión entre contrato y evidencia

Un "CONTRATO" expresa una relación declarada entre componentes o
condiciones.

No constituye evidencia de que dichos componentes estén materializados
ni de que la relación se cumpla en ejecución.


────────────────────────────────────────────────────────────────────────
§8. SEMÁNTICA FORMAL DEL CONTRATO ARQUITECTÓNICO
────────────────────────────────────────────────────────────────────────

El "CONTRATO" se utiliza como unidad declarativa de relación
arquitectónica.

Su función es hacer explícitas las condiciones que una interfaz,
componente o representación debe satisfacer.

§8.1 Estructura conceptual

Un contrato podrá expresar:

CONTRATO <nombre>
  SUJETO <componente>
  REQUIERE <condición>
  GARANTIZA <propiedad>
  REFERENCIA <nombre_invariante>

REFERENCIA <nombre_invariante> no constituye contención sintáctica de
INVARIANTE; identifica nominalmente una definición independiente.

La sintaxis anterior es esquemática hasta su incorporación efectiva a
la gramática.

Los tokens SUJETO, REQUIERE, GARANTIZA y REFERENCIA son convenciones
expositivas del esquema; no se declaran todavía como keywords de la
gramática.

No debe interpretarse como gramática LALR ya implementada.

§8.2 Relación con INVARIANTE

"CONTRATO" e "INVARIANTE" permanecen como bloques de nivel superior.

La relación entre ambos es nominal o referencial, no de anidamiento
sintáctico obligatorio.

Un contrato puede declarar que queda sujeto a un invariante
identificado por nombre.

El invariante conserva su propia definición.

§8.3 Contrato arquitectónico

El contrato sirve para explicitar interfaces entre niveles del
artefacto.

En el contexto SCFV_DSR puede expresar, por ejemplo:

- entrada requerida;
- salida esperada;
- propiedad conservada;
- condición contable;
- relación entre componentes.

La existencia del contrato no demuestra cumplimiento.

§8.4 Distinción entre contrato y ejecución

Un contrato puede existir aunque:

- el componente no esté materializado;
- el parser todavía no lo reconozca;
- la propiedad no haya sido evaluada;
- la evidencia sea inexistente;
- la evaluación produzca FAIL.

Esta separación es necesaria para conservar la trazabilidad
epistemológica del Programa.


────────────────────────────────────────────────────────────────────────
§9. RUNTIME MÍNIMO Y DECISIONES FUERA DEL CONTRATO
────────────────────────────────────────────────────────────────────────

La extensión deberá evitar que decisiones semánticas relevantes
aparezcan implícitamente en el runtime sin correspondencia documental.

La regla de diseño es:

«No introducir decisiones semánticas contables no declaradas fuera del
contrato cuando dichas decisiones sean necesarias para interpretar el
artefacto.»

Esto no significa que toda operación interna de software deba
convertirse en un contrato.

Se refiere a decisiones que afecten la interpretación contable,
arquitectónica o normativa del artefacto.

§9.1 Decisiones explícitas

Cuando una decisión sea necesaria para determinar:

- naturaleza;
- movimiento;
- cuenta;
- consecuencia;
- conservación de un invariante;
- interpretación normativa;

deberá existir una localización identificable para dicha decisión.

§9.2 Decisión no declarada

Una decisión semántica que aparezca exclusivamente en código y no tenga
correspondencia declarativa deberá registrarse como:

«deuda de completitud contractual»

hasta que se determine documentalmente su estatuto.

§9.3 Portabilidad

La portabilidad del artefacto no se presume por la existencia de una
sintaxis ".scfv".

Deberá comprobarse que otro entorno capaz de interpretar el formato
puede reconstruir las condiciones relevantes sin depender de
decisiones ocultas del entorno original.


────────────────────────────────────────────────────────────────────────
§10. RELACIÓN CON LOS ADL EXTERNOS
────────────────────────────────────────────────────────────────────────

El diseño de ADL-SCFV se contrasta metodológicamente con antecedentes
de lenguajes de descripción arquitectónica.

Se consideran como referencias de contraste los materiales efectivamente
incorporados al corpus del ciclo.

La comparación tiene carácter metodológico.

No constituye declaración de conformidad con un estándar externo.

§10.1 Reynoso

Reynoso se utiliza como referencia para el análisis de lenguajes y
descripción arquitectónica según el corpus disponible.

Cuando una formulación sea una construcción interpretativa de IA-1,
deberá distinguirse de una cita literal.

§10.2 Armani

La referencia a Armani se utiliza en la medida en que aparece
documentada mediante el corpus efectivamente disponible.

Las estructuras internas de SCFV_DSR no deberán atribuirse literalmente
a Armani cuando constituyan una construcción propia.

§10.3 Wright y Acme

La presente sección no atribuye contenido documental específico a
Wright o Acme más allá de lo que se encuentre efectivamente respaldado
por el corpus incorporado al ciclo.

La ausencia de una fuente primaria disponible no será sustituida por
una inferencia presentada como cita.

§10.4 Principio metodológico

Los ADL externos funcionan como:

«marcos de contraste para el diseño de ADL-SCFV.»

No funcionan como autoridad normativa del SCFV.


────────────────────────────────────────────────────────────────────────
§11. RELACIÓN CON EL PROTOCOLO DE REVISIÓN DE ACTOS
────────────────────────────────────────────────────────────────────────

ADL-SCFV no constituye un canon metodológico.

Por tanto, la incorporación de conceptos de ADL al documento 10 no
activa por sí misma el régimen reservado a la activación de cánones
externos.

El documento permanece sometido al Protocolo de Revisión de Actos por
su condición de acto documental del Programa.

La relación jerárquica permanece:

Protocolo → Operador → decisiones del Programa → especificaciones y
marcos de contraste.

La presente especificación no modifica el Protocolo.

§11.1 Declaración no equivale a validación

La definición de un contrato, invariante o constructo sintáctico no
constituye validación.

§11.2 Aplicación de Hevner

Hevner continúa operando como canon metodológico externo de contraste
conforme a su activación y extensión vigente.

La especificación de ADL-SCFV podrá ser objeto de contraste metodológico
bajo ese canon.


────────────────────────────────────────────────────────────────────────
§12. ALCANCE Y LÍMITES
────────────────────────────────────────────────────────────────────────

La presente extensión se circunscribe a:

«SCFV_DSR y sus derivados experimentales del Giro 04.»

No constituye modificación de S0.

No constituye una nueva versión pública de S0.

No modifica retrospectivamente:

- "grammar.lark";
- "parser.py";
- los ".scfv" históricos;
- el Motor Contable;
- el Protocolo;
- la Fractalidad Acotada como elemento del núcleo;
- las decisiones ya materializadas.

§12.1 No generalización automática

La existencia de ADL-SCFV no crea una regla automática para futuros
giros.

Cualquier adopción posterior deberá quedar documentada.

§12.2 No equivalencia con S0

La extensión no convierte SCFV_DSR en S0.

S0 permanece como material antecedente y release previamente cerrado.

§12.3 No validación del artefacto

El presente documento no demuestra:

- H-EMG-1;
- H-EMG-2;
- fractalidad;
- reutilización;
- funcionamiento;
- portabilidad;
- suficiencia experimental.

Estas cuestiones permanecen abiertas a evaluación.


────────────────────────────────────────────────────────────────────────
§13. FALSADORES DEL DISEÑO
────────────────────────────────────────────────────────────────────────

La especificación queda sometida, como mínimo, a los siguientes
falsadores.

F-1 — Incompatibilidad sintáctica
La extensión produce conflictos con la gramática existente o impide
analizar documentos previamente válidos.

F-2 — Incompatibilidad LALR
La incorporación de los nuevos constructos produce conflictos no
resueltos en el parser LALR.

F-3 — Redefinición silenciosa
La extensión cambia el significado de "FRACTAL" o "REGLA" sin
declaración explícita.

F-4 — Pérdida de semántica
"REGLA" deja de conservar su carácter imperativo-ejecutable.

F-5 — Colisión semántica
Un nuevo constructo adquiere el significado de un constructo existente
sin una declaración documental que lo justifique.

F-6 — Decisión oculta
El runtime introduce decisiones contables o arquitectónicas relevantes
que no poseen correspondencia declarativa.

F-7 — Insuficiencia contractual
Los contratos no permiten reconstruir las relaciones que pretenden
declarar.

F-8 — Falsa formalidad
El documento denomina "formal" una propiedad que no puede ser verificada
mediante una representación formal efectiva.

F-9 — Confusión declaración/evidencia
La existencia de una declaración se presenta como prueba de
cumplimiento.

F-10 — Dependencia externa no trazada
El diseño requiere una fuente o componente externo cuya procedencia no
pueda ser identificada.

Mapeo de trazabilidad con los criterios de §5.13 y §6.3:

F-1 ↔ §6.3.2
F-2 ↔ §6.3.2
F-3 ↔ §5.13.1.4
F-4 ↔ §5.13.1.5
F-5 ↔ §8
F-6 ↔ §9.2
F-7 ↔ §8.2
F-8 ↔ §7.2
F-9 ↔ §7.4
F-10 ↔ §10.4


────────────────────────────────────────────────────────────────────────
§14. ESTADO DEL DOCUMENTO
────────────────────────────────────────────────────────────────────────

En esta fase el documento 10 queda clasificado como:

«BORRADOR DE ESPECIFICACIÓN — PENDIENTE DE FALSACIÓN BILATERAL»

Los bloques §6–§13 constituyen construcción de IA-1.

Este documento es una especificación de la extensión, no la extensión
materializada. La sintaxis efectiva de los constructos nuevos se
determinará en el acto de materialización correspondiente, sujeto a
decisión del Operador.

No se declara:

- APTO;
- materializado;
- firmado;
- vigente;
- implementado.

El documento solamente podrá cambiar de estado después de la falsación
correspondiente y de la decisión del Operador.


────────────────────────────────────────────────────────────────────────
§15. CICLO BILATERAL DE CONSTRUCCIÓN Y FALSACIÓN
────────────────────────────────────────────────────────────────────────

El documento 10 seguirá el siguiente ciclo:

IA-1 construye → IA-2 falsifica → IA-1 integra → IA-2 verifica →
Operador decide.

Cada bloque podrá generar:

- convergencia;
- divergencia;
- objeción;
- enmienda;
- deuda;
- emergencia metodológica;
- enriquecimiento.

Una objeción de IA-2 no será tratada automáticamente como defecto
definitivo.

IA-1 deberá responderla mediante:

1. aceptación;
2. corrección;
3. justificación;
4. delimitación;
5. traslado a deuda;
6. solicitud de decisión del Operador cuando corresponda.

§15.1 Regla de no materialización anticipada

Mientras existan bloqueantes activos en el documento, no se considerará
concluida la especificación.

La materialización queda posterior a:

1. construcción completa;
2. falsación;
3. integración;
4. verificación;
5. decisión del Operador.


────────────────────────────────────────────────────────────────────────
§16. INTEGRIDAD, MATERIALIZACIÓN Y CIERRE
────────────────────────────────────────────────────────────────────────

Una vez que el documento completo haya superado la falsación bilateral,
deberá ensamblarse en un único archivo:

"GIRO_04/10_adl_scfv.md"

La secuencia documental será:

1. integración de §0–§16;
2. revisión de numeración y referencias internas;
3. verificación de ausencia de bloques pendientes;
4. generación de versión candidata;
5. firma o constancia pre-hash correspondiente;
6. materialización por el Operador;
7. cálculo del SHA-256 del archivo materializado;
8. registro del hash;
9. constancia de estado;
10. incorporación a la trazabilidad del Giro 04.

La constancia de materialización seguirá el régimen de §19.3-bis del
Protocolo: encabezado declarativo → cuerpo → hash previo → registro →
hash final.

El hash deberá corresponder al archivo efectivamente materializado.

No deberá confundirse:

- hash de una fuente externa;
- hash de una versión previa;
- hash del contenido del chat;
- hash del archivo final materializado.

§16.1 Condición de cierre

El documento 10 podrá considerarse cerrado únicamente cuando exista
constancia documental que indique:

«DOCUMENTO 10 — MATERIALIZADO Y FIRMADO»

La materialización no implica que la implementación de la extensión ya
exista.

La implementación posterior de "grammar.lark", "parser.py" u otros
componentes deberá constituir una actuación diferenciada y trazable.

§16.2 Resultado metodológico esperado

Si la especificación supera la falsación y posteriormente se materializa,
el Programa dispondrá de una definición documental de ADL-SCFV que:

- conserva el lenguaje ".scfv" existente;
- extiende el lenguaje de forma compatible;
- preserva "FRACTAL";
- preserva "REGLA";
- distingue declaración, verificación y evidencia;
- permite expresar contratos arquitectónicos;
- permite declarar invariantes;
- permite representar asientos declarados sin colisionar con
  "ASIENTO_REGISTRADO";
- mantiene S0 fuera de la extensión;
- deja trazable la relación entre arquitectura y contabilidad;
- permanece abierta a falsación mediante evidencia posterior.


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 20989db3f08a04aa86abdedac295422071a80cdeb4fb7bc60f76048fdff2fd88
Acta de referencia:      ACTA_MATERIALIZACION_10_ADL_SCFV_2026-09-22
Hash final:              22996478933e948ef190ee88b1d22a9c000052e36f7a4db7fa6911eed32ac5b4

════════════════════════════════════════════════════════════════════════
FIN DEL DOCUMENTO 10 — ADL-SCFV — Versión A
════════════════════════════════════════════════════════════════════════

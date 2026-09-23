06_diseno.md

GIRO 04 · PROGRAMA DE INVESTIGACIÓN SCFV

Identificador: 06_diseno.md
Versión: V3 · consolidada con correcciones T1, T2 y ciclo de falsación
Nivel: DISENO
Unidad del acto: DISENO_ARTEFACTO_SCFV_DSR, conforme Protocolo §2
Naturaleza: Diseño del artefacto SCFV_DSR
Marco: Hevner & Chatterjee 2010 (Design Science Research)
Ruta de investigación: Sampieri Cap 2–4 (Caps 5–6 declarados; Caps 8–10 diferidos)
Estatuto epistemológico: DISENO — V3 · CERRADO EN FALSACIÓN
Antecedentes: 01_idea.md, 02_planteamiento.md V4d, 03_rutas.md V2, 04_ipve_operacionalizado.md V2, 05_marco_teorico.md V1
Régimen: invocación operativa. Sin adopción formal de fuentes externas.
Nota de versión: V3 sustituye al borrador V2. V2 no fue materializado en disco.
Estado de materialización: MATERIALIZADO por decisión del Operador.

Estructura:
- Parte 1 — Fundamento (§0–§5)
- Parte 2 — Artefacto y materialización (§6–§14)
- Parte 3 — Congruencia, deudas, falsación y cierre (§15–§20)
- §21 — Consolidación del ciclo de falsación
- §22 — Firmas

---

PARTE 1 — FUNDAMENTO

§0 — Estatuto del documento

El presente documento especifica el diseño del artefacto SCFV_DSR del Giro 04 del Programa de Investigación SCFV.

El estatuto metodológico adoptado es Design Science Research (DSR), conforme a Hevner & Chatterjee (2010).

La adopción de DSR constituye un estatuto metodológico. No constituye, por sí misma, demostración de una contribución científica.

En consecuencia:

«DSR confirmado = estatuto metodológico adoptado.»

La contribución, utilidad, calidad y eficacia del artefacto quedan sometidas al ciclo DSR de construcción, evaluación y refinamiento.

La articulación metodológica del Giro 04 es:

«Sampieri → organiza la investigación.
Hevner → estructura el diseño.
Rodríguez → rige el proceso de diseño.
XNOR → rige el núcleo del producto.»

Esta articulación no establece equivalencia entre los cuatro elementos. Cada uno cumple función distinta.

Advertencia de rigor: el uso del knowledge base (KB) no equivale a contribución al KB. Hevner L1476–1481 distingue DSR (contribución) de professional design (aplicación). El presente diseño declara su estatuto DSR en función de los constructs nuevos y las dos kernel theories, no del reuso de componentes de S0.

§1 — Objeto

§1.1 — Artefacto SCFV_DSR

El objeto del diseño es el artefacto SCFV_DSR, orientado a investigar la representación y evaluación de secuencias de movimientos contables como trayectorias observables de estado.

El artefacto se denomina SCFV_DSR (Design Science Research del Programa SCFV). No se identifica con la designación interna S1 utilizada por SCFV-S0 para el espacio de reensamblaje. El nombre declara el estatuto metodológico del artefacto.

§1.2 — Fractalidad acotada

La relación entre S0 y el artefacto se formula como fractalidad acotada, conforme a FRACTALIDAD_ACOTADA.md L142–143:

«Fractalidad ≠ identidad de representación.
Fractalidad = preservación mediante representación suficiente.»

El diseño no presupone identidad de representación entre S0 y el artefacto. La pregunta de investigación es si determinadas propiedades relevantes pueden preservarse mediante una representación suficiente dentro de los límites del artefacto.

§1.3 — Materialización de segundo orden

El diseño se encuentra bajo la condición establecida por el Fundacional §13:

«El Programa de Investigación SCFV no solamente investiga el conocimiento; investiga también las condiciones mediante las cuales puede investigar su propio conocimiento.»

Y por el Fundacional §32:

«Cada cierre de un giro puede modificar las condiciones del siguiente.»

La formulación adoptada es materialización de segundo orden, no «fractal de segundo orden». La primera corresponde a la condición reflexiva del Programa; la segunda no se adopta como categoría del diseño.

§1.4 — Precedente histórico de fractales

SCFV-S0 materializó fractales de dominio (Ventas, Compras, Inventario, Fiscal) en su historial. Estos fractales fueron eliminados del Release S0. La carpeta DOMINIOS/ no existe en el Release.

Los fractales constituyen precedente histórico del Programa, no componente operativo vigente. Su eventual reensamblaje sobre el Motor es objeto de hipótesis emergente (H-EMG-1).

§1.5 — Relación Programa / S0 / SCFV_DSR

El Fundacional L25–26 declara:

«El Programa de Investigación SCFV no es SCFV-S0. SCFV-S0 es la primera realización material del Programa.»

El Contrato del Release S0 (§6, punto 7) declara el Fundacional fuera del alcance contractual de S0-v1.0.0.

El SCFV_DSR es una nueva materialización del Programa, con S0 como antecedente material. No es derivado de S0. Se ancla al Programa en su fundamento y a S0 en su material.

§2 — Objetivos

§2.1 — Objetivos sampierianos (O1–O8)

El diseño está condicionado por los objetivos O1–O8 de 02_planteamiento.md §11. Se reproducen literalmente:

- O1. Delimitar provisionalmente ESTADO_OBSERVABLE.
- O2. Construir una representación conceptual de sucesiones de estados y movimientos.
- O3. Identificar propiedades susceptibles de evaluación.
- O4. Examinar invariantes, restricciones y condiciones potencialmente aplicables.
- O5. Determinar qué evidencias serían necesarias.
- O6. Delimitar qué aspectos pueden verificarse sin inferir intención.
- O7. Examinar la relación conceptual entre omisiones y representación/evaluación de trayectorias.
- O8. Evaluar la sostenibilidad de TRAYECTORIA_ESTADO dentro del Programa.

Los objetivos O1–O8 constituyen condiciones de investigación para el diseño. Esta sección reproduce su redacción literal. No se altera ningún objetivo.

Nota: la delimitación del estatuto de ESTADO_ESPERADO no forma parte de los O1–O8. Consta en 02_planteamiento.md §7 como estatuto del término. Se registra como concepto auxiliar del diseño.

§2.2 — Objetivos hevnerianos y problemas de diseño heredados

El diseño adopta cinco objetivos DSR operativos:

- H1 — Artefacto. Producir una materialización viable.
- H2 — Relevancia. Atender un problema de investigación relevante.
- H3 — Evaluación. Establecer procedimientos de evaluación.
- H4 — Contribución. Identificar y someter a evaluación la posible contribución.
- H5 — Rigor. Construir y evaluar con fundamentos explícitos.

Adicionalmente, el diseño incorpora cuatro problemas de diseño heredados del Giro 03 como objeto del artefacto:

- MODELO_SECUENCIA
- EVALUACION_TRAYECTORIAS
- OPERACIONALIZACION_2_2
- REPRESENTACION_RELACIONAL_PCU

Nota de elevación de estatuto (T1): las cuatro formulaciones constan en 02_planteamiento.md §17 como «antecedentes de la idea» con estatuto declarado «Contenido no estabilizado» y procedencia 01_idea.md §1.1. El presente diseño las eleva a problemas de diseño heredados como acto propio de este documento. Esta elevación de estatuto se declara expresamente. No se altera el planteamiento materializado.

Estos problemas no son guidelines de Hevner. Son problemas de diseño del Programa.

§2.3 — Condicionamiento entre objetivos

| Objetivo DSR | Objetivos sampierianos condicionantes |
|---|---|
| H1 — Artefacto | O1–O8 |
| H2 — Relevancia | O1, O2, O5, O8 |
| H3 — Evaluación | O4, O5, O6, O7 |
| H4 — Contribución | O8 |
| H5 — Rigor | O1–O8 |

La tabla establece relación de diseño. No convierte los objetivos sampierianos en DSR ni viceversa.

§3 — Estatuto DSR

§3.1 — DSR y no diseño profesional

Hevner L993:

«Design science research is a research paradigm in which a designer answers questions relevant to human problems via the creation of innovative artifacts, thereby contributing new knowledge to the body of scientific evidence.»

Traducción propia: [Investigación en ciencia del diseño es un paradigma de investigación en el cual un diseñador responde preguntas relevantes a problemas humanos mediante la creación de artefactos innovadores, contribuyendo así nuevo conocimiento al cuerpo de evidencia científica.]

Y L1476–1481:

«Professional design is the application of existing knowledge to organizational problems, such as constructing a financial or marketing information system using 'best practice' artifacts (constructs, models, methods, and instantiations) existing in the knowledge base. On the other hand, design science research addresses important unsolved problems in unique or innovative ways or solved problems in more effective or efficient ways. The key differentiator between professional design and design research is the clear identification of a contribution to the archival knowledge base of foundations and methodologies and the communication of the contribution to the stakeholder communities.»

Traducción propia: [El diseño profesional es la aplicación de conocimiento existente a problemas organizacionales. La investigación en ciencia del diseño aborda problemas no resueltos de maneras únicas o innovadoras. El diferenciador clave es la clara identificación de una contribución al KB archivístico y su comunicación.]

El Giro 04 se sitúa en el segundo estatuto porque introduce constructs nuevos (TRAYECTORIA_ESTADO, ESTADO_OBSERVABLE, categorías de omisión) y dos kernel theories.

§3.2 — Precisión sobre la contribución

La declaración DSR no equivale a declarar una contribución demostrada.

El estatuto correcto es:

«DSR = estatuto metodológico adoptado.»

La eventual contribución deberá ser identificada, materializada, evaluada, sometida a los criterios de rigor y comunicada cuando corresponda.

V3 no declara que el artefacto ya constituya una contribución demostrada.

§3.3 — Hipótesis emergentes del design cycle

El diseño declara dos hipótesis emergentes, ambas pertenecientes al ciclo DSR:

H-EMG-1 — Reensamblaje de fractales históricos. Los fractales de dominio (Ventas, Compras, Inventario, Fiscal) materializados en el historial de SCFV-S0 y eliminados del Release S0 podrían reensamblarse sobre el Motor 9.0.0 en el SCFV_DSR.

H-EMG-2 — Reutilización como motor contable. El SCFV_DSR podría operar como motor contable reutilizable en sistemas que trabajen con partida doble.

Ambas son falseables en iteraciones build-evaluate del design cycle. Su refutación no invalida el diseño completo; produce información sobre los límites del artefacto.

§3.4 — Ausencia de hipótesis causal

El diseño no introduce hipótesis causal. Coherente con 02_planteamiento.md §18.

Sampieri L9355: «No, no siempre debemos establecer hipótesis. Formulamos o no hipótesis dependiendo del alcance inicial del estudio.»

Tabla 6.2: exploratorio → no se formulan hipótesis.

Las hipótesis emergentes del §3.3 no son sampierianas. Pertenecen al ciclo DSR.

§4 — Rodríguez: tres formulaciones performativas

El diseño adopta tres formulaciones del Fundacional §2 como invariantes performativos del proceso de diseño.

§4.1 — Cita 1 (Operación, Dogma, Disciplina y Economía)

Cita completa del Fundacional §2.1:

«Toda operacion se funda en un Dogma, se rige por una Disciplina, propia del Dogma, y se ejecuta con una economia propia de la Disciplina.»

El Fundacional introduce esta formulación como «motor epistemológico generador».

La formulación establece: fundamento → disciplina → operación.

Para el diseño: Dogma → Disciplina → Economía → Operación.

La secuencia no constituye declaración retrospectiva de la arquitectura interna de SCFV-S0. Es estructura que rige el proceso de diseño.

§4.2 — Cita 2 (Educación Popular y ejercicios útiles)

Cita completa del Fundacional §2.2:

«Educación Popular
Destinacion á Ejercicios útiles
Aspiracion fundada á la propiedad.»

Y continúa:

«Son cosas palpables, por consiguiente mas persuasivas, que cuantos discursos pueda hacer la elocuencia mas vehemente.»

El Fundacional interpreta esta formulación como exigencia de materialización:

«conocimiento → ejercicio → apropiación → materialización.»

Para el diseño: Educación Popular → Ejercicios útiles → Apropiación → Cosas palpables.

§4.3 — Cita 3 (Invención y error)

Cita completa del Fundacional §2.3:

«O Inventamos o Erramos.»

El diseño adopta esta formulación como principio generador de un proceso abierto a la invención y al error.

El Fundacional añade:

«El Programa no presume que todo error produzca conocimiento. Debe investigarse qué ocurre con el error, cómo se confronta y qué transformación produce.»

Definición operativa de Rodríguez raw L18196–18200:

«Error / se toma aquí, por todo lo que significa errar ═ / no dar con el punto o con el fin / no tener lugar fijo / que es / desviarse / vagar»

§4.4 — Carácter performativo

Las tres formulaciones son performativas dentro del proceso de diseño. No describen. Reglan.

- Cita 1 estructura el acto (Dogma → Disciplina → Economía → Operación).
- Cita 2 exige materialización.
- Cita 3 expone a error.

§4.5 — Discrepancia 3 vs 4 términos

La cita de Rodríguez contiene cuatro términos: Dogma, Disciplina, Economía, Operación.

El Fundacional descompone la relación en tres términos (L34):

«Esta formulación establece una relación entre: fundamento → disciplina → operación.»

Esta diferencia no es contradicción textual. Es variación hermenéutica de representación. No se elimina ningún término de la cita original. No se atribuye la estructura cuádruple como arquitectura declarada de S0.

§5 — Dos teorías kernel

El diseño adopta explícitamente dos teorías kernel, diferenciadas por función:

1. Rodríguez → kernel de proceso.
2. XNOR → kernel de producto.

§5.1 — Rodríguez como kernel de proceso

Hevner L2540–2600 declara la estructura de ISDT:

- «Kernel design product theories, theories from natural and social sciences that govern design requirements.»
- «Kernel-design process theories, theories from natural or social sciences that inform the design process.»

Traducción propia: [Teorías kernel de producto: gobiernan los requerimientos de diseño. Teorías kernel de proceso: informan el proceso de diseño.]

Hevner Thesis 8 (L3170–3190):

«The Term 'Design Theory' Should Be Used Only When It Is Based on a Sound Kernel Theory.»

Traducción propia: [El término «Teoría de Diseño» debe utilizarse solo cuando esté basado en una teoría kernel sólida.]

Rodríguez cumple la función de kernel de proceso. Las tres formulaciones performativas gobiernan el proceso.

Estatuto lakatosiano: Rodríguez constituye núcleo firme del Programa (Fundacional §2). No es abandonable. Es fundamento.

§5.2 — XNOR como kernel de producto

PODERES/CONTABLE/xnor.py declara:

«XNOR contable — fuente única del axioma de cargo/abono.

Tres representaciones equivalentes de la misma regla estructural:

1. Booleana : tabla cerrada de 4 combinaciones
2. GF(2)    : 1 ⊕ n ⊕ m  (1 → DEBE, 0 → HABER)
3. Signos   : χ(n) · χ(m)  (+1 → DEBE, −1 → HABER)

[...] Ninguna de las tres reemplaza a las otras: son tres vistas del mismo invariante. La coincidencia entre ellas se verifica por test.»

Funciones: ubicacion_booleana, ubicacion_gf2, ubicacion_signos. Alias canónico: calcular_ubicacion = ubicacion_booleana.

XNOR cumple la función de kernel de producto porque gobierna un requisito estructural del núcleo contable del artefacto.

Estatuto lakatosiano: XNOR es cinturón protector. Es ajustable sin abandonar el Programa.

§5.3 — Articulación de los dos kernels

Los dos kernels no son equivalentes ni intercambiables.

| Elemento | Función | Estatuto lakatosiano |
|---|---|---|
| Rodríguez | Kernel de proceso | Núcleo firme |
| XNOR | Kernel de producto | Cinturón protector |

Relación: Rodríguez rige cómo se diseña. XNOR rige un núcleo estructural de lo diseñado.

§5.4 — Estado de D-02

La deuda D-02 (pluralidad de núcleos) queda resuelta dentro del diseño mediante la diferenciación de dos funciones kernel.

Esta resolución es interna. No constituye afirmación universal sobre todas las teorías de diseño ni sobre todos los sistemas contables. No declara demostrada una teoría de diseño completa.

---

PARTE 2 — ARTEFACTO Y MATERIALIZACIÓN

§6 — Artefacto

§6.1 — Estatuto del artefacto

El artefacto objeto de este diseño es una materialización del Programa de Investigación SCFV orientada a explorar, representar y evaluar secuencias de movimientos contables como trayectorias observables de estado.

Comprende conjuntamente:

- Constructos para representar estados y secuencias.
- Modelos para organizar las representaciones.
- Métodos para examinarlas.
- Instanciaciones materiales verificables.

§6.2 — Objeto de materialización

Cinco componentes de diseño:

1. Tablero de estados observables.
2. Modelo de secuencia de movimientos.
3. Mecanismo de evaluación de trayectorias.
4. Operacionalización de la exigencia de materialización (Fundacional §2.2).
5. Representación relacional del PCU.

Estos componentes no son propiedades previamente demostradas de SCFV. Son objetos de diseño a construir, examinar y eventualmente modificar.

§6.3 — Relación con S0

S0 es antecedente material del Programa. El diseño no atribuye retrospectivamente al S0 una arquitectura no declarada.

La interpretación del S0 como núcleo contable verificable pertenece al diseño actual y no constituye nueva declaración retrospectiva de su arquitectura original.

El SCFV_DSR es materialización del Programa, no derivado del S0.

§6.4 — Fractalidad acotada del artefacto

Conforme a §1.2. El SCFV_DSR ensayará si determinados invariantes se preservan bajo las transformaciones que materialice. No se declara que el SCFV_DSR sea fractal acotado. Es hipótesis a evaluar.

§7 — Usuarios y contexto de uso

§7.1 — Usuarios como interpretación del Fundacional §4

El Fundacional §4 declara que quien investiga no es neutral, participa con historia, lenguaje, conocimientos, expectativas, intereses, herramientas, limitaciones, interpretaciones y decisiones.

Los usuarios del artefacto se determinan a partir de esa interpretación:

- CPC (Contador Público Certificado) — conductor principal.
- Arquitecto — configura estructura.
- Programador — extiende motor.
- Auditores — inspeccionan trayectoria.
- Entes interesados — externos.

Esta identificación no constituye afirmación empírica. Es decisión de diseño derivada del contexto del Fundacional.

§7.2 — Uso previsto

El artefacto se diseña para permitir que un usuario pueda:

- Observar una sucesión de estados.
- Identificar los movimientos que producen transiciones.
- Representar la sucesión explícitamente.
- Formular propiedades de evaluación.
- Examinar la trayectoria frente a esas condiciones.
- Documentar los resultados.
- Confrontar los resultados mediante evidencia reproducible.

Pregunta operacional del diseño:

«¿Qué puede determinarse sobre una trayectoria a partir de sus estados, movimientos, relaciones y evidencias disponibles, sin convertir la inferencia de intención en condición necesaria de la verificación?»

§8 — Ciclos de Design Science Research

§8.1 — Relevance cycle

Hevner L1582:

«The Relevance Cycle bridges the contextual environment of the research project with the design science activities.»

Traducción propia: [El Ciclo de Relevancia conecta el entorno contextual del proyecto de investigación con las actividades de ciencia del diseño.]

En el Giro, la relevancia surge de la indeterminación identificada en el planteamiento. El diseño responde construyendo artefactos capaces de hacer observable y evaluable aquello que actualmente es pregunta de investigación.

§8.2 — Rigor cycle

Nota de estatuto: el pipeline perceptum → intellectus → dictum se declara como interpretación del diseñador sobre la arquitectura de S0. No es estructura declarada explícitamente por S0. El orquestador que integra las tres clases vive en PODERES/PROFESIONAL/interfaces/cli/, no en PODERES/EPISTEMOLOGICO/.

Hevner L1615:

«The Rigor Cycle connects the design science activities with the knowledge base of scientific foundations, experience, and expertise that informs the research project.»

El rigor cycle se ancla en la ruta canónica v8.2 de SCFV Motor 9.0.0, conforme a migracion_v82.md:

orquestador_v82 → H1 → H2 → autorización → consecuencia → MotorContable → ASIENTO_REGISTRADO

No se ancla en la ruta legacy (deprecada).

El rigor cycle se ancla en:

- (a) Invariantes verificados del Programa: I2, I13, I6, XNOR tres caras, hash chain EventStore.
- (b) Los 229 tests recogidos de S0: 225 pasan, 3 fallan por ausencia de datos externos (normas/, perfiles/) — deuda técnica del Release que el design cycle declara reconstruir —, 1 pospuesto por vaciedad (test_E12_universo_cerrado) — reconsiderado en el design cycle.
- (c) maquina_estados_asiento.py con sus 7 estados: PROPUESTO → EVALUADO → ADMITIDO/MODIFICADO/RECHAZADO → ASENTADO → ANULADO.
- (d) DECISION_H2 persistido antes del asiento (precedente de trayectoria).
- (e) Estado del Arte 2.0, declarado como documento previsto del Release S0.

No se declara «suite OK». Se declara el estado real.

§8.3 — Design cycle

Hevner L1650:

«The internal design cycle is the heart of any design science research project. This cycle of research activities iterates more rapidly between the construction of an artifact, its evaluation, and subsequent feedback to refine the design further.»

Traducción propia: [El ciclo interno de diseño es el corazón de todo proyecto de investigación en ciencia del diseño. Este ciclo itera entre construcción, evaluación y retroalimentación para refinar el diseño.]

Secuencia prevista: construcción → evaluación → retroalimentación → modificación → nueva evaluación.

El artefacto no se considera validado por el solo hecho de haber sido construido.

§8.4 — Integración

| Ciclo | Función en el Giro 04 |
|---|---|
| Relevancia | Conecta la indeterminación del planteamiento con el problema de diseño |
| Rigor | Conecta el diseño con fundamentos, conocimiento disponible y evidencia |
| Diseño | Construye, evalúa y modifica iterativamente el artefacto |

La articulación no convierte los ciclos en secuencia estrictamente lineal. La evaluación puede producir nueva información relevante.

§9 — Salidas

§9.1 — Cuatro outputs

Hevner L9054:

«March and Smith (1995) identify four possible design outputs: constructs, models, methods, and instantiations.»

Traducción propia: [March y Smith (1995) identifican cuatro posibles productos de diseño: constructos, modelos, métodos e instanciaciones.]

1. Constructs.
2. Models.
3. Methods.
4. Instantiations.

§9.2 — Salida primaria

Una materialización verificable de la posibilidad de representar y evaluar trayectorias contables.

El resultado puede ser positivo, parcial o negativo. Una materialización que demuestre un límite también constituye resultado de investigación.

§9.3 — Trazabilidad

Organización propuesta por el diseño (no categoría de Hevner):

problema → constructo → modelo → método → instanciación → evaluación → evidencia → resultado

§10 — Criterios de evaluación DSR

Guidelines de Hevner L1340–1362.

§10.1 — Diseño como artefacto. Debe existir materialización identificable (constructo, modelo, método o instanciación). Descripción puramente discursiva no es suficiente.

§10.2 — Relevancia del problema. El artefacto debe responder a la indeterminación establecida en el planteamiento.

§10.3 — Evaluación del diseño. La utilidad, calidad o eficacia no se presume. Debe existir procedimiento de evaluación + evidencia.

§10.4 — Contribución de investigación. El diseño debe permitir identificar qué conocimiento nuevo aporta. La contribución deberá distinguirse de la mera aplicación de conocimiento previamente disponible.

§10.5 — Rigor de investigación. Trazabilidad respecto de fundamentos, métodos y evidencias. El rigor no se reduce a existencia de código o pruebas.

§10.6 — Diseño como proceso de búsqueda. La solución no se considera conocida antes del proceso. Hevner L1340–1362 (Guideline 6).

§10.7 — Comunicación. Los resultados deben poder comunicarse tanto a especialistas del dominio contable como a quienes examinan fundamentos y materializaciones técnicas.

§11 — Componentes del artefacto

§11.1 — Tablero de estados observables

Representación espacial o estructurada de los estados que pueden observarse en una trayectoria.

Nota de estatuto (T2): el término «tablero» se adopta como denominación funcional del componente del artefacto. En 01_idea.md §8 el término aparecía como recurso heurístico (analogía del tablero). En el presente diseño el término pasa de analogía a componente operativo. Esta transformación de estatuto se declara expresamente. No se invoca la analogía del ajedrez ni ninguna otra analogía del Operador como fundamento.

§11.2 — Modelo de secuencia. Representa estado → movimiento → estado siguiente. Distingue estado previo, movimiento, estado resultante, evidencia asociada y condiciones de evaluación.

§11.3 — Evaluación de trayectorias. Método de examen. Objeto: propiedades observables de la sucesión. No inferir intención.

§11.4 — §2.2 operacionalizado. Producción de objetos susceptibles de ejercicio, confrontación, apropiación, demostración o examen.

§11.5 — PCU relacional. Representación que hace explícitas las relaciones necesarias para examinar una trayectoria.

§11.6 — Cadena funcional. Organización propuesta por el diseño: tablero → secuencia → trayectoria → evaluación → demostración. No es declaración retrospectiva de arquitectura existente en S0.

§11.7 — Reuso de componentes S0.

- xnor.py (kernel de producto).
- motor_contable/motor.py (invariantes I2, I13, I6).
- event_store/event_store.py (hash chain).
- maquina_estados_asiento.py (7 estados).
- decision_provider.py (adaptador de DECISION_H2).
- nucleo_consecuencias.py.
- Los 225 tests que pasan.

§11.8 — Componentes a reconstruir por el design cycle.

- normas/, perfiles/, DOMINIOS/.
- Fractales históricos (Ventas, Compras, Inventario, Fiscal).
- Los 3 tests fallidos (test_schema_validator, test_and_condition, test_carga_normas_validas).
- El skip test_E12_universo_cerrado.

§12 — Fractalidad acotada y materialización de segundo orden

§12.1 — Definición operativa. FRACTALIDAD_ACOTADA.md L142–143. Preservación mediante representación suficiente, no identidad.

§12.2 — Precedente histórico. S0 materializó fractales de dominio. Fueron eliminados del Release. Precedente histórico del Programa.

§12.3 — Estatuto en el SCFV_DSR. Hipótesis a ensayar por el design cycle. No propiedad declarada.

§12.4 — Acotación. Cualquier afirmación sobre preservación de invariantes queda limitada al dominio de materializaciones y transformaciones efectivamente ensayadas.

§12.5 — Estatuto del teorema. Si el SCFV_DSR sostiene la fractalidad acotada en sus ensayos, refuerza la conjetura de FRACTALIDAD_ACOTADA.md §3. No la eleva a teorema.

La elevación a teorema requiere acto matemático formal separado, con las cuatro condiciones de FRACTALIDAD_ACOTADA.md §7 cumplidas:

1. Extensión a NIIF completas.
2. Transformaciones no ensayadas.
3. Invariantes no lineales.
4. Validación cruzada completa.

DSR produce artefactos, no teoremas.

§13 — Hipótesis emergentes

§13.1 — Estatuto. Las dos hipótesis (H-EMG-1, H-EMG-2) pertenecen al dominio DSR. No son hipótesis causal del estudio sampieriano. Se generan en el design cycle.

§13.2 — H-EMG-1: reensamblaje de fractales históricos. Los fractales de S0 eliminados del Release podrían reensamblarse sobre el Motor. Falseable en el design cycle.

§13.3 — H-EMG-2: reutilización como motor contable. El SCFV_DSR podría operar como motor contable reutilizable en sistemas que trabajen con partida doble. Falseable en el design cycle.

§13.4 — Relación con Hevner. El design cycle itera build-evaluate (L1650). Hevner L1479: «Reliance on creativity and trial and error search are characteristic of such research efforts.» Las hipótesis emergen de esta iteración.

§13.5 — Criterio de cierre de Parte 2. Artefacto identificable + forma explícita de evaluación + evidencia + trazabilidad. La existencia de estos elementos no implica que el artefacto haya superado la falsación.

§14 — Aporías habitadas y su operacionalización

§14.1 — Las aporías como condiciones operativas

El diseño del SCFV_DSR opera en presencia de aporías derivadas de la problematización registrada en ACTA_RESPUESTA_CALDERON_2026-09-19.md. Las aporías no se exponen aquí como crítica, sino como condiciones operativas que el artefacto habita.

- A-1 — Soberanía de H2. El sistema no sustituye la decisión del contador.
- A-1a — Error. El sistema distingue error de dolo sin inferir intención.
- A-1b — Dolo por acción. El sistema puede leer la celada como secuencia legal. No la explica.
- A-1c — Dolo por omisión. El sistema modela lo que falta. No infiere dolo por la ausencia.
- A-2a — Herramienta. El SCFV_DSR es la herramienta. Se distingue de su uso.
- A-2b — Uso. El sistema no controla el uso. Solo habilita la lectura.

Estatuto del Acta referenciada: ACTA_RESPUESTA_CALDERON_2026-09-19.md está materializada en ~/Programa-de-Investigacion-SCFV/ACTAS/. Su estatuto es el de acta registrada del Giro 03. El presente diseño la referencia sin reproducirla.

§14.2 — Resolución a nivel de objeto vs sujeto

Las aporías no se resuelven a nivel de objeto. El objeto contable no captura intención. No distingue error de dolo. No lee celada como estrategia.

Las aporías se resuelven a nivel de sujeto. El sistema no sustituye al sujeto. Habilita su juicio.

§14.3 — Operacionalización en el SCFV_DSR

| Componente | Aporía que habita |
|---|---|
| DECISION_H2 persistido antes del asiento | A-1 |
| Modelo de secuencia sin hipótesis causal | A-1a, A-1b |
| Tablero que lee lo que falta | A-1c |
| XNOR como invariante estructural | transversal |
| Máquina de estados (7 estados) | transversal |
| Ausencia de inferencia de intención | A-2a, A-2b |

§14.4 — Estatuto

El SCFV_DSR es la operacionalización del habitar. No cierra las aporías. Las habita materialmente.

La problematización externa como texto se reporta en el cierre de la investigación (Cap 15 y Cap 17 sampierianos). El diseño no expone la crítica. Expone las condiciones operativas que derivan de ella.

§14.5 — Lo que el diseño no declara

- No declara que el SCFV_DSR detecta dolo.
- No declara que el SCFV_DSR impide celadas.
- No declara que las aporías están resueltas.
- No declara que el sistema sustituye al contador.

§14.6 — Lo que el diseño sí declara

- El SCFV_DSR habilita la lectura de secuencias legales sin inferir intención.
- El SCFV_DSR preserva la soberanía del sujeto.
- El SCFV_DSR habita las aporías materialmente.
- La resolución es a nivel de sujeto, no de objeto.

---

PARTE 3 — CONGRUENCIA, DEUDAS, FALSACIÓN Y CIERRE

§15 — Relación con el planteamiento

§15.1 — Correspondencia fundamental. El diseño responde al problema de 02_planteamiento.md §3.

§15.2 — Pregunta de diseño. Reformulación funcional de la pregunta general de 02_planteamiento.md §8.

§15.3 — Relación con la sostenibilidad de la línea. El diseño no presupone continuidad de TRAYECTORIA_ESTADO. Entre los resultados posibles: sostenerse, requerir delimitación, requerir reformulación, encontrar límite, o no sostenerse.

§15.4 — Ausencia de hipótesis causal. Coherente con 02_planteamiento.md §18.

§15.5 — Respuesta al crítico. El diseño responde al problema del planteamiento y habita las aporías derivadas de la problematización registrada en ACTA_RESPUESTA_CALDERON_2026-09-19.md. Las aporías se abordan en §14. Su estatuto como problematización externa de la investigación se reporta en el cierre (Cap 15 y Cap 17 sampierianos).

§16 — Deudas

§16.1 — Divergencias consolidadas. Ver §21.

§16.2 — Estado del Arte 2.0. Declarado contractualmente como documento previsto del Release S0. No vigente.

§16.3 — Fundacional y separación Programa/S0. El Fundacional pertenece al Programa. No forma parte del Release S0 (Contrato §6, punto 7).

§16.4 — D-02 resuelta en §5.4.

§16.5 — D-08 (universalidad partida doble). Permanece abierta.

§16.6 — Reconstrucción en el design cycle.

| Raíz | Acción |
|---|---|
| normas/ | Reconstruir |
| perfiles/ | Reconstruir |
| DOMINIOS/ | Reconstruir |
| Fractales históricos | Reensamblar (H-EMG-1) |
| test_E12_universo_cerrado | Reconsiderar |
| 3 tests fallidos | Corregir al reconstruir |

§16.7 — Deudas residuales del Release S0. Los 3 tests fallidos y el skip quedan como trabajo a realizar por el SCFV_DSR.

§17 — Estatuto del diseño

§17.1 — Estatuto metodológico. DSR. Articulación: Sampieri organiza. Hevner estructura. Rodríguez rige proceso. XNOR rige núcleo.

§17.2 — Estatuto del artefacto. Condición de diseño. No validado por su formulación. Su estatuto depende de materializaciones y evaluaciones posteriores.

§17.3 — Estatuto de las propiedades. Seis categorías (propuesta del diseñador): propuesta / condición de diseño / propiedad evaluada / propiedad verificada / propiedad refutada / propiedad cuyo estatuto permanece no determinado.

§18 — Falsación del diseño

§18.1 — Principio. El diseño debe permanecer abierto a resultados que contradigan sus presupuestos operativos. La falsación no se limita a comprobar si el artefacto funciona conforme a la intención del diseñador. También permite descubrir insuficiencias, contradicciones, pérdida de invariantes, imposibilidad de evaluar propiedades, dependencia indebida de inferencias no observables y límites del dominio.

§18.2 — Condiciones de refutación. Propuesta del diseñador. Anclaje metodológico en Protocolo §3 (eje Falsación). La línea se considera comprometida cuando una evaluación reproducible muestra que:

1. El estado no puede representarse suficientemente.
2. La secuencia no conserva el orden necesario.
3. La trayectoria no puede reconstruirse.
4. La propiedad propuesta no puede evaluarse.
5. La evaluación depende necesariamente de inferir intención no observable.
6. Una transformación destruye una propiedad que se pretendía preservar.
7. La materialización no produce evidencia suficiente.

§18.3 — Falsación y modificación. Una falsación de un componente no implica rechazo de toda la línea. Puede producir: resultado → diagnóstico → modificación → nueva construcción.

§18.4 — Ausencia de garantía de éxito. El diseño no contiene garantía de que TRAYECTORIA_ESTADO sea materializable. Una imposibilidad demostrada bajo condiciones determinadas constituye resultado admisible.

§19 — Tres ejes del Protocolo

§19.1 — Falsación. Confronta afirmaciones del diseño con evidencia capaz de mostrar que no se cumplen bajo las condiciones declaradas. Pregunta: no solo «¿funciona?», sino «¿qué tendría que observarse para determinar que esta formulación no se sostiene?»

§19.2 — Deconstrucción. Examina oposiciones, supuestos y categorías incorporados: observable/inferido, estado/movimiento, representación/realidad, evidencia/interpretación, trayectoria/intención.

§19.3 — Horizonte Rodriguiano. Conforme a Protocolo §3 y Fundacional §2.1–§2.3. Orienta: fundamento, disciplina y operación; exigencia de materialización; apertura al error como fuente de nuevas preguntas.

§19.4 — IPVE como transversal. I — Invariantes. P — Propiedades. V — Validaciones. E — Evidencias. Remisión a 04_ipve_operacionalizado.md para la operacionalización.

Los cuatro adjetivos heredados de Rodríguez §2.2 (público, útil, apropiable, palpable), declarados en 04_ipve_operacionalizado.md §5 como exclusivos del Giro 04, permanecen vigentes.

§20 — Cierre

§20.1 — Cierre documental. La Parte 3 cierra la estructura del documento pero no declara validado el artefacto. Quedan establecidos: fundamento, objeto, artefacto, componentes, ciclos DSR, criterios de evaluación, relación con el planteamiento, deudas conocidas, condiciones de falsación, tres ejes.

§20.2 — Cierre investigativo. Posterior. Depende de materializaciones y evaluaciones efectivamente realizadas.

cierre documental ≠ validación del artefacto.
materialización ≠ demostración.
evaluación ≠ confirmación automática.

§20.3 — Resultado abierto. La línea TRAYECTORIA_ESTADO podrá producir: representación viable, viable bajo restricciones, que requiera reformulación, delimitación del problema, o evidencia suficiente para rechazar una formulación.

§20.4 — Estatuto final. Las formulaciones de este documento conservan el estatuto de diseño de investigación hasta que se produzcan las materializaciones y evaluaciones.

§20.5 — Estatuto del ciclo de falsación. Constancia final: IA-2. Decisión de materialización: Operador. La problematización externa se reporta en Cap 15/17 sampierianos.

---

§21 — CONSOLIDACIÓN DEL CICLO DE FALSACIÓN

§21.1 — Divergencias de Parte 1

- D1: reformulación funcional de O1–O8 — corregida en V3 (O1–O8 reproducidos literalmente).
- D2: separación objetivos DSR / ausencias — declarada en §2.2.
- D3: síntesis del redactor — declarada en §4.4.
- D4: comillas unificadas a «...».
- D5: xnor.py como fuente primaria de implementación.
- E-07: Sampieri en capítulos pertinentes (2–6). Estructuración del artefacto corresponde a DSR/Hevner.

§21.2 — Divergencias de Parte 2

- D1: SCFV_DSR como materialización del Programa, no derivado de S0.
- D2: 229 tests recogidos / 225 pasan / 3 fallan / 1 skip.
- D3: reuso de componentes S0 declarado (§11.7).
- D4: citas Hevner (Guideline 6, L1340–1362).
- H-04: pipeline se orquesta en CLI.
- H-05: main.py.BACKUP_D2 residuo declarado.
- E-09: cadena §9.3 declarada como organización del diseño.

§21.3 — Divergencias de Parte 3

- D2: reformulación funcional declarada (§15.2).
- D3: esquema de deudas consolidado (§16, §21).
- D4: categorías de propiedades declaradas propuesta del diseñador (§17.3).
- D5: condiciones de refutación declaradas propuesta del diseñador (§18.2).
- D6: cuatro adjetivos integrados (§19.4).
- D7: categorías de resultado declaradas propuesta del diseñador (§20.3).
- D8: remisión a 04_ipve_operacionalizado.md (§19.4).
- E-12: hipótesis emergentes remitidas a Parte 1 §3.3 y Parte 2 §13.
- E-13: Horizonte Rodriguiano anclado en Protocolo §3 y Fundacional §2.1–§2.3.

§21.4 — Correcciones adicionales integradas en V3

- T1: elevación de estatuto de las cuatro ausencias declarada (§2.2).
- T2: transformación de estatuto del término «tablero» declarada (§11.1).
- D-V2-1: O1–O8 reproducidos literalmente (§2.1).
- D-V2-2: pipeline declarado como interpretación del diseñador (§8.2).
- D-V2-3: «descompone» en lugar de «puede descomponer» (§4.5).
- E-V2-1: V3 sustituye V2 en encabezado.
- E-V2-2: §2.1 declara reproducción literal.
- E-V2-3: §14.1 declara estatuto del Acta.

§21.5 — Deudas consolidadas

Cerradas: D-02, D-05, D-11 a D-16.

Abiertas:

- D-01: NIIF diferida a Giro 4+.
- D-03: Merlin no materializado.
- D-04: usuarios como interpretaciones.
- D-06: validación cruzada de fractalidad pendiente.
- D-07: reutilización como hipótesis declarada.
- D-08: universalidad partida doble abierta.
- D-09: HL-46 cerrado con nota de error.
- D-10: Romney raw parcial.

§21.6 — Regla de trazabilidad. Ninguna divergencia del ciclo se considera desaparecida por consolidación.

---

§22 — FIRMAS

El presente documento cierra el ciclo de falsación bilateral sobre 06_diseno.md.

Autoría y verificación:

- IA-1 (constructor): redacción de Partes 1, 2 y 3. Constancia. Fecha: 2026-09-21
- IA-2 (falsador): falsación bilateral por bloques + verificación contra Termux. Constancia. Fecha: 2026-09-21
- Operador (autoridad): decisión de materialización. Firma. Fecha: 2026-09-21

Estatuto final del documento: DISENO — V3 · CERRADO EN FALSACIÓN.

El ciclo §19.2 correspondiente a este acto queda cerrado técnicamente. El cierre formal corresponde al Operador.

FIN DEL DOCUMENTO — 06_diseno.md V3

---

VIGENCIA

Documento firmado y vigente desde 2026-09-21.
Acta de firma: ACTAS/ACTA_FIRMA_06_diseno_2026-09-21.md
Estado: DISENO — V3 · VIGENTE.

# ACTO 09 — CONSTRUCCIÓN Y EVALUACIÓN INICIAL DE U-SEQ-01

**Giro:** 04
**Sesión:** 4
**Design Cycle:** primer acto evaluativo
**Documento:** "GIRO_04/09_evaluacion_useq_01.md"
**Versión:** D
**Objeto:** U-SEQ-01
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Autoría:** IA-1 — constructor
**Falsación:** IA-2 — APTO SIN OBJECIONES
**Autoridad:** Operador

---

## §1. Antecedente y especificación vigente

El Acto 08 materializó U-SEQ-01.

La "ACTA_ENMIENDA_USEQ_01_GIRO_04", Versión E, materializó posteriormente las correcciones C-1 a C-4 y desplazó parcialmente los §§8.1, 8.2, 8.3, 8.5 y 13 del Acto 08.

Por tanto, la Enmienda U-SEQ-01, Versión E, constituye la especificación vigente para este Acto 09 en las materias que desplazó del Acto 08.

El Acto 08 continúa siendo antecedente documental en las materias no desplazadas.

El Acto 09 no modifica ninguno de los dos actos materializados.

---

## §2. Pregunta de diseño

¿Puede una instancia de U-SEQ-01 construirse y evaluarse sobre un segmento efectivamente persistido del corpus, representando una transición contable observable y verificable, sin introducir datos inexistentes y conservando las condiciones I-1 a I-4 en la medida previamente definida como evaluable?

La expresión "en la medida evaluable" queda operacionalizada por los criterios §§10–20 y no será determinada después de conocer los resultados.

---

## §3. Distinciones operativas

La evaluación distinguirá:

### §3.1 Disponible

Información que:

1. existe materialmente en una fuente persistida;
2. puede recuperarse mediante el procedimiento declarado;
3. corresponde al objeto evaluado.

### §3.2 No persistido

Información perteneciente al modelo o proceso conceptual que no está almacenada en la fuente persistida evaluada.

### §3.3 No disponible

Información que no puede recuperarse de las fuentes declaradas para la instancia.

### §3.4 Relación demostrada

Relación respaldada por identificadores o estructuras persistidas cuya correspondencia pueda verificarse directamente.

### §3.5 Relación no demostrada

Relación que podría ser conceptualmente plausible, pero para la cual el corpus no contiene evidencia suficiente para establecerla.

Ninguna relación será inferida por semejanza semántica, proximidad temporal o coincidencia parcial.

---

## §4. Base de trabajo declarada

La base de trabajo de esta instancia será:

"~/scfv_v6/scfv.db"

Razón de selección declarada antes de la observación de resultados:

«Entre las bases locales candidatas previamente identificadas que contienen eventos "ASIENTO_REGISTRADO", se selecciona la que contiene el mayor número de dichos eventos persistidos al momento del pre-registro, sin utilizar para la selección ningún resultado de la evaluación I-1–I-4.»

Estado conocido previamente:

- "scfv.db": 10 "ASIENTO_REGISTRADO";
- "INFRAESTRUCTURA/db/scfv.db": 4 "ASIENTO_REGISTRADO";
- "scfv_h6_5.db": 0 "ASIENTO_REGISTRADO".

La selección no se fundamenta en presencia o ausencia de H2.

La base "scfv.db" queda fijada como corpus de trabajo de este Acto 09, salvo imposibilidad técnica materialmente demostrada conforme al §4-ter.

---

## §4-bis. Criterio previo de selección del corpus

El criterio de selección queda fijado antes de observar el contenido evaluativo de la instancia:

1. la base debe contener al menos un "ASIENTO_REGISTRADO";
2. debe pertenecer al entorno local de trabajo declarado;
3. debe ser recuperable por el procedimiento de lectura de U-SEQ-01;
4. entre las bases que cumplan 1–3 se seleccionará la de mayor número de "ASIENTO_REGISTRADO";
5. los resultados I-1–I-4, H2, contexto o trazabilidad no podrán utilizarse para modificar la selección.

Si existe empate, se aplicará como desempate el orden lexical del path completo.

El criterio queda fijado independientemente del resultado esperado.

---

## §4-ter. Imposibilidad técnica

Se considerará imposibilidad técnica materialmente demostrada únicamente cuando, antes de la observación evaluativa, ocurra al menos una de estas condiciones:

1. el archivo de base no puede abrirse como base SQLite válida;
2. la tabla "event_store" no existe o no puede consultarse;
3. la estructura necesaria para recuperar "ASIENTO_REGISTRADO" no puede leerse;
4. el archivo no puede ser leído por permisos del entorno de ejecución y el Operador no dispone de autorización para corregirlos;
5. la lectura produce un error reproducible que impide recuperar el corpus.

La imposibilidad deberá registrarse con:

- comando o procedimiento ejecutado;
- salida o error obtenido;
- identificación de la base;
- fecha/hora;
- evidencia preservada.

Un resultado desfavorable de I-1–I-4 no constituye imposibilidad técnica.

---

## §5. Condición de construcción

La construcción respetará la especificación vigente de U-SEQ-01.

No se construirá un segundo Motor Contable.

No se modificará el Motor Contable v8.2.

No se inventará:

- "contexto_contable";
- "evidencia_hash";
- "cuenta_codigo";
- "state_id" persistido inexistente;
- relación H2→asiento no demostrada.

Los identificadores derivados deberán distinguirse de los identificadores originalmente persistidos.

---

## §6. Número de instancias

El Acto 09 evaluará una instancia elemental de U-SEQ-01.

La instancia será un "ASIENTO_REGISTRADO" seleccionado mediante el procedimiento definido en §7, después del pre-registro y antes de ejecutar la evaluación de sus propiedades.

No se evaluarán las 10 instancias por defecto.

La ampliación a múltiples instancias será un acto posterior si la evidencia obtenida lo justifica.

La elección de una sola instancia no podrá depender de su resultado.

---

## §7. Selección de la instancia

La instancia se seleccionará después del pre-registro, pero antes de ejecutar la evaluación.

Procedimiento:

1. recuperar los "ASIENTO_REGISTRADO" de la base fijada;
2. ordenar por "event_store.id" ascendente;
3. seleccionar el primer "ASIENTO_REGISTRADO" que cumpla las condiciones mínimas de recuperabilidad de payload;
4. fijar su "event_store.id" como "k_evento";
5. no excluir una instancia por presentar ausencia de H2, contexto o evidencia.

### §7-bis. Caso de primer evento

Si el evento seleccionado es el primer "ASIENTO_REGISTRADO" del corpus:

- "k_inicial = k_evento";
- no existe "k_t" anterior;
- el estado previo se define como el estado del corte inicial del corpus, sin eventos "ASIENTO_REGISTRADO" anteriores al movimiento;
- ese estado previo se representa como una posición contable vacía "{}".

Por tanto, I-1 no será declarado NO EVALUABLE por el mero hecho de tratarse del primer evento.

La evaluación verificará si la transición desde "{}" hacia el estado resultante puede determinarse conforme a I-3.

Si la estructura real del corpus impide materializar la representación "{}", la imposibilidad se registrará como resultado de evaluación y no se resolverá mediante datos inventados.

---

## §8. Instancia de transición

La instancia contendrá, cuando estén disponibles:

- estado previo;
- movimiento contable observado;
- estado resultante;
- cuentas afectadas;
- importes Debe;
- importes Haber;
- evidencia estructurada;
- "correlation_id";
- "event_store.id";
- "idempotency_key";
- "asiento.id";
- referencias H2 disponibles;
- contexto persistido efectivamente vinculado, si existe.

La ausencia de cualquiera de estos elementos será registrada como ausencia, no completada mediante inferencia.

---

## §9. Lectura y observación

La observación utilizará la estructura definida por U-SEQ-01:

- "event_store.id" para orden;
- "idempotency_key" para identidad del evento;
- "correlation_id" para identidad del movimiento;
- payload deserializado para recuperar el asiento.

La información contextual externa al EventStore sólo podrá utilizarse cuando su fuente y relación con el movimiento estén materialmente demostradas.

---

## §10. Identidad de estados — I-1

I-1 se evaluará verificando que el estado previo y el estado resultante puedan diferenciarse como posiciones contables observables dentro del rango declarado.

Se considerará:

- conjunto de cuentas afectadas;
- saldos correspondientes;
- movimiento que produce la transición;
- límite temporal del corpus.

Resultado posible:

- PASA
- FALLA
- INCONCLUSO
- NO DISPONIBLE

La categoría será determinada mediante la evidencia efectivamente recuperada, no por decisión posterior orientada al resultado.

---

## §11. Conservación de partida doble — I-2

I-2 se evaluará sobre el asiento correspondiente al movimiento seleccionado.

Condición:

    |ΣDebe − ΣHaber| ≤ 0.001

La tolerancia se alinea con el comportamiento declarado del Motor Contable v8.2.

La determinación de Debe/Haber se realizará mediante la representación XNOR de la combinación "naturaleza" + "movimiento" de cada partida, conforme a la regla contable declarada por el Motor.

Los campos reales utilizados serán:

- "partidas[*].cuenta";
- "partidas[*].naturaleza";
- "partidas[*].movimiento";
- "partidas[*].monto";
- "total_debe";
- "total_haber".

Los valores "total_debe" y "total_haber" persistidos serán utilizados como control directo del asiento.

La derivación por XNOR y los totales persistidos deberán ser coherentes.

No se utilizará "cuenta_codigo".

---

## §12. Determinabilidad de transición — I-3

I-3 se evaluará conforme a:

1. Motor Contable v8.2;
2. regla de partida doble/XNOR correspondiente;
3. datos efectivamente persistidos;
4. rango canónico declarado.

La pregunta será si el estado resultante puede determinarse a partir de los datos y reglas efectivamente disponibles.

No se aceptará como determinabilidad una reconstrucción basada en información no persistida.

---

## §13. Trazabilidad — I-4

I-4 se evaluará por relaciones individuales:

- H2 → movimiento;
- movimiento → asiento;
- asiento → evento;
- evento → evidencia;
- evento → estado;
- contexto persistido → movimiento, cuando exista fuente y vínculo demostrables.

Cada relación recibirá uno de los estados definidos en §17.

La existencia aislada de un identificador no demuestra la relación.

---

## §14. Estado de H2

La evaluación utilizará los estados definidos por la Enmienda U-SEQ-01:

### H2-A — Ausente

No existe un registro "DECISION_H2" recuperable que pueda vincularse materialmente con la instancia.

Resultado específico H2→asiento:

INCONCLUSO respecto de la relación.

No equivale a afirmar que no existió una decisión profesional.

### H2-B — Presente sin vínculo demostrable

Existe un registro "DECISION_H2", pero no existe correspondencia demostrable con el movimiento evaluado.

Resultado:

FALLA del vínculo específico H2→asiento.

### H2-C — Presente y vinculado

Existe un registro H2 cuya relación con el movimiento evaluado puede demostrarse mediante identificadores persistidos.

Resultado:

PASA el vínculo específico, sujeto a la evaluación del resto de la cadena.

---

## §15. Evidencia

La evidencia será tratada como estructura persistida.

No se utilizará "evidencia_hash" si el hash no está efectivamente almacenado.

Para la instancia seleccionada se verificarán directamente los campos existentes.

En los asientos previamente examinados se observaron estructuras como:

- factura;
- RIF;
- monto;
- fecha;
- tipo;
- producto;
- cantidad;
- costo unitario.

El Acto 09 no generalizará esos campos a la instancia hasta verificarlos directamente.

---

## §16. Contexto

La Enmienda U-SEQ-01 estableció que los cuatro campos del modelo Python "ContextoContable" no están persistidos en el corpus evaluado.

Por tanto se distinguirá:

### §16.1 ContextoContable formal

Los campos formales del modelo Python no serán considerados persistidos en el corpus salvo que una fuente material posterior demuestre lo contrario.

### §16.2 "contexto.json"

"contexto.json" constituye una fuente distinta, con bloques persistidos propios.

Su existencia no demuestra por sí misma que un asiento haya utilizado esos valores.

Sólo será evaluable una relación:

"contexto.json → movimiento"

si existe evidencia persistida que permita demostrarla.

### §16.3 Ausencia

Cuando ninguna fuente declarada permita demostrar el contexto utilizado por el movimiento:

NO DISPONIBLE / NO EVALUABLE COMO RELACIÓN CONTEXTUAL.

No se convertirá la ausencia en inferencia.

---

## §17. Procedimiento de determinación de relaciones

Cada relación se determinará mediante esta secuencia:

1. identificar los extremos de la relación;
2. recuperar sus identificadores o estructuras persistidas;
3. buscar una correspondencia explícita;
4. verificar que la correspondencia pertenece a la instancia evaluada;
5. registrar la evidencia material;
6. asignar resultado.

Resultados:

| Resultado | Significado |
|---|---|
| PASA | relación demostrada |
| FALLA | relación requerida examinada y contradicha o ausente donde debía existir |
| INCONCLUSO | la evidencia disponible no permite determinarla |
| NO DISPONIBLE | el extremo o fuente requerida no está disponible en el corpus declarado |

Correspondencia con la Enmienda E:

- PASA = PASS.
- FALLA = FAIL.
- INCONCLUSO = INCONCLUSO.
- NO DISPONIBLE es una categoría adicional introducida por este acto para distinguir ausencia de fuente de insuficiencia probatoria.

---

## §18. Representación y reproducibilidad

La representación producida por U-SEQ-01 será comparada mediante la función "serializar(...)" de:

"PODERES/INFRAESTRUCTURA/serializador_canonico.py"

Dos ejecuciones sobre el mismo corpus persistido, mismos límites, mismas reglas y mismos datos de entrada serán consideradas equivalentes cuando:

    serializar(representación_1) == serializar(representación_2)

La igualdad será estructural y exacta sobre la representación serializada.

No se utilizará el hash como sustituto de la definición de igualdad.

---

## §19. Identificadores y reproducibilidad

Se distinguen:

| Identificador | Función |
|---|---|
| "event_store.id" | orden temporal canónico |
| "idempotency_key" | identidad persistida del evento |
| "correlation_id" | identidad del movimiento |
| "asiento.id" | identidad del asiento |
| "decision_id" | identidad de H2 |
| "propuesta_h1_id" | referencia potencial H1 |
| "propuesta_h2_id" | referencia potencial H2 |

Tanto "asiento.id" como "idempotency_key" pueden cambiar entre ejecuciones nuevas del Motor porque el primero utiliza "uuid4()" y el segundo deriva de ese identificador.

Por ello la reproducibilidad de este acto se limita al corpus persistido.

---

## §20. Rango temporal

El rango canónico utilizará:

- "k_inicial": primer "ASIENTO_REGISTRADO" del corpus completo evaluado;
- "k_t": "event_store.id" del "ASIENTO_REGISTRADO" inmediatamente anterior al evento evaluado, si existe;
- "k_evento": "event_store.id" del asiento evaluado;
- límite resultante: "k_evento".

Para el primer evento:

- "k_t" no existe;
- "k_inicial = k_evento";
- el estado previo es "{}".

No se seleccionará el rango después de observar el resultado.

---

## §20-bis. Pre-registro de corpus e instancia

Antes de ejecutar la observación de la instancia se producirá un registro de pre-registro que contendrá:

1. fecha y hora;
2. base de trabajo;
3. criterio de selección;
4. "k_inicial", si ya puede determinarse sin observar resultados;
5. criterio de selección de instancia;
6. versión de U-SEQ-01;
7. versión del Motor Contable;
8. pregunta de evaluación;
9. propiedades I-1–I-4;
10. criterio de comparación de representaciones;
11. previsión de que la base seleccionada contiene 10 "ASIENTO_REGISTRADO" y 0 "DECISION_H2", si dicha condición es confirmada antes del pre-registro;
12. declaración de que, bajo esa condición, H2-A constituye un resultado esperado por composición del corpus y no una conclusión sobre U-SEQ-01.

El pre-registro deberá quedar en un archivo independiente antes de la observación evaluativa.

Su integridad se documentará mediante:

1. cuerpo del pre-registro;
2. hash SHA-256;
3. firma o constancia del Operador;
4. fecha/hora de materialización.

En este Acto 09, la constancia del Operador es obligatoria porque el pre-registro fija formalmente el corpus, la instancia y las condiciones anteriores a la observación.

La observación evaluativa no podrá ejecutarse antes de que el pre-registro esté materializado.

---

## §21. Control positivo

El control positivo consistirá en una instancia que cumpla las condiciones mínimas para evaluar al menos I-1, I-2 e I-3.

Su selección estará sometida al mismo pre-registro de §20-bis.

El control positivo podrá ser:

- la misma instancia principal, si cumple las condiciones;
- una segunda instancia, si la principal no las cumple y el procedimiento de selección permite elegirla sin observar resultados;
- no disponible, si ninguna instancia del corpus satisface las condiciones mínimas.

Si no existe control positivo, el ciclo de evaluación no se considerará evaluativamente cerrado.

El resultado del acto será:

INCONCLUSO POR AUSENCIA DE CONTROL POSITIVO

y sólo podrá continuarse mediante un nuevo acto que:

1. declare el nuevo corpus, o
2. declare un criterio previo de ampliación del corpus.

No se repetirá la selección simplemente hasta obtener un resultado favorable.

---

## §22. Evidencia negativa

La ausencia de un campo o relación será registrada mediante:

1. consulta reproducible;
2. resultado obtenido;
3. identificación de la fuente examinada;
4. cantidad de ocurrencias, cuando corresponda;
5. cita o transcripción mínima del resultado material;
6. hash o integridad del registro de ejecución cuando sea materialmente necesario.

La ausencia no se transformará en explicación causal.

Ejemplo:

"justificacion_h2 = null"

se registra como ausencia observada.

No permite inferir ausencia de decisión profesional fuera del registro examinado.

---

## §23. Falsadores del Acto 09

La instancia será falsable.

Entre las condiciones de refutación:

1. imposibilidad de distinguir estado previo y resultante;
2. violación de "|ΣDebe − ΣHaber| ≤ 0.001";
3. imposibilidad de determinar el resultado con las reglas declaradas;
4. imposibilidad de recuperar los identificadores necesarios;
5. inconsistencia interna de la representación;
6. necesidad de introducir datos no persistidos;
7. dependencia de inferencias sobre intención subjetiva;
8. selección del rango condicionada por el resultado;
9. pérdida de trazabilidad material en una relación declarada evaluable.

Una falla de la instancia no refuta automáticamente todo SCFV_DSR.

---

## §24. Hevner — condiciones previas de evaluación

Antes de evaluar el resultado deberán quedar declarados:

1. Objeto: instancia de U-SEQ-01;
2. Problema: representación y evaluación de una transición contable observable;
3. Aspecto de construcción/evaluación: preservación y verificabilidad de I-1–I-4;
4. Criterios: §§10–20;
5. Evidencia prevista: corpus persistido, payload, identificadores, rango y representación canónica.

Los elementos 6–10 sólo podrán completarse después de producir la evidencia.

---

## §25. Hevner — evaluación posterior

Después de producir evidencia se registrarán:

6. diseño como artefacto;
7. relevancia del problema;
8. resultados de evaluación;
9. contribución observada;
10. comunicación, cuando corresponda.

No se declarará resultado Hevner antes de disponer de evidencia.

---

## §26. Relación con H-EMG-1

El Acto 09 no demuestra H-EMG-1.

Produce evidencia local sobre la capacidad de U-SEQ-01 para representar y evaluar una transición.

La evidencia podrá alimentar posteriormente la evaluación de H-EMG-1.

No se confundirá evidencia local con confirmación de la hipótesis global.

---

## §27. Relación con H-EMG-2

El Acto 09 tampoco demuestra H-EMG-2.

No se probará mediante este acto que SCFV_DSR sea un motor contable reutilizable.

Esa hipótesis requiere evaluación propia conforme a sus condiciones de falsación.

---

## §28. Registro de resultados

El registro de resultados se producirá durante la ejecución del Acto 09 y contendrá:

1. corpus utilizado;
2. base de datos;
3. rango;
4. evento evaluado;
5. datos recuperados;
6. representación construida;
7. I-1;
8. I-2;
9. I-3;
10. I-4;
11. reproducibilidad;
12. evidencia;
13. contexto;
14. falsadores;
15. resultado de la instancia.

La materialización documental del registro de resultados se incorporará al acto sucesor correspondiente a la evaluación ejecutada, salvo que el Operador determine documentalmente otro soporte antes de la observación.

No se utilizará un resultado global para ocultar resultados parciales.

---

## §29. Condiciones operativas y criterio de cierre

Se separan dos niveles.

### §29.1 Cierre de construcción del Acto 09

La construcción se considerará completa cuando:

1. corpus y criterio de selección estén fijados;
2. mecanismo de pre-registro esté definido;
3. instancia y rango tengan procedimiento de selección;
4. criterios I-1–I-4 estén operacionalizados;
5. falsadores estén declarados;
6. procedimiento de registro de evidencia esté definido.

Este cierre no equivale a evaluación exitosa.

### §29.2 Cierre de evaluación de U-SEQ-01

La evaluación sólo podrá cerrarse después de:

1. materializar el pre-registro;
2. ejecutar la observación;
3. preservar la evidencia;
4. producir el resultado de I-1–I-4;
5. confrontar los falsadores;
6. producir el registro de resultados durante la ejecución;
7. materializar documentalmente ese registro en el acto evaluativo sucesor;
8. someter la evaluación a falsación de IA-2.

Los puntos 6–8 pertenecen al ciclo evaluativo posterior a la construcción de este Acto 09 y no constituyen condiciones circulares de su construcción.

---

## §30. Límites

Este acto no:

- modifica el Motor Contable v8.2;
- modifica el Acto 08;
- modifica la Enmienda U-SEQ-01;
- crea un nuevo sistema contable;
- presume contexto formal persistido;
- reconstruye decisiones no registradas;
- infiere intención subjetiva;
- demuestra H-EMG-1;
- demuestra H-EMG-2.

---

## §31. Estado

CONSTRUIDO — PENDIENTE DE FALSACIÓN POR IA-2

Las objeciones O-115 a O-138 de las falsaciones de IA-2 han sido integradas en esta Versión D.

No materializado.

No firmado.

IA-1 no declara APTO.

---

## §32. Autoridad y próximo movimiento

IA-1 construye.

IA-2 falsará.

El Operador autoriza cualquier materialización.

La siguiente acción bilateral es:

IA-2 → falsación de la Versión D del Acto 09.

No se ejecutará observación del corpus ni pre-registro material hasta que la construcción haya superado la falsación correspondiente y el Operador autorice el acto.

---

**FIN DEL CUERPO DEL ACTA**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** f293e074f8d6dfaec9280ec8fe67fd41719683ab732c413d72313d674e010f2e

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter.

**Nota:** hash previo = cuerpo anterior al registro. Hash final = documento completo tras incorporación del registro, comunicado externamente.

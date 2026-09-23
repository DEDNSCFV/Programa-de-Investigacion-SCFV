# PRE-REGISTRO DE EVALUACIÓN
## U-SEQ-01 · Giro 04 · Sesión 4

**Versión:** E
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Naturaleza:** pre-registro independiente previo a la observación evaluativa
**Acto de referencia:** "GIRO_04/09_evaluacion_useq_01.md"
**Base normativa inmediata:** §20-bis del Acto 09 materializado y firmado
**Autoría:** IA-1 — constructor
**Falsación:** IA-2 — APTO SIN OBJECIONES
**Autoridad:** Operador

---

## §1. Objeto

Fijar documentalmente, antes de la observación evaluativa, las condiciones bajo las cuales se ejecutará la primera evaluación de U-SEQ-01 sobre el corpus seleccionado.

El presente documento no contiene resultados de la evaluación.

Los valores de identificación de la instancia quedan incorporados antes de la materialización y firma definitiva del presente pre-registro.

Una vez firmado y materializado, las condiciones aquí fijadas no podrán modificarse después de iniciada la observación evaluativa, salvo mediante un acto documental posterior que deje constancia expresa de la modificación y de su momento respecto de la observación.

---

## §2. Fechas y horas

Fecha de elaboración: 2026-09-22
Hora de elaboración: 08:06:37

Fecha de firma: 2026-09-22
Hora de firma: 08:06:37

La observación evaluativa deberá comenzar después de la firma y materialización del presente pre-registro.

---

## §3. Base material seleccionada

La evaluación se realizará sobre:

"~/scfv_v6/scfv.db"

El criterio de selección de esta base fue fijado previamente en el Acto 09 §4: entre las bases candidatas identificadas, seleccionar aquella que contenga el mayor número de eventos "ASIENTO_REGISTRADO", siempre que sea técnicamente legible y evaluable conforme a las condiciones declaradas.

La verificación previa registró:

- "ASIENTO_REGISTRADO": 10
- "DECISION_H2": 0

Esta composición constituye un dato previo de identificación del corpus y no constituye un resultado de la evaluación de U-SEQ-01.

La evidencia previa de composición fue obtenida mediante consultas SQLite separadas sobre "event_store", limitadas al conteo por tipo de evento.

Consulta para "ASIENTO_REGISTRADO":

    SELECT COUNT(*)
    FROM event_store
    WHERE tipo_evento = 'ASIENTO_REGISTRADO';

Consulta para "DECISION_H2":

    SELECT COUNT(*)
    FROM event_store
    WHERE tipo_evento = 'DECISION_H2';

Fecha de verificación previa: 2026-09-22
Base: "~/scfv_v6/scfv.db"
Salida relevante: 10 eventos "ASIENTO_REGISTRADO", 0 eventos "DECISION_H2".

---

## §4. Criterio de selección de la base

El criterio de selección es:

«seleccionar, entre las bases candidatas previamente identificadas, aquella que contenga el mayor número de eventos "ASIENTO_REGISTRADO", siempre que sea técnicamente legible y evaluable conforme a las condiciones del Acto 09 §4-ter.»

La composición de la base no podrá modificarse en función del resultado esperado de la evaluación.

La imposibilidad técnica se limitará a las condiciones definidas en el Acto 09 §4-ter.

Un resultado desfavorable, inconcluso o no disponible no constituye imposibilidad técnica.

---

## §4-bis. Criterios fijados antes de la observación

Antes de observar el contenido evaluativo se consideran fijados:

1. la base de trabajo;
2. el criterio de selección de la base;
3. la versión de U-SEQ-01 y su régimen documental;
4. la versión del Motor Contable;
5. la pregunta evaluativa;
6. I-1, I-2, I-3 e I-4;
7. el criterio de selección de la instancia;
8. el tratamiento del primer evento;
9. el régimen de reproducibilidad;
10. el régimen de falsación;
11. la condición H2-A prevista por la composición previamente verificada;
12. el criterio de comparación de representaciones.

Ninguno de estos elementos podrá seleccionarse o modificarse después de conocer el resultado evaluativo con el propósito de favorecer una conclusión.

---

## §5. k_inicial

"k_inicial" corresponde al "event_store.id" del primer evento "ASIENTO_REGISTRADO" del corpus completo seleccionado.

Valor definitivo:

k_inicial = 1

El valor fue obtenido mediante el procedimiento de identificación previa del §5-bis.

No fue inferido, estimado ni seleccionado manualmente.

---

## §5-bis. Identificación previa de k_inicial y k_evento

La identificación de "k_inicial" y "k_evento" constituye una operación de ubicación documental previa, no una observación evaluativa.

La consulta limitó su acceso a la estructura de "event_store", utilizando exclusivamente:

- "id";
- "tipo_evento".

La consulta no observó:

- "payload";
- "partidas";
- "monto";
- "cuenta";
- "evidencia";
- "justificacion_h2";
- ni ningún otro contenido utilizado por los criterios I-1–I-4.

Consulta ejecutada:

    SELECT id, tipo_evento
    FROM event_store
    WHERE tipo_evento = 'ASIENTO_REGISTRADO'
    ORDER BY id ASC
    LIMIT 1;

Resultado: id = 1, tipo_evento = 'ASIENTO_REGISTRADO'.

Para esta primera instancia, el criterio del §6 produce:

k_evento = k_inicial = 1

La consulta de identificación no fue utilizada para seleccionar una instancia por su contenido favorable o desfavorable, porque el contenido evaluativo no fue leído durante esta operación.

La identificación quedó documentada conforme al §5-ter.

Si el "payload" no pudiera ser recuperado o deserializado, esa condición no invalidaría la identificación previa. La recuperabilidad del "payload" corresponde a la observación evaluativa de U-SEQ-01 y no al presente pre-registro.

---

## §5-ter. Constancia de la identificación previa

La constancia de la consulta de identificación forma parte del mismo pre-registro materializado.

La salida de la consulta no permaneció únicamente en "stdout" efímero.

Fue capturada en un archivo de texto destinado exclusivamente a conservar la evidencia de identificación previa.

Archivo de salida de identificación:

"GIRO_04/identificacion_previa_useq_01.out.txt"

El archivo contiene únicamente la salida de identificación correspondiente a "id" y "tipo_evento".

Se registra:

Consulta SQL ejecutada:

    SELECT id, tipo_evento
    FROM event_store
    WHERE tipo_evento = 'ASIENTO_REGISTRADO'
    ORDER BY id ASC
    LIMIT 1;

Base consultada: "~/scfv_v6/scfv.db"

Fecha de ejecución: 2026-09-22

Hora de ejecución: 08:06:37

Resultado "k_inicial": 1

Resultado "k_evento": 1

SHA-256 del archivo de salida:

80218cbfd4fb7bfad75d7443bc9e9ffb9cc0b3fa7c5bbccaab95599ba017d6ef

El SHA-256 indicado en esta sección es un hash de evidencia externa: identifica el archivo de salida de la consulta. No es el hash previo ni el hash final del presente pre-registro.

El archivo de salida y su hash quedan conservados como evidencia de la operación de identificación.

No se incorporaron al registro de identificación valores derivados del "payload".

La consulta de identificación es una operación de ubicación de la instancia; la lectura del "payload" comienza con la observación evaluativa posterior.

---

## §6. Criterio de selección de la instancia

La instancia evaluada será:

«el primer evento "ASIENTO_REGISTRADO" según el orden canónico de "event_store.id" dentro del corpus seleccionado.»

Valor definitivo:

k_evento = 1

Para esta primera instancia no existe un "k_t" anterior.

Conforme al Acto 09 §7-bis, el estado previo será representado inicialmente como:

{}

La ausencia de un asiento anterior no constituye por sí misma una falla de la evaluación.

---

## §7. Especificación documental de U-SEQ-01

La especificación evaluada será:

U-SEQ-01 Versión I

Documento:

"GIRO_04/08_unidad_secuencia.md"

Hash final materializado:

5bb94a423a1fc4cb0944b99e5c4b4b697f39564991f441dae269dc8c6bae45e9

La especificación queda parcialmente desplazada en los extremos expresamente determinados por:

Acta de Enmienda U-SEQ-01 — Giro 04, Versión E

Documento:

"ACTAS/ACTA_ENMIENDA_USEQ_01_GIRO_04.md"

Hash final:

ee6ee209ee3d24963bf47cf42e7e0ad205ff6ab9456cd376f65b7b0e52fcb515

Por tanto:

«U-SEQ-01 Versión I tal como queda parcialmente desplazada por la Acta de Enmienda U-SEQ-01, Versión E, en los puntos expresamente declarados en su §11.»

No existe una "U-SEQ-01 Versión E". La Versión E corresponde al acta de enmienda, no a una nueva versión nominal de la unidad.

---

## §8. Versión del Motor Contable

Motor Contable: v8.2

El Motor Contable v8.2 se considera congelado para esta evaluación.

No se realizará reimplementación del motor como parte de esta instancia.

La evaluación observará el corpus persistido y las estructuras necesarias para representar la secuencia conforme a las condiciones declaradas.

---

## §9. Pregunta evaluativa

La pregunta pre-registrada es:

«¿Puede U-SEQ-01 representar y evaluar una transición contable persistida, reproducible dentro del corpus evaluado, preservando I-1, I-2, I-3 e I-4 en la medida materialmente evaluable, sin introducir inferencias sobre intención subjetiva y manteniendo la trazabilidad disponible?»

La respuesta no está determinada por este pre-registro.

---

## §10. Invariantes y propiedades de evaluación

Las condiciones I-1–I-4 se evaluarán conforme a:

- "GIRO_04/08_unidad_secuencia.md" §§16–18;
- "ACTAS/ACTA_ENMIENDA_USEQ_01_GIRO_04.md" §7 y disposiciones de desplazamiento declaradas en §11;
- Acto 09 §§10–18.

### I-1 — Identidad de estados

El estado previo y el estado resultante deberán poder identificarse y diferenciarse conforme a las condiciones de U-SEQ-01 vigentes.

Para la primera instancia, el estado previo será "{}" conforme al §7-bis del Acto 09.

### I-2 — Conservación de partida doble

Se verificará:

    |ΣDebe − ΣHaber| ≤ 0.001

La determinación de Debe/Haber utilizará la estructura material de "partidas", particularmente:

- "cuenta";
- "naturaleza";
- "movimiento";
- "monto".

Se contrastará además con:

- "total_debe";
- "total_haber".

La determinación de la naturaleza del movimiento utilizará la lógica XNOR establecida en el Acto 09.

### I-3 — Determinabilidad de transición

Dado el estado previo, el movimiento persistido y las reglas declaradas, deberá poder determinarse el estado resultante conforme a la representación evaluada.

### I-4 — Trazabilidad

Se evaluará la trazabilidad materialmente disponible entre:

- decisión H2, cuando exista en el corpus;
- movimiento;
- evento "ASIENTO_REGISTRADO";
- identificadores persistidos;
- evidencia estructurada;
- representación del estado.

Las categorías serán:

- "PASS";
- "FAIL";
- "INCONCLUSO";
- "NO DISPONIBLE".

La ausencia de un elemento no será convertida en inferencia de existencia.

---

## §11. Criterio de comparación de representaciones

Cuando corresponda comparar representaciones, la comparación utilizará la serialización canónica mediante:

"PODERES/INFRAESTRUCTURA/serializador_canonico.py"

y su función "serializar(...)".

La comparación se limitará a representaciones materialmente disponibles y declaradas.

No se considerará equivalente una representación cuya igualdad dependa de datos no persistidos.

---

## §12. Previsión de composición del corpus y condición H2

Antes de la observación queda registrada la composición previamente verificada de la base:

- 10 "ASIENTO_REGISTRADO";
- 0 "DECISION_H2".

Conforme a la definición de estados H2 del Acto 09 §14, la condición prevista para esta instancia es:

«H2-A: H2 ausente en el corpus evaluado.»

Esta previsión describe la composición material previamente identificada y no constituye el resultado de I-4.

La evaluación no podrá cambiar de corpus con el propósito de obtener otra condición H2.

Si la observación contradice la composición previamente verificada, la discrepancia será registrada como evidencia antes de modificar cualquier condición evaluativa.

---

## §13. Reproducibilidad

La reproducibilidad evaluada se refiere al corpus persistido seleccionado.

No se considerará reproducibilidad del mismo resultado la repetición del Motor Contable sobre una nueva ejecución, debido a la intervención de "uuid4()" en la generación de identificadores.

Las reglas documentales de U-SEQ-01 y su Enmienda E distinguen:

- "event_store.id" → orden canónico;
- "idempotency_key" → identidad del evento;
- "correlation_id" → identidad del movimiento.

Estas reglas no serán alteradas durante la observación.

---

## §14. Condición de no confirmación

La selección de base e instancia no podrá modificarse después de observar el resultado para favorecer una conclusión determinada.

Un resultado desfavorable, inconcluso o no disponible será registrado como tal.

La repetición sobre otra base requerirá un nuevo acto documental con sus propias condiciones pre-registradas.

---

## §15. Falsadores previamente declarados

La evaluación podrá producir evidencia contra U-SEQ-01 si, en la instancia definida:

1. no puede identificarse el estado previo o resultante conforme a las reglas declaradas;
2. no puede verificarse la conservación de partida doble;
3. no puede determinarse reproduciblemente la transición dentro del corpus persistido;
4. la representación no puede vincularse a los identificadores y evidencia materialmente disponibles;
5. la unidad requiere inferir intención subjetiva para producir su evaluación;
6. las condiciones declaradas resultan incompatibles con la estructura real del corpus.

La observación deberá registrar evidencia positiva o negativa, no solamente una conclusión verbal.

---

## §16. Condición previa a la observación

La observación queda bloqueada hasta que:

1. este documento sea falsado bilateralmente por IA-2;
2. las objeciones pertinentes sean integradas;
3. el Operador autorice su materialización;
4. el documento sea materializado conforme al §19.3-bis;
5. exista registro propio de integridad y hash final;
6. exista constancia del Operador.

Hasta entonces, no existe resultado evaluativo.

---

## §16-bis. Estados del pre-registro

El pre-registro distingue tres fases operativas.

### Fase A — Elaboración

Corresponde al período de construcción del documento.

Puede contener campos pendientes de identificación.

No constituye el pre-registro materializado y no autoriza observación.

### Fase B — Identificación previa

Se ejecuta únicamente después de la autorización correspondiente y antes de la firma definitiva.

Comprende:

1. consulta limitada a "id" y "tipo_evento";
2. identificación de "k_inicial" y "k_evento";
3. captura de la salida en el archivo de §5-ter;
4. cálculo del SHA-256 de ese archivo;
5. incorporación de resultados y evidencia al cuerpo.

No comprende lectura del "payload".

### Fase C — Pre-registro fijado y materializado

Se alcanza cuando:

1. los valores de identificación fueron incorporados;
2. la constancia de identificación fue incorporada;
3. el Operador firmó la constancia del §18;
4. el cuerpo quedó cerrado;
5. se calculó el hash previo sobre ese cuerpo;
6. se incorporó el bloque final de integridad;
7. se calculó el hash final.

Sólo la Fase C constituye el pre-registro materializado que habilita la observación.

---

## §17. Régimen de integridad

El régimen de integridad no incorpora campos de hash dentro del cuerpo numerado del pre-registro.

El procedimiento será:

«cuerpo definitivo y firmado → cálculo del hash previo → incorporación del bloque final de registro de integridad → cálculo del hash final.»

El hash previo deberá corresponder exactamente al cuerpo existente después de completar la identificación y la constancia del Operador, pero antes de añadir el registro de integridad.

Se aplican:

- H-EXT-01-bis: coherencia del estatuto efectivo declarado en el encabezado;
- H-EXT-01-ter: orden cuerpo → hash previo → registro de integridad → hash final.

Esta regla se refiere exclusivamente a los hashes propios del presente pre-registro.

El SHA-256 de la salida de identificación previsto en §5-ter es diferente: constituye hash de evidencia externa, forma parte del cuerpo porque identifica un objeto externo y no participa en el cálculo del hash previo como campo independiente.

---

## §18. Constancia del Operador

La constancia del Operador queda incorporada al cuerpo antes de iniciar la observación evaluativa.

El Operador declara que:

1. las condiciones evaluativas quedan fijadas antes de la observación;
2. la identificación previa de "k_inicial" y "k_evento" fue realizada sin observar el contenido evaluativo del "payload";
3. los valores identificados fueron incorporados al presente documento antes de su firma;
4. el documento no será utilizado para modificar retrospectivamente las condiciones de observación;
5. la constancia corresponde al cuerpo documental existente al momento de la firma.

Operador: Domingo E. Díaz N.
Fecha de firma: 2026-09-22
Hora de firma: 08:06:37
Constancia/firma: DEDN — C.P.C. Nº 183594

La constancia no contiene el hash previo ni el hash final.

---

## §19. Estado del acto

IA-1: construcción integrada de O-139–O-162 y Em-31–39.

IA-2: verificación final — APTO SIN OBJECIONES.

Operador: autoriza materialización.

Estado efectivo: MATERIALIZADO Y FIRMADO.

---

## §20. Secuencia obligatoria antes de la observación

La secuencia documental fue:

1. IA-2 verifica el presente borrador. Cumplido.
2. el Operador autoriza la ejecución de la identificación previa. Cumplido.
3. se consulta "event_store" exclusivamente mediante "id" y "tipo_evento". Cumplido.
4. se obtienen "k_inicial" y "k_evento". Cumplido: k_inicial = k_evento = 1.
5. se captura la salida en el archivo de §5-ter. Cumplido.
6. se calcula el SHA-256 de dicho archivo. Cumplido.
7. se incorporan "k_inicial", "k_evento", consulta, fecha, hora y hash de evidencia al cuerpo. Cumplido.
8. el Operador firma la constancia del §18. Cumplido.
9. se cierra el cuerpo.
10. se calcula el hash previo.
11. se incorpora el bloque final de "REGISTRO DE INTEGRIDAD".
12. se calcula el hash final.
13. se verifica externamente la integridad.
14. sólo entonces se inicia la observación evaluativa.

La observación evaluativa no se inicia en este acto.

Ningún paso posterior podrá utilizarse para seleccionar retrospectivamente otra instancia en función del resultado.

---

## §21. Siguiente acción bilateral

La siguiente acción corresponde a:

«Inicio de la observación evaluativa de U-SEQ-01 conforme a las condiciones pre-registradas.»

La observación se ejecutará mediante un acto documental posterior que no modifique las condiciones aquí fijadas.

---

**FIN DEL CUERPO DEL PRE-REGISTRO**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** 8a70b0c4d9264639d04328d4bb34ae90f61652071fdfc06fe973de52078cf7ad

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter.

**Nota:** hash previo = cuerpo anterior al registro. Hash final = documento completo tras incorporación del registro, comunicado externamente.

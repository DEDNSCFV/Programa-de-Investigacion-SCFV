# U-SEQ-01 · UNIDAD DE SECUENCIA

**Giro:** 04
**Sesión:** 4
**Design Cycle:** primer movimiento
**Ruta canónica:** "GIRO_04/08_unidad_secuencia.md"
**Versión:** I
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Rol de construcción:** IA-1
**Falsación:** IA-2 — APTO SIN OBJECIONES
**Autoridad de materialización:** Operador

---

## §1. Objeto

U-SEQ-01 define una unidad de secuencia para representar y evaluar una transición contable observable:

estado previo → movimiento → estado resultante

La unidad no pretende inferir intención subjetiva, dolo, fraude ni cualquier otro estado mental del sujeto.

Su función es hacer evaluable una transición contable materializada sobre el corpus persistido del SCFV.

---

## §2. Estatuto

U-SEQ-01 es una unidad de diseño de "SCFV_DSR".

No constituye un nuevo motor contable, una nueva autoridad contable ni una sustitución del Motor Contable.

La unidad utiliza infraestructura existente y añade una especificación de representación y evaluación.

---

## §3. Tipo de artefacto

El artefacto es un modelo de representación de una secuencia contable observable.

Su soporte primario es documental.

Podrá requerir código mínimo adicional cuando la evaluación no pueda ejecutarse con la infraestructura existente.

La construcción de código adicional no implica la construcción de un segundo Motor Contable.

---

## §4. Relación con SCFV_DSR

U-SEQ-01 materializa uno de los componentes previstos en:

"GIRO_04/07_materializacion_scfv_dsr.md"

La unidad pertenece al dominio de diseño de "SCFV_DSR".

No constituye por sí misma una validación de las hipótesis globales H-EMG-1 o H-EMG-2.

---

## §5. Relación con S0

S0 constituye antecedente material del Programa.

U-SEQ-01 no presupone identidad representacional entre S0 y "SCFV_DSR".

La relación S0 ↔ SCFV_DSR permanece como cuestión evaluable dentro del design cycle.

---

## §6. Posición dentro de la cadena funcional

La cadena funcional declarada para el artefacto es:

tablero → secuencia → trayectoria → evaluación → demostración

La cadena funcional no establece por sí misma un orden obligatorio de construcción.

U-SEQ-01 puede construirse antes que el componente tablero porque la unidad posee condiciones de evaluación independientes.

---

## §7. Alcance

U-SEQ-01 evalúa una transición contable observable materializada en el EventStore.

Incluye:

- estado previo;
- movimiento contable;
- estado resultante;
- evidencia asociada;
- contexto contable;
- identificadores persistidos;
- propiedades evaluables.

No incluye:

- inferencia de intención;
- inferencia de dolo;
- determinación automática de responsabilidad subjetiva;
- sustitución de la decisión profesional H2;
- reconstrucción histórica ilimitada;
- validación global de H-EMG-1 o H-EMG-2.

---

## §8. Unidad evaluable

La unidad evaluable es una secuencia materializada que contiene:

1. un estado previo;
2. un movimiento contable;
3. evidencia asociada;
4. un estado resultante;
5. las propiedades declaradas para evaluación.

### §8.1 Identificadores reales

La unidad utiliza los identificadores existentes del corpus:

- "event_store.id": identificador entero del evento y referencia canónica de orden de inserción;
- "idempotency_key": identidad del evento persistido;
- "correlation_id": identidad de correlación del movimiento;
- "asiento_id": identificador del asiento contenido en el payload;
- "decision_id": identificación de la decisión H2 persistida;
- "propuesta_id": identificación de la propuesta asociada;
- "firma_h2": firma persistida de la decisión H2;
- "evidencia_hash": identificación de evidencia mediante su hash.

"state_id" no se toma de una entidad preexistente del Motor Contable. Es un identificador derivado propio de U-SEQ-01.

### §8.2 Contexto contable

El contexto se obtiene del payload deserializado del asiento mediante:

"payload["contexto_contable"]"

El contexto comprende, cuando estén presentes:

- "marco_contable";
- "PCU_version";
- "reglas_version";
- "politica_monetaria_version".

### §8.3 Estado

Un estado es una posición contable observable en un punto determinado de la secuencia.

Su representación mínima comprende:

- "state_id";
- contexto contable;
- conjunto de cuentas afectadas;
- saldo observable de cada cuenta relevante;
- referencia al movimiento;
- identificadores del evento;
- evidencia asociada.

El estado no es el asiento.

El asiento es el movimiento que produce una transición entre estados.

---

## §9. Lectura canónica del EventStore

U-SEQ-01 requiere una lectura que conserve los metadatos necesarios para ordenar e identificar los eventos.

Se declara conceptualmente la función propia:

"leer_eventos_asiento(db_path, correlation_id=None, id_hasta=None)"

### §9.1 Forma de la lectura

La lectura canónica de U-SEQ-01 utiliza la vía (b):

«"leer_eventos_asiento()" filtra por "id_hasta" y admite "correlation_id" como filtro opcional.»

La firma conceptual es:

    leer_eventos_asiento(
        db_path,
        id_hasta,
        correlation_id=None
    )

"id_hasta" es obligatorio en la evaluación porque la unidad opera sobre un rango canónico finito.

"correlation_id" es opcional:

- si se omite, la función retorna todos los eventos "ASIENTO_REGISTRADO" hasta "id_hasta";
- si se declara, la función restringe el resultado al movimiento identificado por dicho "correlation_id".

El uso principal para calcular estados utiliza la lectura sin filtro de "correlation_id", porque los saldos dependen del conjunto de eventos comprendido en el rango.

### §9.2 Retorno y payload

La función retorna una colección de registros de eventos con:

- id
- idempotency_key
- correlation_id
- payload
- timestamp

El campo "payload" retorna deserializado como estructura de datos.

La deserialización se realiza dentro de "leer_eventos_asiento()" mediante la función existente:

"deserializar(...)"

ubicada en:

"PODERES/INFRAESTRUCTURA/serializador_canonico.py:290"

Esto permite que el resultado de la lectura sea directamente compatible con "_saldos_mayor(...)".

No se declara que "leer_eventos_asiento()" exista actualmente en el corpus.

### §9.3 Ubicación prevista

La función será parte del soporte mínimo de evaluación de U-SEQ-01 y se materializará como código dentro del componente de evaluación de "SCFV_DSR" cuando la evaluación lo requiera.

No se declara que esta función exista actualmente.

### §9.4 Precedentes existentes

La función propia no sustituye las lecturas existentes.

Como precedentes del corpus se reconocen:

- "_leer_asientos(...)", utilizado para obtener payloads de asientos;
- "integrator.reproducir_asiento(...)", que realiza una lectura ampliada del EventStore.

U-SEQ-01 requiere conservar los metadatos que "_leer_asientos(...)" no retorna.

---

## §10. Representación del estado resultante

El estado resultante es una estructura observable y consultable mediante la infraestructura existente y el soporte mínimo de evaluación de U-SEQ-01.

Su cálculo reutiliza el mecanismo de saldos:

"_saldos_mayor(...)"

No se crea una segunda implementación del cálculo de saldos.

La representación queda vinculada al EventStore y al Motor Contable v8.2.

---

## §11. Identidad determinista del estado

"state_id" se deriva de:

    SHA-256(
        serializar(
            (correlation_id, idempotency_key)
        )
    )

El serializador utilizado es:

"PODERES/INFRAESTRUCTURA/serializador_canonico.py"

y su función "serializar(...)".

### §11.1 Dominio de estabilidad

El "state_id" es estable para el par persistido:

(correlation_id, idempotency_key)

dentro del corpus evaluado.

No se afirma que sea estable frente a una nueva ejecución del Motor Contable.

El Motor Contable utiliza "uuid4()" para el identificador del asiento; por ello, una nueva ejecución puede producir un nuevo "asiento_id" y, consecuentemente, un nuevo "idempotency_key".

---

## §12. Observación canónica

La observación de una secuencia se realizará mediante:

1. lectura de eventos "ASIENTO_REGISTRADO" desde EventStore hasta el corte declarado;
2. conservación de "event_store.id";
3. conservación de "idempotency_key";
4. conservación de "correlation_id";
5. recuperación del payload deserializado;
6. cálculo de saldos mediante "_saldos_mayor(...)".

El "timestamp" se conserva como dato observable, pero no constituye el orden canónico de la secuencia.

---

## §13. Conjunto de cuentas

El conjunto de cuentas relevante para el movimiento evaluado se determina a partir de las cuentas presentes en las partidas "Debe" y "Haber" del asiento contenido en el payload correspondiente.

No se declara un conjunto de cuentas independiente del movimiento.

Los saldos relevantes se obtienen mediante "_saldos_mayor(...)".

---

## §13-bis. Rango y cortes canónicos

U-SEQ-01 utiliza una única definición de rango canónico de evaluación:

[k_inicial, k_t+1]

donde:

- "k_inicial" = "event_store.id" del primer evento "ASIENTO_REGISTRADO" del corpus completo evaluado;
- "k_t" = "event_store.id" del evento "ASIENTO_REGISTRADO" inmediatamente anterior al movimiento evaluado;
- "k_evento" = "event_store.id" del evento "ASIENTO_REGISTRADO" correspondiente al movimiento evaluado;
- "k_t+1" = "k_evento" en la transición elemental canónica.

La instancia de evaluación no puede recortar arbitrariamente el inicio del rango. Si existen eventos "ASIENTO_REGISTRADO" anteriores al movimiento evaluado, el rango canónico se extiende desde el primero de esos eventos.

Por tanto:

    k_inicial <= k_t < k_evento = k_t+1

### §13-bis.1 Estado previo

El estado previo se calcula sobre los eventos comprendidos en:

[k_inicial, k_t]

### §13-bis.2 Movimiento

El movimiento evaluado corresponde al evento:

    id = k_evento

con:

    tipo_evento = ASIENTO_REGISTRADO

### §13-bis.3 Estado resultante

En la transición elemental canónica, el estado resultante se calcula sobre:

[k_inicial, k_t+1]

donde:

    k_t+1 = k_evento

Así:

    Estado_t   = saldos([k_inicial, k_t])

    Movimiento = evento con id = k_evento

    Estado_t+1 = saldos([k_inicial, k_t+1])

### §13-bis.4 Cortes alternativos

Un corte distinto del canónico solamente es admisible cuando:

1. la instancia de evaluación lo declara explícitamente;
2. el corte permanece dentro del corpus persistido disponible;
3. existe una justificación metodológica relacionada con la pregunta de evaluación;
4. el corte queda registrado como condición de la instancia;
5. su selección no se justifica por el resultado esperado.

El corte alternativo forma parte de la evidencia del ciclo y debe poder ser reconstruido por IA-2.

La transición elemental:

    k_t+1 = k_evento

es el caso canónico de U-SEQ-01.

Un corte posterior permite observar consecuencias posteriores al movimiento, pero constituye una instancia distinta de evaluación y no modifica retrospectivamente la definición de la transición elemental.

---

## §14. Reutilización de infraestructura

U-SEQ-01 reutiliza:

- EventStore para persistencia;
- "deserializar(...)" del serializador canónico para recuperar el payload como estructura de datos;
- "_saldos_mayor(...)" para el cálculo de saldos;
- Motor Contable v8.2 como fuente de las reglas contables ya existentes.

No reimplementa el Motor Contable.

---

## §15. Condiciones de evaluación

Una instancia de evaluación debe declarar como mínimo:

1. base de datos o corpus utilizado;
2. "k_inicial";
3. "k_evento";
4. "k_t" si difiere del evento "ASIENTO_REGISTRADO" inmediatamente anterior;
5. "k_t+1";
6. si existe, cualquier corte alternativo;
7. evento "ASIENTO_REGISTRADO" evaluado;
8. contexto contable;
9. conjunto de cuentas relevantes;
10. evidencia asociada;
11. propiedades evaluadas;
12. resultado de la evaluación.

Cuando "k_t" coincide con el inmediato anterior por defecto, no requiere una declaración alternativa; forma parte de la regla canónica de la unidad.

---

## §16. Invariantes

### I-1. Identidad de estados

El estado previo y el estado resultante deben ser identificables y diferenciables.

### I-2. Conservación de partida doble

La igualdad:

    ΣDebe − ΣHaber = 0

se verifica sobre el asiento correspondiente al movimiento evaluado.

Esta verificación es coherente con la validación por asiento existente en el Motor Contable.

No se interpreta I-2 como una nueva validación global del corpus.

### I-3. Determinabilidad de transición

Dado:

- el estado previo;
- el movimiento persistido;
- las reglas existentes del Motor Contable v8.2;
- las reglas de partida doble/XNOR aplicables;

el estado resultante debe poder determinarse de manera consistente.

### I-4. Trazabilidad

La transición debe conservar trazabilidad mediante los identificadores persistidos:

    decision_id
    propuesta_id
    firma_h2
    correlation_id
    event_store.id
    idempotency_key
    asiento_id
    evidencia_hash
    state_id

No todos los identificadores tienen la misma función.

"event_store.id" determina orden.

"idempotency_key" identifica el evento persistido.

"correlation_id" identifica la correlación del movimiento.

"state_id" identifica la representación derivada de U-SEQ-01.

---

## §17. H2 y posición de la unidad

U-SEQ-01 opera después de H2.

La decisión profesional H2 debe encontrarse persistida antes del asiento.

La unidad no toma la decisión H2.

La unidad representa y evalúa la transición producida después de esa decisión.

La persistencia H2 se referencia mediante los identificadores:

- "decision_id";
- "propuesta_id";
- "firma_h2".

La localización de H2 forma parte del corpus de consecuencias que precede al "ASIENTO_REGISTRADO" evaluado. La instancia deberá aportar la referencia concreta al registro o evento que contiene esos identificadores.

U-SEQ-01 no presupone una tabla independiente para H2 ni declara que "negocio_diario" sea su almacenamiento.

---

## §18. Reproducibilidad

La reproducibilidad de U-SEQ-01 se define sobre el rango canónico de evaluación:

[k_inicial, k_t+1]

Una segunda lectura debe producir la misma representación cuando:

1. se utiliza el mismo corpus de eventos comprendido en ese rango;
2. se mantienen las mismas reglas declaradas;
3. se mantienen las mismas condiciones de evaluación.

### §18.1 Eventos posteriores

La aparición de nuevos eventos con:

    event_store.id > k_t+1

no altera la reproducibilidad de la instancia evaluada, porque esos eventos quedan fuera del rango canónico.

### §18.2 Cambios dentro del rango

Una modificación, eliminación o sustitución de eventos dentro de:

[k_inicial, k_t+1]

constituye un corpus distinto para efectos de reproducibilidad.

### §18.3 Límite

La reproducibilidad aquí definida no incluye la re-ejecución del Motor Contable.

Una nueva ejecución del motor puede producir nuevos identificadores UUID y nuevos "idempotency_key".

---

## §19. Relación con la evaluación DSR

La construcción de U-SEQ-01 no constituye por sí misma evaluación exitosa del artefacto.

La evaluación deberá producir evidencia sobre:

- representabilidad;
- determinabilidad;
- conservación de invariantes;
- trazabilidad;
- reproducibilidad dentro del rango canónico.

Los resultados serán incorporados en un acto posterior de evaluación.

---

## §20. Condición de falsación

U-SEQ-01 queda falsada en su formulación actual si una evaluación reproducible dentro del dominio declarado demuestra, entre otros posibles resultados:

1. que el estado previo y el resultante no pueden diferenciarse;
2. que I-2 no puede verificarse para el asiento evaluado;
3. que la transición no puede determinarse con las reglas declaradas;
4. que la evidencia no puede vincularse al movimiento;
5. que la representación cambia entre lecturas del mismo rango canónico sin cambio declarado de reglas o corpus;
6. que la unidad requiere inferir intención subjetiva para producir su evaluación.

La falsación de U-SEQ-01 no implica por sí misma la falsación de todo "SCFV_DSR".

---

## §21. Caso falsable

El caso falsable forma parte del conjunto de instancias evaluadas y su resultado se registra como evidencia del ciclo.

El caso no constituye por sí mismo una demostración de H-EMG-1 ni H-EMG-2.

---

## §22. Control positivo

La evaluación deberá incluir al menos un caso positivo en el que:

- exista un "ASIENTO_REGISTRADO";
- exista decisión H2 persistida y sus identificadores sean recuperables;
- exista evidencia asociada;
- el asiento satisfaga I-2;
- el estado previo pueda obtenerse;
- el estado resultante pueda calcularse;
- la trazabilidad pueda reconstruirse.

La persistencia H2 se considerará demostrada para la instancia cuando los identificadores "decision_id", "propuesta_id" y "firma_h2" puedan vincularse documentalmente al contexto de consecuencias que precede al "ASIENTO_REGISTRADO" evaluado.

El control positivo sirve para verificar que la unidad puede operar sobre una instancia conforme a sus condiciones declaradas.

---

## §23. Relación con las aporías del Giro 03

U-SEQ-01 hereda expresamente las limitaciones declaradas en:

"GIRO_04/07_materializacion_scfv_dsr.md §13"

incluyendo las aporías:

- A-1a;
- A-1b;
- A-2a;
- A-2b.

La unidad no transforma esas aporías en mecanismos automáticos de detección de intención, dolo o fraude.

---

## §24. Relación con Hevner

La aplicación de Hevner se realiza sobre:

1. objeto: U-SEQ-01 dentro de "SCFV_DSR";
2. problema: representación y evaluación de transiciones contables observables;
3. aspecto de construcción/evaluación: modelo de secuencia y condiciones de evaluación;
4. criterio: constructo/modelo evaluable dentro del ciclo DSR;
5. evidencia: corpus persistido, instancias de secuencia y resultados de evaluación;
6. construcción material;
7. demostración;
8. evaluación;
9. resultado;
10. convergencia/divergencia/emergencia/enriquecimiento.

Los puntos 1–5 pueden declararse antes de la construcción.

Los puntos 6–10 requieren evidencia producida por la construcción y evaluación correspondiente y serán completados en el acto sucesor cuando proceda.

La mera mención de Hevner no constituye aplicación metodológica.

---

## §25. Relación con H-EMG-1 y H-EMG-2

U-SEQ-01 aporta evidencia local al design cycle.

No confirma por sí misma:

- H-EMG-1: reconstrucción de los cuatro dominios históricos;
- H-EMG-2: operación como motor contable reutilizable.

Su resultado podrá constituir evidencia parcial dentro de las evaluaciones de esas hipótesis.

---

## §26. Alcance del código adicional

Si la evaluación requiere código adicional, este deberá limitarse al soporte de lectura, representación o evaluación de U-SEQ-01.

No podrá alterar el Motor Contable v8.2 para producir artificialmente el resultado buscado.

La necesidad de código adicional será documentada como parte del ciclo.

---

## §27. Estado epistemológico

U-SEQ-01 es una construcción provisional del design cycle.

No se declara como propiedad demostrada del SCFV.

La fractalidad permanece como hipótesis de diseño y no constituye un invariante de esta unidad.

---

## §28. Estado de aplicación Hevner

Antes de la construcción:

- objeto;
- problema;
- aspecto;
- criterio;
- evidencia prevista.

Después de la construcción y evaluación:

- construcción material;
- demostración;
- evaluación;
- resultado;
- convergencia/divergencia/emergencia/enriquecimiento.

Los resultados posteriores deberán registrarse mediante acto sucesor y no mediante modificación retroactiva de esta especificación una vez materializada.

---

## §29. Dominio de falsabilidad

El dominio falsable de U-SEQ-01 comprende:

EventStore persistido
+
rango canónico [k_inicial, k_t+1]
+
ASIENTO_REGISTRADO
+
Motor Contable v8.2
+
reglas declaradas
+
evidencia asociada

Quedan fuera:

- re-ejecuciones no idénticas del motor;
- intenciones subjetivas;
- eventos posteriores al corte;
- afirmaciones globales sobre H-EMG-1/H-EMG-2.

---

## §30. Próximo acto

El acto bilateral de falsación concluyó con veredicto APTO SIN OBJECIONES.

La materialización de "GIRO_04/08_unidad_secuencia.md" se ejecuta bajo decisión expresa del Operador.

---

## §31. Estado del documento

IA-1: construcción integrada — Versión I.

IA-2: APTO SIN OBJECIONES.

Operador: materialización ejecutada.

Estado: MATERIALIZADO Y FIRMADO.

---

**FIN DEL CUERPO DEL ACTA**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** 1c976bec542faabe72fc84cc37095352c103b71a63c5f04746db83e6f4e31266

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter.

**Nota:** hash previo = cuerpo anterior al registro. Hash final = documento completo tras incorporación del registro, comunicado externamente.

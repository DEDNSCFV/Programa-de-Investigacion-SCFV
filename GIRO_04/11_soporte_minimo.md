════════════════════════════════════════════════════════════════════════
ACTA DE CONSTRUCCIÓN DEL SOPORTE MÍNIMO DE U-SEQ-01

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 11
Documento: GIRO_04/11_soporte_minimo.md
Versión: D
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN OBJECIONES.

Estatuto: este acto especifica el soporte mínimo de evaluación de U-SEQ-01.
No modifica S0. No modifica el Motor Contable. No modifica el corpus histórico.
No materializa código. No cierra I-3. No cierra U-SEQ-01. No cierra Giro 04.

Hash previo al registro: 7ca62b9b5c563faf9864cc6d1be67eb7b7f917d239a12111c6863945d428f734
Hash final registrado:   7c2cb6db7d899d3f31b154e186ef66808499cd74c1cfbb1d4d5d39be064d5159
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO DEL ACTO
────────────────────────────────────────────────────────────────────────

El presente acto constituye el sucesor documental de las especificaciones
establecidas en "ACTA_APERTURA_SESION_04_2026-09-21.md",
"GIRO_04/08_unidad_secuencia.md", "GIRO_04/09_evaluacion_useq_01.md" y
"GIRO_04/pre_registro_evaluacion_useq_01.md", sin modificar retroactivamente
ninguno de dichos actos.

Su objeto es especificar la construcción del soporte mínimo de evaluación
requerido para materializar la lectura de eventos declarada en
"GIRO_04/08_unidad_secuencia.md", §§9.2–9.3.

El soporte consiste en la función:

    leer_eventos_asiento(db_path, id_hasta, correlation_id=None)

Su finalidad es proporcionar al componente de evaluación de "SCFV_DSR" una
lectura reproducible de los eventos "ASIENTO_REGISTRADO" hasta un corte
determinado, entregando el "payload" deserializado mediante el mecanismo
canónico existente.

El presente acto especifica el soporte. No declara su materialización efectiva.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES DOCUMENTALES
────────────────────────────────────────────────────────────────────────

Son antecedentes directos:

1. "ACTA_APERTURA_SESION_04_2026-09-21.md";
2. "GIRO_04/08_unidad_secuencia.md", especialmente §§9.2–9.4, §10, §§13-bis
   y §16;
3. "GIRO_04/09_evaluacion_useq_01.md";
4. "GIRO_04/pre_registro_evaluacion_useq_01.md";
5. "ACTAS/ACTA_ENMIENDA_USEQ_01_GIRO_04.md";
6. "GIRO_04/06_diseno.md";
7. "GIRO_04/07_materializacion_scfv_dsr.md".

El hash materializado del pre-registro vigente es:

    9bb8c1faa741ab5712386fc470dd2091c71bd6bc8723434c9ed9a0f266457c91

El soporte aquí especificado deriva especialmente de la declaración de
"GIRO_04/08_unidad_secuencia.md" §9.3, que establece que la función será
parte del soporte mínimo de evaluación de U-SEQ-01 y que se materializará
dentro del componente de evaluación de "SCFV_DSR" cuando la evaluación lo
requiera.


────────────────────────────────────────────────────────────────────────
§3. NECESIDAD DEL SOPORTE
────────────────────────────────────────────────────────────────────────

La evaluación empírica de U-SEQ-01 identificó una divergencia entre:

1. la representación persistida del "payload" de "ASIENTO_REGISTRADO";
2. la interfaz actualmente consumida por "_saldos_mayor(...)";
3. la función de lectura actualmente disponible en
   "PODERES/CONTABLE/reportes_motor.py"; y
4. la función de lectura declarada conceptualmente en
   "GIRO_04/08_unidad_secuencia.md" §9.2.

La aplicación directa de la ruta material actual:

    event_store.payload
    → reportes_motor._leer_asientos(...)
    → _saldos_mayor(...)

sobre el evento evaluado produjo:

    {'?': -2000.0}

debido a que "_saldos_mayor(...)" espera los campos:

    cuenta_codigo
    ubicacion
    monto

mientras que el "payload" observado contiene:

    cuenta
    naturaleza
    movimiento
    monto

Esta divergencia no constituye por sí misma una falsación de U-SEQ-01 ni de
"SCFV_DSR".

Constituye una razón material para construir el soporte de evaluación
declarado en §9.3 del Acto 08.


────────────────────────────────────────────────────────────────────────
§4. NATURALEZA DEL SOPORTE
────────────────────────────────────────────────────────────────────────

"leer_eventos_asiento(...)" será exclusivamente un componente de lectura
para evaluación.

No constituye:

- Motor Contable;
- nuevo Motor;
- mecanismo de persistencia;
- sustituto del "EventStore";
- autoridad contable;
- mecanismo de decisión H2;
- mecanismo de autorización;
- componente de S0;
- sustituto de "reportes_motor._leer_asientos(...)";
- segundo sistema contable;
- fuente autónoma de verdad contable.

Su función queda limitada a recuperar y deserializar los eventos necesarios
para la evaluación declarada.


────────────────────────────────────────────────────────────────────────
§5. LOCUS ARQUITECTÓNICO
────────────────────────────────────────────────────────────────────────

La función será construida dentro del componente de evaluación de "SCFV_DSR".

Ese componente no se declara actualmente existente como módulo material
autónomo.

Por tanto, su creación forma parte de la implementación del presente acto.

La construcción no deberá modificar unilateralmente:

    PODERES/CONTABLE/reportes_motor.py

ni alterar:

- "_saldos_mayor(...)";
- el Motor Contable;
- el "EventStore";
- S0;
- el corpus histórico evaluado.

§5-bis. Locus físico previsto

El componente de evaluación residirá en un árbol dedicado a "SCFV_DSR".

El path físico concreto no se fija en el presente borrador.

Será declarado por el Operador en el acto de materialización correspondiente,
antes de ejecutar la construcción material.

La materialización deberá verificar expresamente la no-colisión con:

    ~/scfv_v6/
    ~/SCFV_S0_V1.0.0/

y con los árboles históricos que el Operador identifique como relevantes.

La ausencia de un path concreto en este borrador no constituye autorización
para que IA-1, IA-2 o el propio soporte lo decidan unilateralmente.


────────────────────────────────────────────────────────────────────────
§6. FIRMA FUNCIONAL
────────────────────────────────────────────────────────────────────────

La firma declarada es:

    leer_eventos_asiento(
        db_path,
        id_hasta,
        correlation_id=None
    )

§6.1 "db_path"

Identifica la base de datos sobre la cual se realizará la lectura.

La función no crea ni modifica la base de datos.

§6.2 "id_hasta"

Constituye el límite superior del rango de eventos.

El límite es inclusivo.

Por tanto:

    id ≤ id_hasta

El evento cuyo "id" sea exactamente igual a "id_hasta" forma parte de la
lectura.

§6.2-bis. IDs ausentes

La lectura filtra por:

    event_store.id ≤ id_hasta

Los IDs ausentes en el corpus no se generan artificialmente ni se interpretan
como eventos faltantes.

El rango representa el conjunto de eventos materialmente presentes cuyos "id"
satisfacen la condición de corte.

Una discontinuidad de IDs, si llegara a ser relevante para una evaluación
posterior, deberá ser registrada como propiedad observable del corpus y no
completada mediante inferencia.

§6.3 "correlation_id"

Es un filtro opcional.

Cuando no se proporciona, la lectura utiliza únicamente el corte "id_hasta".

Cuando se proporciona, actúa conjuntamente con "id_hasta".

§6.3-bis. Intersección de filtros

La presencia de "correlation_id" no sustituye el límite "id_hasta".

La condición de lectura será:

    id ≤ id_hasta
    Y
    correlation_id = correlation_id_proporcionado

cuando el segundo parámetro opcional esté presente.

Cuando no esté presente, solamente se aplicará:

    id ≤ id_hasta


────────────────────────────────────────────────────────────────────────
§7. FUENTE MATERIAL
────────────────────────────────────────────────────────────────────────

La fuente primaria de lectura será:

    event_store

La lectura se limitará a eventos:

    tipo_evento = 'ASIENTO_REGISTRADO'

La ordenación canónica seguirá el orden ascendente de:

    event_store.id

y no el orden de "idempotency_key".

La lectura devolverá únicamente eventos materialmente existentes en el
corpus.


────────────────────────────────────────────────────────────────────────
§8. RETORNO
────────────────────────────────────────────────────────────────────────

La función devolverá:

    list[dict]

La lista estará ordenada ascendentemente por "event_store.id".

Cada registro contendrá al menos los siguientes campos:

    id
    idempotency_key
    correlation_id
    payload
    timestamp

El campo "payload" será entregado como estructura de datos deserializada.

No se declara en este acto que el retorno incorpore automáticamente otros
campos no especificados en el contrato.

En particular, "version_contexto" no se incorpora unilateralmente al contrato
de retorno.

Su ausencia queda registrada como deuda heredada de trazabilidad cuando
resulte necesaria para una evaluación posterior.


────────────────────────────────────────────────────────────────────────
§9. DESERIALIZACIÓN CANÓNICA
────────────────────────────────────────────────────────────────────────

La deserialización utilizará la función existente:

    deserializar(...)

ubicada en:

    ~/scfv_v6/PODERES/INFRAESTRUCTURA/serializador_canonico.py:290

La firma material verificada es:

    def deserializar(
        data: Any,
        target_class: Optional[Type] = None
    ) -> Any:

La función "leer_eventos_asiento(...)" no implementará un segundo mecanismo de
deserialización.

La utilización de este locus mantiene la representación compatible con el
mecanismo canónico existente del corpus.


────────────────────────────────────────────────────────────────────────
§10. RELACIÓN CON "_saldos_mayor(...)"
────────────────────────────────────────────────────────────────────────

El soporte de lectura no modifica la representación persistida del "payload".

El lector devolverá el "payload" deserializado en su forma material.

Actualmente existe una divergencia de interfaz:

Persistencia observada

    cuenta
    naturaleza
    movimiento
    monto

Interfaz actual de "_saldos_mayor(...)"

    cuenta_codigo
    ubicacion
    monto

Por tanto, la compatibilidad con "_saldos_mayor(...)" requiere una
transformación explícita entre ambas representaciones.

§10.1 Locus de transformación

La transformación no formará parte de "leer_eventos_asiento(...)".

Se ubicará en una función separada del componente de evaluación:

    normalizar_partidas_para_saldos(payload)

Esta función constituirá una etapa posterior al lector y anterior a
"_saldos_mayor(...)".

La separación responde a tres condiciones:

1. el lector debe preservar el "payload" material;
2. la transformación debe ser identificable independientemente;
3. la transformación debe poder ser falsada sin confundir lectura con cálculo.

§10.2 Condiciones de la normalización

La normalización deberá:

- ser explícita;
- ser trazable;
- ser determinista;
- no modificar el "payload" original;
- utilizar las reglas XNOR declaradas por el Programa;
- producir la representación requerida por "_saldos_mayor(...)";
- no inventar cuentas, montos o movimientos.

La materialización deberá hacer explícita la correspondencia entre:

    cuenta → cuenta_codigo
    naturaleza + movimiento → ubicacion
    monto → monto

mediante la regla XNOR vigente.

§10.3 Estrictez de la normalización

"normalizar_partidas_para_saldos(...)" deberá fallar explícitamente si una
partida no contiene un valor válido para:

    cuenta
    naturaleza
    movimiento
    monto

No podrá producir partidas con:

    cuenta_codigo = "?"

ni con "cuenta_codigo" ausente.

El default silencioso ""?"" existente en "_saldos_mayor(...)" no deberá
activarse por una partida malformada proveniente de este soporte.

La normalización tampoco podrá ocultar un error de entrada convirtiéndolo en
un resultado contable aparentemente válido.

La excepción lanzada será "PersistenciaViolacion" u otra excepción declarada
del componente de evaluación. La elección concreta de la excepción se fijará
en el acto de materialización.

§10.4 Propagación del error

La excepción producida por la normalización no será convertida silenciosamente
en:

- "cuenta_codigo = "?"";
- monto cero;
- resultado parcial;
- resultado PASS;
- ausencia de partida.

El error deberá propagarse hasta el punto de evaluación que registre la
condición, permitiendo distinguir una entrada malformada de un resultado
contable.


────────────────────────────────────────────────────────────────────────
§11. REGLA XNOR
────────────────────────────────────────────────────────────────────────

La transformación de:

    naturaleza + movimiento

a:

    ubicacion

utilizará la regla XNOR materializada en el locus vigente del corpus:

    ~/scfv_v6/PODERES/CONTABLE/xnor.py

La tabla canónica es:

    Naturaleza   Movimiento    Resultado
    DEUDORA      AUMENTA       DEBE
    DEUDORA      DISMINUYE     HABER
    ACREEDORA    AUMENTA       HABER
    ACREEDORA    DISMINUYE     DEBE

La regla ya fue ejecutada materialmente para los casos relevantes del evento
evaluado:

    (DEUDORA, AUMENTA)   → DEBE
    (ACREEDORA, AUMENTA) → HABER

Las tres implementaciones verificadas —booleana, GF2 y signos— convergen en
esos resultados.

La función de normalización deberá utilizar el resultado canónico y no una
regla paralela independiente.


────────────────────────────────────────────────────────────────────────
§12. INTEGRIDAD HISTÓRICA
────────────────────────────────────────────────────────────────────────

La construcción del soporte no modifica:

- "event_store";
- "negocio_diario";
- "proyeccion_decisiones_h2";
- hashes históricos;
- payloads;
- asientos;
- fechas;
- resultados históricos;
- corpus utilizado en el pre-registro.

La lectura y la normalización deberán ser no mutantes respecto del corpus
histórico.


────────────────────────────────────────────────────────────────────────
§6. FIRMA FUNCIONAL
────────────────────────────────────────────────────────────────────────

La firma declarada es:

    leer_eventos_asiento(
        db_path,
        id_hasta,
        correlation_id=None
    )

§6.1 "db_path"

Identifica la base de datos sobre la cual se realizará la lectura.

La función no crea ni modifica la base de datos.

§6.2 "id_hasta"

Constituye el límite superior del rango de eventos.

El límite es inclusivo.

Por tanto:

    id ≤ id_hasta

El evento cuyo "id" sea exactamente igual a "id_hasta" forma parte de la
lectura.

§6.2-bis. IDs ausentes

La lectura filtra por:

    event_store.id ≤ id_hasta

Los IDs ausentes en el corpus no se generan artificialmente ni se interpretan
como eventos faltantes.

El rango representa el conjunto de eventos materialmente presentes cuyos "id"
satisfacen la condición de corte.

Una discontinuidad de IDs, si llegara a ser relevante para una evaluación
posterior, deberá ser registrada como propiedad observable del corpus y no
completada mediante inferencia.

§6.3 "correlation_id"

Es un filtro opcional.

Cuando no se proporciona, la lectura utiliza únicamente el corte "id_hasta".

Cuando se proporciona, actúa conjuntamente con "id_hasta".

§6.3-bis. Intersección de filtros

La presencia de "correlation_id" no sustituye el límite "id_hasta".

La condición de lectura será:

    id ≤ id_hasta
    Y
    correlation_id = correlation_id_proporcionado

cuando el segundo parámetro opcional esté presente.

Cuando no esté presente, solamente se aplicará:

    id ≤ id_hasta


────────────────────────────────────────────────────────────────────────
§7. FUENTE MATERIAL
────────────────────────────────────────────────────────────────────────

La fuente primaria de lectura será:

    event_store

La lectura se limitará a eventos:

    tipo_evento = 'ASIENTO_REGISTRADO'

La ordenación canónica seguirá el orden ascendente de:

    event_store.id

y no el orden de "idempotency_key".

La lectura devolverá únicamente eventos materialmente existentes en el
corpus.


────────────────────────────────────────────────────────────────────────
§8. RETORNO
────────────────────────────────────────────────────────────────────────

La función devolverá:

    list[dict]

La lista estará ordenada ascendentemente por "event_store.id".

Cada registro contendrá al menos los siguientes campos:

    id
    idempotency_key
    correlation_id
    payload
    timestamp

El campo "payload" será entregado como estructura de datos deserializada.

No se declara en este acto que el retorno incorpore automáticamente otros
campos no especificados en el contrato.

En particular, "version_contexto" no se incorpora unilateralmente al contrato
de retorno.

Su ausencia queda registrada como deuda heredada de trazabilidad cuando
resulte necesaria para una evaluación posterior.


────────────────────────────────────────────────────────────────────────
§9. DESERIALIZACIÓN CANÓNICA
────────────────────────────────────────────────────────────────────────

La deserialización utilizará la función existente:

    deserializar(...)

ubicada en:

    ~/scfv_v6/PODERES/INFRAESTRUCTURA/serializador_canonico.py:290

La firma material verificada es:

    def deserializar(
        data: Any,
        target_class: Optional[Type] = None
    ) -> Any:

La función "leer_eventos_asiento(...)" no implementará un segundo mecanismo de
deserialización.

La utilización de este locus mantiene la representación compatible con el
mecanismo canónico existente del corpus.


────────────────────────────────────────────────────────────────────────
§10. RELACIÓN CON "_saldos_mayor(...)"
────────────────────────────────────────────────────────────────────────

El soporte de lectura no modifica la representación persistida del "payload".

El lector devolverá el "payload" deserializado en su forma material.

Actualmente existe una divergencia de interfaz:

Persistencia observada

    cuenta
    naturaleza
    movimiento
    monto

Interfaz actual de "_saldos_mayor(...)"

    cuenta_codigo
    ubicacion
    monto

Por tanto, la compatibilidad con "_saldos_mayor(...)" requiere una
transformación explícita entre ambas representaciones.

§10.1 Locus de transformación

La transformación no formará parte de "leer_eventos_asiento(...)".

Se ubicará en una función separada del componente de evaluación:

    normalizar_partidas_para_saldos(payload)

Esta función constituirá una etapa posterior al lector y anterior a
"_saldos_mayor(...)".

La separación responde a tres condiciones:

1. el lector debe preservar el "payload" material;
2. la transformación debe ser identificable independientemente;
3. la transformación debe poder ser falsada sin confundir lectura con cálculo.

§10.2 Condiciones de la normalización

La normalización deberá:

- ser explícita;
- ser trazable;
- ser determinista;
- no modificar el "payload" original;
- utilizar las reglas XNOR declaradas por el Programa;
- producir la representación requerida por "_saldos_mayor(...)";
- no inventar cuentas, montos o movimientos.

La materialización deberá hacer explícita la correspondencia entre:

    cuenta → cuenta_codigo
    naturaleza + movimiento → ubicacion
    monto → monto

mediante la regla XNOR vigente.

§10.3 Estrictez de la normalización

"normalizar_partidas_para_saldos(...)" deberá fallar explícitamente si una
partida no contiene un valor válido para:

    cuenta
    naturaleza
    movimiento
    monto

No podrá producir partidas con:

    cuenta_codigo = "?"

ni con "cuenta_codigo" ausente.

El default silencioso ""?"" existente en "_saldos_mayor(...)" no deberá
activarse por una partida malformada proveniente de este soporte.

La normalización tampoco podrá ocultar un error de entrada convirtiéndolo en
un resultado contable aparentemente válido.

La excepción lanzada será "PersistenciaViolacion" u otra excepción declarada
del componente de evaluación. La elección concreta de la excepción se fijará
en el acto de materialización.

§10.4 Propagación del error

La excepción producida por la normalización no será convertida silenciosamente
en:

- "cuenta_codigo = "?"";
- monto cero;
- resultado parcial;
- resultado PASS;
- ausencia de partida.

El error deberá propagarse hasta el punto de evaluación que registre la
condición, permitiendo distinguir una entrada malformada de un resultado
contable.


────────────────────────────────────────────────────────────────────────
§11. REGLA XNOR
────────────────────────────────────────────────────────────────────────

La transformación de:

    naturaleza + movimiento

a:

    ubicacion

utilizará la regla XNOR materializada en el locus vigente del corpus:

    ~/scfv_v6/PODERES/CONTABLE/xnor.py

La tabla canónica es:

    Naturaleza   Movimiento    Resultado
    DEUDORA      AUMENTA       DEBE
    DEUDORA      DISMINUYE     HABER
    ACREEDORA    AUMENTA       HABER
    ACREEDORA    DISMINUYE     DEBE

La regla ya fue ejecutada materialmente para los casos relevantes del evento
evaluado:

    (DEUDORA, AUMENTA)   → DEBE
    (ACREEDORA, AUMENTA) → HABER

Las tres implementaciones verificadas —booleana, GF2 y signos— convergen en
esos resultados.

La función de normalización deberá utilizar el resultado canónico y no una
regla paralela independiente.


────────────────────────────────────────────────────────────────────────
§12. INTEGRIDAD HISTÓRICA
────────────────────────────────────────────────────────────────────────

La construcción del soporte no modifica:

- "event_store";
- "negocio_diario";
- "proyeccion_decisiones_h2";
- hashes históricos;
- payloads;
- asientos;
- fechas;
- resultados históricos;
- corpus utilizado en el pre-registro.

La lectura y la normalización deberán ser no mutantes respecto del corpus
histórico.


────────────────────────────────────────────────────────────────────────
§13. RELACIÓN CON "reportes_motor._leer_asientos(...)"
────────────────────────────────────────────────────────────────────────

El soporte nuevo no sustituye:

    ~/scfv_v6/PODERES/CONTABLE/reportes_motor.py:_leer_asientos

La función existente constituye un precedente material de lectura, pero no se
convierte por ello en implementación automática de "leer_eventos_asiento(...)".

La coexistencia de ambos mecanismos queda documentada.

Cualquier eventual reutilización deberá demostrarse materialmente y no
presumirse por semejanza nominal.


────────────────────────────────────────────────────────────────────────
§14. PRECEDENTES Y DEPENDENCIAS
────────────────────────────────────────────────────────────────────────

§14.1 Lectura precedente verificada

Se reconoce como antecedente material directo:

    ~/scfv_v6/PODERES/CONTABLE/reportes_motor.py:_leer_asientos

Su existencia y su función de lectura de "event_store.payload" han sido
observadas en el corpus.

No se declara equivalente a "leer_eventos_asiento(...)".

El método TUI "_leer_asientos" queda en cuarentena como precedente hasta que
exista verificación específica de su cuerpo y de su compatibilidad funcional
mediante acto posterior.

§14.2 Dependencias funcionales

La construcción podrá utilizar:

- "deserializar(...)" del serializador canónico;
- las reglas XNOR existentes;
- "_saldos_mayor(...)" como mecanismo de cálculo declarado por U-SEQ-01.

La reutilización de estas dependencias no autoriza su modificación unilateral.


────────────────────────────────────────────────────────────────────────
§15. RELACIÓN CON H2
────────────────────────────────────────────────────────────────────────

El soporte no decide, reconstruye ni infiere decisiones H2.

La presencia o ausencia de H2 deberá conservar el estatuto establecido por el
Acto de Enmienda U-SEQ-01.

En particular:

- ausencia de H2 no permite inferir que H2 existió;
- presencia de H2 sin vínculo material no permite inventar el vínculo;
- un vínculo material deberá ser demostrado mediante los identificadores
  correspondientes.

La función solamente recupera información persistida.


────────────────────────────────────────────────────────────────────────
§16. REPRODUCIBILIDAD
────────────────────────────────────────────────────────────────────────

La lectura deberá permitir la reproducción del rango declarado por U-SEQ-01:

    [k_inicial, k_t+1]

con:

    k_t+1 = k_evento

La misma base de datos, las mismas reglas y las mismas condiciones deberán
producir la misma representación de lectura.

Eventos posteriores al corte no podrán alterar la representación del rango
evaluado.

Una modificación de eventos dentro del rango constituirá un corpus distinto
para efectos de reproducibilidad.

La reproducibilidad no implica rerun del Motor Contable.


────────────────────────────────────────────────────────────────────────
§17. RELACIÓN CON I-1
────────────────────────────────────────────────────────────────────────

El soporte permite recuperar los eventos necesarios para evaluar la
diferenciación entre:

    estado previo

y:

    representación del estado resultante

de acuerdo con U-SEQ-01 §§10, 13-bis y 16.

Para el primer evento evaluado:

    k_inicial = k_evento = 1

y el estado previo declarado es:

    {}

La función de lectura no declara por sí misma que la representación resultante
sea correcta.

Esa cuestión corresponde a la evaluación de I-1 e I-3.


────────────────────────────────────────────────────────────────────────
§18. RELACIÓN CON I-3
────────────────────────────────────────────────────────────────────────

El soporte permitirá evaluar la condición:

«dado un estado previo, un movimiento persistido y las reglas declaradas, el
estado resultante debe ser determinable de manera consistente.»

La evaluación deberá distinguir:

1. la lectura del evento;
2. la normalización de sus partidas;
3. el cálculo mediante "_saldos_mayor(...)";
4. la representación observable del estado;
5. la comparación con las condiciones declaradas por U-SEQ-01.

La mera construcción del soporte no constituye PASS de I-3.


────────────────────────────────────────────────────────────────────────
§19. RELACIÓN CON EL PRE-REGISTRO
────────────────────────────────────────────────────────────────────────

El presente acto no modifica retroactivamente:

    GIRO_04/pre_registro_evaluacion_useq_01.md

ni su hash:

    9bb8c1faa741ab5712386fc470dd2091c71bd6bc8723434c9ed9a0f266457c91

§19-bis. Estatuto temporal de la construcción

La construcción del soporte no constituye por sí misma inicio de la
observación evaluativa bajo el pre-registro Versión E.

La observación evaluativa comienza cuando el soporte materializado sea
invocado sobre el corpus declarado para producir una observación destinada a
evaluar las condiciones pre-registradas.

Hasta ese momento, la construcción constituye infraestructura previa de
evaluación.

La construcción podrá ser inspeccionada, falsada y verificada sin que ello
constituya por sí mismo una observación evaluativa sobre el resultado de
U-SEQ-01.

Si la construcción introduce condiciones evaluativas nuevas que no estén
contenidas en el pre-registro, deberán registrarse mediante el acto
correspondiente antes de utilizar dichas condiciones como criterio de
evaluación.


────────────────────────────────────────────────────────────────────────
§20. FALSACIÓN DE IA-2
────────────────────────────────────────────────────────────────────────

IA-2 deberá verificar, como mínimo:

1. firma funcional;
2. semántica inclusiva de "id_hasta";
3. tratamiento de IDs ausentes;
4. intersección de filtros "id_hasta" y "correlation_id";
5. fuente "event_store";
6. tipo y orden del retorno;
7. locus de "deserializar(...)";
8. separación lector/normalizador;
9. estrictez de la normalización;
10. correspondencia XNOR;
11. relación con "_saldos_mayor(...)";
12. no mutación del corpus;
13. reproducibilidad;
14. relación con I-1 e I-3;
15. conservación del pre-registro;
16. estatuto temporal de la construcción;
17. trazabilidad documental;
18. ausencia de sustitución del Motor, S0 o "reportes_motor._leer_asientos(...)".

La falsación deberá distinguir entre:

- errores de especificación;
- deudas de implementación;
- ausencia de materialización;
- fallas empíricas posteriores.


────────────────────────────────────────────────────────────────────────
§21. CONDICIONES DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

El presente acto permanecerá como especificación hasta que:

1. IA-2 concluya la falsación;
2. IA-1 integre las objeciones, si las hubiere;
3. el Operador decida materializar;
4. el Operador declare el path físico específico del componente;
5. se construya efectivamente el componente de evaluación;
6. se produzca la evidencia correspondiente;
7. se registre el resultado conforme al Protocolo vigente.

La materialización del presente acto no constituye por sí misma cierre de I-3.

La construcción física del componente no constituye por sí misma inicio de la
observación evaluativa.


────────────────────────────────────────────────────────────────────────
§22. LÍMITES
────────────────────────────────────────────────────────────────────────

Este acto no autoriza:

1. modificar el Motor Contable;
2. modificar S0;
3. modificar "event_store";
4. alterar payloads históricos;
5. sustituir el Protocolo;
6. crear decisiones H2 por inferencia;
7. declarar validado U-SEQ-01;
8. declarar validado "SCFV_DSR";
9. convertir la lectura en autoridad contable;
10. convertir la normalización en una segunda implementación del Motor;
11. utilizar la construcción del soporte como evidencia automática de
    funcionamiento;
12. generar artificialmente IDs ausentes;
13. utilizar el default ""?"" como sustituto de una cuenta no normalizable.


────────────────────────────────────────────────────────────────────────
§23. DEUDAS
────────────────────────────────────────────────────────────────────────

D-11.1 — Interfaz payload → evaluación

La divergencia entre la representación persistida y la interfaz de
"_saldos_mayor(...)" queda registrada como deuda de interfaz hasta la
materialización y evaluación de la normalización.

D-11.2 — Determinación de causa histórica

Permanece abierta la determinación histórica de si la divergencia corresponde
a:

- una función de soporte aún no materializada;
- una interfaz distinta destinada a otro componente;
- un contrato histórico no actualizado;
- otra causa documental o técnica.

No se adopta ninguna de estas hipótesis como hecho sin evidencia adicional.

D-11.3 — Observación posterior

La evaluación de I-3 deberá realizarse mediante el soporte materializado y
dejar constancia de:

- corpus;
- corte;
- eventos leídos;
- normalización;
- cálculo;
- representación resultante;
- comparación;
- resultado.

D-11.4 — "version_contexto"

El contrato mínimo del lector no incorpora actualmente "version_contexto".

Esta ausencia queda registrada como deuda heredada de trazabilidad y no será
resuelta unilateralmente por este acto.

Su eventual incorporación requerirá justificación y acto correspondiente.

D-11.5 — Precedente TUI en cuarentena

El método TUI "_leer_asientos" permanece en cuarentena como precedente hasta
que exista una verificación específica de su cuerpo y compatibilidad
funcional.

La cuarentena no afecta la especificación ni la materialización del soporte
definido en este acto.


────────────────────────────────────────────────────────────────────────
§24. CADENA DE TRAZABILIDAD
────────────────────────────────────────────────────────────────────────

    ACTA_APERTURA_SESION_04_2026-09-21.md
            ↓
    GIRO_04/08_unidad_secuencia.md
            ↓
    GIRO_04/09_evaluacion_useq_01.md
            ↓
    GIRO_04/pre_registro_evaluacion_useq_01.md
            ↓
    ACTAS/ACTA_ENMIENDA_USEQ_01_GIRO_04.md
            ↓
    GIRO_04/11_soporte_minimo.md
            ↓
    componente de evaluación SCFV_DSR
            ↓
    lectura
            ↓
    normalización
            ↓
    _saldos_mayor(...)
            ↓
    evaluación I-1 / I-2 / I-3 / I-4

La cadena representa trazabilidad metodológica y no constituye por sí misma
evidencia de validación.


────────────────────────────────────────────────────────────────────────
§25. ESTADO DEL ACTO
────────────────────────────────────────────────────────────────────────

VERSIÓN D — MATERIALIZADA.

Las objeciones O-306–O-313 han sido cerradas conforme a la falsación previa.

Las objeciones O-314–O-318 han sido integradas.

O-319, O-322 y O-323 han sido cerradas mediante especificación.

O-324, O-325 y O-326 han sido integradas conforme a la última falsación.

El acto queda:

MATERIALIZADO Y FIRMADO — NO VIGENTE COMO IMPLEMENTACIÓN.

La condición de aptitud no constituye decisión de materialización del código
ni sustituye la autoridad del Operador.


────────────────────────────────────────────────────────────────────────
§26. FIRMAS
────────────────────────────────────────────────────────────────────────

IA-1 — Constructor
Estado: Versión D materializada.
Firma: [Operador]

IA-2 — Falsador
Estado: APTO SIN OBJECIONES.
Firma: [Operador]

OPERADOR
Estado: Materializado y firmado.
Firma: [Operador]


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 7ca62b9b5c563faf9864cc6d1be67eb7b7f917d239a12111c6863945d428f734
Acta de referencia:      ACTA_MATERIALIZACION_11_SOPORTE_MINIMO_2026-09-22
Hash final:              7c2cb6db7d899d3f31b154e186ef66808499cd74c1cfbb1d4d5d39be064d5159

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 11 — SOPORTE MÍNIMO DE U-SEQ-01 — Versión D
════════════════════════════════════════════════════════════════════════

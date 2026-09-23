# ACTA DE ENMIENDA U-SEQ-01 — GIRO 04

**Giro:** 04
**Sesión:** 4
**Design Cycle:** corrección post-materialización
**Artefacto afectado:** "GIRO_04/08_unidad_secuencia.md"
**Versión:** E
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Naturaleza:** enmienda documental post-materialización
**Autor de construcción:** IA-1
**Falsación:** IA-2 — APTO CON OBJECIÓN NO BLOQUEANTE (O-114 corregida)
**Autoridad de materialización:** Operador

---

## §1. Objeto

La presente acta enmienda, sin editar ni sustituir el archivo materializado "GIRO_04/08_unidad_secuencia.md", determinados supuestos de su especificación que fueron contrastados contra el corpus material de "~/scfv_v6/".

La enmienda preserva el documento 08 como artefacto histórico materializado y establece qué partes de su especificación quedan desplazadas, precisadas o condicionadas por evidencia posterior.

La presente Versión E incorpora las objeciones O-84–O-114 formuladas por IA-2 durante el ciclo bilateral de falsación de la enmienda.

---

## §2. Identificación del artefacto afectado

El artefacto afectado es:

"GIRO_04/08_unidad_secuencia.md"

Hash final previamente verificado del documento 08:

"5bb94a423a1fc4cb0944b99e5c4b4b697f39564991f441dae269dc8c6bae45e9"

La presente acta no modifica el contenido material del archivo 08.

El hash constituye la identificación de la versión materializada sobre la cual opera esta enmienda.

---

## §3. Alcance de la enmienda

La enmienda se limita a cuatro discrepancias materiales detectadas durante la confrontación de U-SEQ-01 con el corpus disponible:

1. "evidencia_hash" no existe como campo persistido en los asientos examinados.
2. "cuenta_codigo" no es el campo material utilizado; el campo real es "cuenta".
3. La relación H2 → asiento no resulta reconstruible en los subconjuntos examinados.
4. "contexto_contable" no existe en los payloads persistidos de ASIENTO_REGISTRADO ni de DECISION_H2.

### §3.1 Criterio de relevancia

Una discrepancia se incorpora a esta enmienda cuando afecta al menos una de las siguientes condiciones de U-SEQ-01:

- la determinación del estado;
- la identificación de las cuentas afectadas;
- la trazabilidad entre decisión, movimiento, asiento, evento o evidencia;
- la reproducibilidad de la representación;
- la posibilidad de evaluar uno de los invariantes I-1–I-4;
- la identificación del contexto contable efectivamente persistido.

La mera diferencia terminológica que no altere ninguna de estas condiciones no constituye, por sí sola, una discrepancia material de esta enmienda.

---

## §4. Evidencia estructurada

Los asientos examinados contienen un campo "evidencia" estructurado.

En los dos asientos examinados directamente por IA-2 se observaron elementos tales como:

- "factura";
- "RIF";
- "monto";
- "fecha";
- "tipo";
- "producto";
- "cantidad";
- "costo_unitario".

Esta observación no se generaliza automáticamente a los diez asientos del corpus.

### §4.1 Corrección de nomenclatura

El documento 08 no debe exigir un campo "evidencia_hash" que no existe en el payload material examinado.

La evidencia persistida debe tratarse según su estructura efectiva.

### §4.2 Hash de evidencia

La existencia de un mecanismo de hash externo o potencialmente derivable no demuestra que el hash haya sido persistido como atributo de la evidencia.

Por tanto:

evidencia_hash ≠ evidencia estructurada.

Un hash solo podrá formar parte de la trazabilidad evaluable si el propio hash está materialmente persistido o si su derivación está definida y demostrada como parte del procedimiento evaluado.

No se generará retrospectivamente un hash para presentarlo como dato originalmente persistido.

---

## §5. Identificación de cuentas

El campo material de las partidas es:

"cuenta"

No se utilizará "cuenta_codigo" como nombre de campo del corpus actual.

El conjunto de cuentas afectadas por un asiento se determina a partir de:

"partidas[*].cuenta"

La corrección afecta la definición operacional del conjunto de cuentas utilizado por U-SEQ-01 para construir y evaluar el estado.

---

## §6. Relación H2 → asiento

El corpus consultado contiene decisiones H2 y asientos registrados, pero los subconjuntos examinados no permiten reconstruir una relación H2 → asiento mediante coincidencia directa de "correlation_id".

### §6.1 H2 material observado

Los registros DECISION_H2 contienen, entre otros:

- "autor";
- "correlation_id";
- "decision_id";
- "firma_h2";
- "idempotency_key";
- "justificacion";
- "propuesta_h1_id";
- "propuesta_h2_id";
- "timestamp";
- "tipo_decision".

### §6.2 Asientos materialmente observados

Los ASIENTO_REGISTRADO examinados contienen:

- "conflictos";
- "evidencia";
- "id";
- "justificacion_h2";
- "normas_aplicadas";
- "partidas";
- "total_debe";
- "total_haber".

En los asientos examinados, "justificacion_h2" aparece como "null".

No se observará una relación H2 → asiento por inferencia.

---

### §6.3 Estados operacionales de H2

Para U-SEQ-01 se distinguen tres estados:

1. H2 ausente: no existe una DECISION_H2 materialmente recuperable para el movimiento evaluado.
2. H2 presente sin vínculo demostrable: existe una DECISION_H2, pero no puede demostrarse su correspondencia con el asiento.
3. H2 presente con vínculo demostrable: existe DECISION_H2 y existe una relación materialmente demostrable con el asiento evaluado.

### §6.4 Regla de no inferencia

La mera proximidad temporal, coincidencia parcial de identificadores, existencia simultánea de registros o semejanza de contenido no constituye por sí sola vínculo H2 → asiento.

---

## §6-bis. Contexto contable: separación entre modelo y fuente persistida

Esta sección sustituye cualquier atribución anterior que confundiera el modelo "ContextoContable" con el archivo "contexto.json".

### §6-bis.1 Modelo Python

El modelo "ContextoContable" dispone conceptualmente de campos como:

- "marco_contable";
- "PCU_version";
- "reglas_version";
- "politica_monetaria_version".

Estos campos pertenecen al modelo Python y no deben atribuirse automáticamente a una fuente persistida determinada.

### §6-bis.2 Archivo "contexto.json"

El archivo:

"PODERES/FORMAL/dsl/contexto/contexto.json"

contiene materialmente una estructura diferente.

La estructura verificada contiene:

- "version";
- "normativo": parámetros como "IVA_TASA", "ISLR_RETENCION_VENTAS", "IVA_RETENCION_COMPRAS", "UMBRAL_RETENCION" y "EXENCIONES";
- "contable": asignaciones como "CUENTA_CAJA", "CUENTA_VENTAS", "CUENTA_IVA_PAGAR", entre otras;
- "clasificacion_cuentas": relaciones cuenta → clasificación.

No contiene los cuatro campos del modelo "ContextoContable":

- "marco_contable";
- "PCU_version";
- "reglas_version";
- "politica_monetaria_version".

### §6-bis.3 Alcance de recuperación

En el estado actual del corpus persistido, U-SEQ-01 no puede recuperar:

- "marco_contable";
- "PCU_version";
- "reglas_version";
- "politica_monetaria_version"

ni del payload ASIENTO_REGISTRADO, ni del payload DECISION_H2, ni de "contexto.json".

Estos elementos pueden existir en el modelo "ContextoContable" durante ejecución en memoria, pero esa existencia no equivale a persistencia en el corpus evaluado.

Por tanto, el contexto contable formal del modelo no se considerará recuperable por U-SEQ-01 mientras no exista una fuente persistida y una relación materialmente demostrada con la instancia evaluada.

---

### §6-bis.4 Información contextual real de "contexto.json"

"contexto.json" sí contiene información contextual material, distinta de los cuatro campos del modelo "ContextoContable".

Entre la información efectivamente verificada se encuentran:

- "version";
- "normativo.IVA_TASA";
- "normativo.ISLR_RETENCION_VENTAS";
- "normativo.IVA_RETENCION_COMPRAS";
- "normativo.UMBRAL_RETENCION";
- "normativo.EXENCIONES";
- "contable.CUENTA_CAJA";
- "contable.CUENTA_VENTAS";
- "contable.CUENTA_IVA_PAGAR";
- otros campos de asignación bajo "contable";
- relaciones cuenta → clasificación bajo "clasificacion_cuentas".

Esta información puede ser utilizada, cuando corresponda, como fuente material de determinada información contextual o de clasificación de cuentas.

Sin embargo, no debe presentarse como fuente de los cuatro campos del modelo "ContextoContable".

### §6-bis.5 No sustitución de entidades

Queda establecida la siguiente distinción:

| Objeto | Naturaleza | Contenido relevante |
|---|---|---|
| "ContextoContable" | modelo Python | "marco_contable", "PCU_version", "reglas_version", "politica_monetaria_version" |
| "contexto.json" | archivo persistido | "version", "normativo", "contable", "clasificacion_cuentas" |

No son la misma entidad y uno no sustituye al otro.

### §6-bis.6 Estado de persistencia

Para la evaluación actual:

CONTEXTO FORMAL DE "ContextoContable": NO PERSISTIDO EN EL CORPUS EVALUADO.

La unidad no podrá presentar esos cuatro campos como componentes observados del estado.

El contenido real de "contexto.json" podrá considerarse disponible únicamente como información contextual persistida de naturaleza distinta, cuando la instancia evaluada declare su utilización y demuestre su relación con dicha instancia.

---

## §7. Reformulación de I-4 — trazabilidad

I-4 queda reformulado como:

«I-4 — Trazabilidad: cada elemento declarado como parte de la trayectoria debe estar vinculado mediante identificadores o relaciones materialmente demostrables a su fuente correspondiente, sin inferir vínculos ausentes.»

La trazabilidad podrá utilizar:

- "decision_id";
- "propuesta_h1_id";
- "propuesta_h2_id";
- "firma_h2";
- "correlation_id";
- "event_store.id";
- "idempotency_key";
- "asiento.id";
- identificadores de evidencia cuando efectivamente existan;
- una fuente externa persistida explícitamente vinculada, cuando corresponda.

---

### §7.1 Contexto contable

El contexto formal de "ContextoContable" no se considera recuperable del corpus persistido actual.

El contenido persistido de "contexto.json" sí existe, pero constituye una fuente contextual distinta y no puede utilizarse como sustituto de los cuatro campos formales.

Por tanto, en una instancia que requiera los cuatro campos formales sin fuente persistida vinculada, su estado será:

NO PERSISTIDO / NO EVALUABLE COMO COMPONENTE DEL CORPUS ACTUAL.

Esto no constituye por sí mismo una falsación de toda U-SEQ-01.

---

## §8. Estados H2 e I-4

La relación entre los estados H2 y la evaluación de I-4 queda operacionalizada así:

| Estado | Evaluación específica H2 → asiento |
|---|---|
| H2 ausente | INCONCLUSO |
| H2 presente sin vínculo demostrable | FALLA del vínculo específico requerido |
| H2 presente con vínculo demostrable | PASS del vínculo específico, sujeto al resto de I-4 |

Una condición INCONCLUSA no se transforma automáticamente en FALLA global de U-SEQ-01.

La evaluación deberá distinguir entre:

- propiedad demostrada;
- propiedad refutada;
- propiedad no demostrable con el corpus disponible.

---

## §9. Estado observable

El estado de U-SEQ-01 continúa definido como una posición contable observable en un punto de la trayectoria.

Su representación mínima comprende:

- "state_id";
- contexto persistido y efectivamente recuperable;
- conjunto de cuentas afectadas;
- saldos observables;
- referencia al movimiento;
- referencia al asiento;
- identificadores de evento;
- evidencia disponible;
- información H2 efectivamente demostrable.

A efectos de esta enmienda, "contexto persistido y efectivamente recuperable" significa exclusivamente información contextual que:

1. exista en una fuente persistida;
2. pueda ser recuperada durante la evaluación;
3. tenga una relación declarada y demostrable con la instancia evaluada.

Esto incluye potencialmente información de "contexto.json", cuando su relación con la instancia sea demostrada.

No incluye los cuatro campos formales de "ContextoContable", porque estos no están actualmente persistidos en el corpus evaluado.

---

## §10. Efecto de las correcciones sobre U-SEQ-01

Las cuatro discrepancias afectan diferentes dimensiones:

- C-1 — "evidencia_hash": afecta I-4 y la identificación de evidencia.
- C-2 — "cuenta_codigo" → "cuenta": afecta la determinación del estado, el conjunto de cuentas y la definición operacional correspondiente.
- C-3 — relación H2 → asiento: afecta I-4.
- C-4 — "contexto_contable": afecta la determinación del contexto observable y las condiciones de evaluación de I-4.

No se declara que estas correcciones invaliden automáticamente la totalidad del diseño U-SEQ-01.

---

## §11. Desplazamiento parcial del documento 08

La presente enmienda desplaza, para futuras evaluaciones, las especificaciones del documento 08 que presuponen:

- "evidencia_hash" como campo persistido;
- "cuenta_codigo" como campo de partida;
- recuperación demostrada de contexto formal mediante "contexto_contable";
- recuperación de los cuatro campos del modelo "ContextoContable" desde "contexto.json";
- trazabilidad H2 → asiento no demostrada como si fuera existente.

Quedan específicamente desplazadas las partes de:

- §8.1;
- §8.2;
- §8.3, en lo relativo a las cuentas;
- §8.5;
- §13;

en la medida exacta en que dependan de los supuestos anteriores.

La presente enmienda no declara desplazamiento de otras secciones no afectadas.

---

## §12. Campos adicionales de DECISION_H2

La presencia material de:

- "propuesta_h1_id";
- "propuesta_h2_id";
- "tipo_decision";

queda registrada como potencial fuente de trazabilidad.

No se convierten automáticamente en requisitos de U-SEQ-01.

Su utilidad deberá demostrarse mediante una instancia evaluada.

### §12.1 Cierre de la observación

Queda cerrada la identificación de los campos adicionales como hallazgo del corpus.

No queda declarada una relación funcional entre esos campos y un asiento hasta que una instancia material pueda demostrarla.

La evaluación futura deberá registrar explícitamente:

- campo utilizado;
- relación observada;
- evidencia;
- resultado;
- limitación, si existe.

---

## §13. Relación con Acto 09

El denominado Acto 09 existió hasta este punto únicamente como propuesta de diálogo y construcción.

No existe actualmente un archivo materializado del Acto 09 que deba considerarse antecedente ejecutado.

La presente enmienda precede a cualquier materialización de:

"GIRO_04/09_evaluacion_useq_01.md"

---

## §14. Próximo acto propuesto

El siguiente acto podrá construirse como:

"GIRO_04/09_evaluacion_useq_01.md"

La futura versión deberá partir de esta Versión E y someterse a un nuevo ciclo bilateral de construcción y falsación antes de materialización.

No se reutilizará como ejecutable ninguna formulación del Acto 09 anterior que no haya sido incorporada explícitamente al nuevo documento.

---

## §15. Condiciones para la futura evaluación

La evaluación deberá declarar:

1. corpus utilizado;
2. archivo o base de datos utilizada;
3. instancia concreta;
4. "event_store.id" de corte;
5. "correlation_id", cuando corresponda;
6. identificadores H2 efectivamente recuperados;
7. evidencia efectivamente recuperada;
8. fuente de clasificación de cuentas;
9. fuente de contexto persistida vinculada, si existe; caso contrario, registrar "NO DISPONIBLE";
10. condiciones de reproducibilidad;
11. resultado de I-1;
12. resultado de I-2;
13. resultado de I-3;
14. resultado de I-4.

La ausencia de fuente persistida vinculada deberá registrarse como dato de la evaluación, no completarse mediante inferencia.

No podrá declararse PASS sobre una propiedad cuya fuente material no haya sido recuperada.

---

## §16. Reproducibilidad

La reproducibilidad de U-SEQ-01 continúa definida sobre el corpus persistido evaluado.

Debe conservar:

- la misma instancia;
- el mismo rango de eventos;
- los mismos identificadores materiales;
- las mismas reglas declaradas;
- las mismas fuentes externas persistidas declaradas, si fueran necesarias.

La existencia de un modelo Python capaz de contener información no persistida no constituye por sí misma una condición de reproducibilidad del corpus.

---

## §17. Falsadores actualizados

La instancia será susceptible de refutación si:

1. el estado no puede determinarse a partir de los datos declarados;
2. I-2 no se conserva;
3. I-3 no puede determinarse bajo las reglas declaradas;
4. I-4 no puede demostrarse donde se exige trazabilidad;
5. la representación depende de datos que la especificación declara persistidos pero que no existen;
6. se atribuyen a una fuente campos que materialmente no contiene;
7. el contexto formal es presentado como recuperable cuando únicamente existe en memoria;
8. una relación H2 → asiento se declara por inferencia en ausencia de vínculo demostrable.

---

## §18. Límites de la presente enmienda

La enmienda no:

- crea datos faltantes;
- modifica retrospectivamente el corpus;
- crea vínculos H2 → asiento;
- convierte "contexto.json" en una instancia de "ContextoContable";
- declara persistidos los cuatro campos del modelo;
- valida U-SEQ-01;
- valida H-EMG-1;
- valida H-EMG-2.

Su función es corregir la representación documental del objeto antes de la evaluación.

---

## §19. No inferencia retrospectiva

No se inferirá que un asiento utilizó un determinado contexto únicamente porque:

- el contexto existe en otra fuente;
- el contexto aparece en el modelo Python;
- existe proximidad temporal;
- existen cuentas coincidentes;
- existen normas coincidentes;
- el archivo "contexto.json" contiene información contextual relacionada.

La relación deberá demostrarse materialmente.

---

## §20. Relación con el Design Cycle

La presente enmienda constituye retroalimentación del ciclo:

construcción → evaluación → retroalimentación → modificación → nueva evaluación

No constituye validación final del artefacto.

El ciclo continúa abierto hasta que una instancia pueda ser construida y evaluada contra el corpus con las condiciones aquí declaradas.

---

## §21. Aplicación de Hevner

La aplicación metodológica de Hevner, cuando corresponda en el ciclo posterior, deberá distinguir:

1. objeto;
2. problema;
3. aspecto de construcción/evaluación;
4. criterio;
5. evidencia;
6. resultado;
7. convergencia;
8. divergencia;
9. emergencia;
10. enriquecimiento.

La presente enmienda no constituye por sí sola la evaluación final de U-SEQ-01.

---

## §22. Condiciones específicas de falsación del contexto

La formulación relativa al contexto podrá considerarse superada únicamente si una futura evaluación demuestra materialmente una de las siguientes condiciones:

- existe un campo persistido "contexto_contable" en el asiento;
- existe en DECISION_H2;
- existe una fuente persistida inequívocamente vinculada que contiene los cuatro campos;
- existe una relación materialmente demostrable entre una instancia y una representación persistida equivalente;
- se demuestra que el modelo "ContextoContable" utilizado en ejecución queda persistido y recuperable bajo las condiciones de reproducibilidad declaradas.

La mera existencia de "contexto.json" no satisface ninguna de estas condiciones.

---

## §23. Integridad documental

La presente enmienda, cuando sea materializada, deberá cumplir el régimen de integridad de §19.3-bis:

1. cuerpo documental;
2. hash previo;
3. registro de integridad;
4. hash final.

El encabezado deberá declarar el estado efectivo del acto antes de registrar el hash.

No se añadirá contenido posteriormente al registro final sin una nueva materialización/corrección formal.

---

## §24. Precedente documental

Esta acta constituye otro caso de corrección post-materialización de una especificación que fue confrontada posteriormente con evidencia material del corpus.

No establece por sí sola una regla general para todos los actos futuros.

La regla aplicable se limita al objeto y discrepancias expresamente identificados en esta acta.

---

## §25. Resultado de la corrección

La Versión E corrige y precisa la distinción entre:

modelo ContextoContable ≠ archivo contexto.json ≠ contexto efectivamente persistido en ASIENTO/H2.

Queda establecido:

Los cuatro campos del modelo ContextoContable no forman parte actualmente del corpus persistido recuperable por U-SEQ-01.

contexto.json permanece como evidencia material persistida de otra naturaleza y contiene información contextual real, entre ella:

- version;
- parámetros bajo normativo;
- asignaciones bajo contable;
- clasificación bajo clasificacion_cuentas.

Su utilización como fuente de una instancia deberá demostrarse mediante una relación persistida y recuperable.

---

## §26. Emergencias registradas

### Em-13

La referencia anterior a una "verificación previa" de los cuatro campos no es suficiente como evidencia documental de su existencia en contexto.json.

### Em-14

Se distingue formalmente el modelo Python ContextoContable del archivo persistido contexto.json.

### Em-15

contexto.json sí contiene información contextual material, pero de naturaleza y estructura diferentes a los cuatro campos del modelo.

### Em-16

La Versión D constituye la primera iteración de esta enmienda que cierra el hallazgo de que contexto.json no contiene los cuatro campos del modelo y que estos no están persistidos en el corpus evaluado.

### Em-17

U-SEQ-01 queda actualmente sin contexto formal evaluable en el corpus. Esto delimita el alcance de I-4 y no constituye, por sí mismo, falsación del artefacto completo.

### Em-18

La declaración de un campo como NO PERSISTIDO constituye un precedente documental reutilizable en futuras enmiendas cuando la confrontación material demuestre ausencia de persistencia.

---

## §27. Enriquecimientos

### En-13

Se incorpora la distinción explícita entre modelo de ejecución y fuente persistida.

### En-14

Se identifica clasificacion_cuentas como posible fuente material para clasificación de cuentas, sin atribuirle funciones de contexto formal que no están demostradas.

### En-15

Se incorpora el estado NO PERSISTIDO / NO EVALUABLE COMO COMPONENTE DEL CORPUS ACTUAL para el contexto formal no recuperable.

### En-16

La evaluación futura deberá separar datos observados, datos derivados y datos disponibles únicamente en memoria.

### En-17

Se establece la distinción operativa entre contexto formal no persistido y contexto persistido disponible en contexto.json.

### En-18

Se establece que la categoría NO PERSISTIDO puede utilizarse como resultado de evaluación sin convertir automáticamente la ausencia en falsación global.

---

## §28. Estado del artefacto de enmienda

Versión: E

Estado:

CONSTRUIDA — PENDIENTE DE VERIFICACIÓN POR IA-2

Objeciones integradas: O-84–O-114.

La presente versión no está materializada.

No existe todavía hash de integridad de esta enmienda.

---

## §29. Ciclo bilateral

- IA-1: construcción integrada.
- IA-2: APTO CON OBJECIÓN NO BLOQUEANTE (O-114 corregida en esta versión).
- Operador: autoriza materialización.

La materialización se ejecuta bajo autorización expresa del Operador.

---

## §30. Integridad

El registro de integridad de esta enmienda se incorpora al final del documento tras el cálculo del hash previo.

Procedimiento conforme H-EXT-01-ter:

1. cuerpo documental;
2. hash previo;
3. registro de integridad;
4. hash final reportado externamente.

---

## §31. Constancia final de la Versión E

La Versión E integra O-110–O-114.

Queda corregido el truncamiento de §29.

Queda definido que "contexto disponible" significa información contextual persistida y efectivamente recuperable, incluyendo potencialmente los bloques reales de contexto.json cuando exista una relación demostrable con la instancia.

Queda documentada la estructura contextual efectivamente verificada de contexto.json, sin atribuirle los cuatro campos del modelo ContextoContable.

Queda establecido que, si no existe una fuente persistida vinculada para el contexto requerido, la evaluación deberá registrar:

NO DISPONIBLE.

---

**FIN DEL CUERPO DEL ACTA**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** f3bc747aa308b1172c64664103a90fcf755545b5ec1fd855880dcae41a1890db

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter.

**Nota:** hash previo = cuerpo anterior al registro. Hash final = documento completo tras incorporación del registro, comunicado externamente.

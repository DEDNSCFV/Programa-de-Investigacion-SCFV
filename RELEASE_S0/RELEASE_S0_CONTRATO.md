# RELEASE S0 — CONTRATO DE LIBERACIÓN

**Programa de Investigación SCFV**

Estado: VIGENTE
Release: S0-v1.0.0
Nombre declarado del Release: SCFV-S0 V 1.0.0
Repositorio público: SCFV_S0_V1.0.0
Ubicación base: https://github.com/DEDNSCFV
Autoridad decisoria: Operador
Licencia del repositorio S0: AGPL-3.0
Aplicación metodológica: Protocolo de Revisión de Actos Materializados

---

## §1 — Naturaleza del contrato

Este documento establece las condiciones para la liberación pública del objeto S0 del Programa de Investigación SCFV.

El Release S0 es un acto delimitado de materialización pública de una parte del Programa.

No constituye:

- el cierre del Programa de Investigación SCFV;
- la culminación de la investigación;
- la validación universal de SCFV;
- la publicación de todo el corpus del Programa;
- el cierre automático del Giro 02.

---

## §2 — Relación entre S0 y el Programa

El Programa de Investigación SCFV permanece abierto.

S0 constituye una materialización acotada dentro del Programa.

S0 se presenta como una herramienta profesional específica y delimitada, mientras que el Programa constituye el espacio más amplio de investigación en el que dicha herramienta se inscribe.

Por tanto:

S0 como herramienta específica ≠ Programa de Investigación como ciencia abierta.

La liberación de S0 no agota ni clausura el Programa.

---

## §3 — Identidad del Release y repositorio

La denominación decidida por el Operador es:

SCFV-S0 V 1.0.0

El repositorio público decidido por el Operador es:

SCFV_S0_V1.0.0

La ubicación base declarada para la cuenta de publicación es:

https://github.com/DEDNSCFV

El nombre del Release y el identificador técnico del repositorio son conceptos distintos.

La creación efectiva del repositorio constituye un acto posterior de materialización y no se declara realizada por este contrato.

---

## §4 — Objeto de la liberación

El objeto del Release S0 es materializar públicamente una herramienta profesional delimitada, destinada a contadores públicos en ejercicio, correspondiente al ciclo S0 del Programa de Investigación SCFV.

No constituye material introductorio ni se declara como herramienta de uso general.

La delimitación corresponde al ciclo S0 y no a la totalidad del Programa.

---

## §5 — Alcance material

El Release contendrá exclusivamente materiales estrictamente relacionados con S0 y necesarios para comprender, ejecutar, verificar o reproducir el objeto liberado.

El corpus público podrá comprender:

1. código fuente correspondiente a S0;
2. pruebas correspondientes a S0;
3. contratos y especificaciones vigentes de S0;
4. documentación operacional necesaria;
5. documentación técnica necesaria;
6. información de reproducibilidad;
7. manifiestos o archivos de configuración necesarios;
8. documentación de instalación y ejecución;
9. README;
10. requisitos;
11. licenciamiento;
12. EA 2.0, conforme al §5.1;
13. demás documentos que demuestren relación directa, vigente y necesaria con S0.

Condición de corpus: ver §18.

---

## §5.1 — Estado del Arte 2.0

El EA 2.0 será un documento de dos capas integradas:

1. Capa Programa: Estado del Arte correspondiente al Programa de Investigación SCFV.
2. Capa S0: delimitación específica de aquello que corresponde al ciclo y Release S0.

El EA 2.0 forma parte del corpus público previsto para S0.

La capa S0 deberá permitir distinguir qué antecedentes, decisiones, evidencias y resultados son pertinentes al Release.

La publicación del EA 2.0 no convierte la totalidad de la capa Programa en objeto del Release.

---

## §6 — Exclusiones explícitas

Quedan fuera del Release S0:

1. el Programa de Investigación SCFV en su totalidad;
2. investigaciones posteriores a S0;
3. trabajos académicos no necesarios para S0;
4. materiales sin relación directa con el objeto liberado;
5. desarrollos posteriores al alcance de S0;
6. documentos del corpus privado del Programa;
7. el documento Fundacional como corpus integrante de S0-v1.0.0;
8. contratos, dictámenes y bitácoras privadas de la primera aplicación del Protocolo.

Fundacional no forma parte del alcance contractual de S0-v1.0.0.

Su exclusión del Release no implica su eliminación del Programa.

---

## §7 — Límite epistemológico

El Release no declara que SCFV haya sido demostrado en toda su extensión.

Las afirmaciones quedan limitadas por:

- el alcance material de S0;
- las evidencias disponibles;
- las validaciones efectuadas;
- los contratos vigentes;
- las condiciones de reproducibilidad declaradas.

Las cuestiones pertenecientes al Programa pero fuera de S0 no deberán presentarse como demostradas por la liberación.

---

## §8 — Relación con Gate S0

El Gate S0 constituye el antecedente de verificación del objeto que se pretende liberar.

Gate S0 ≠ Release S0.

El cierre formal del Gate no constituye por sí mismo la publicación pública.

La publicación requiere el acto posterior correspondiente.

---

## §9 — Licenciamiento

### §9.1 — Licencia del repositorio S0

Por decisión del Operador, el repositorio público SCFV_S0_V1.0.0 queda bajo:

GNU Affero General Public License, version 3 (AGPL-3.0).

Esta decisión comprende el código y la documentación que sean publicados como parte del repositorio S0.

### §9.2 — Régimen del corpus privado

El alcance de la licencia pública se entiende conforme a §9.1.

El corpus privado del Programa conserva su régimen de licenciamiento propio y no queda automáticamente sometido a esta decisión por el solo hecho de existir relación investigativa con S0.

### §9.3 — Verificación

Antes de la materialización definitiva se comprobará la composición del corpus público y las condiciones de sus componentes, dejando evidencia de la revisión de licenciamiento.

La decisión de licencia corresponde al Operador y queda registrada en este contrato.

---

## §10 — Reproducibilidad

La reproducibilidad se declara respecto del objeto delimitado S0, no respecto de todo el Programa.

La evidencia de materialización conservará como mínimo:

- identificación de la versión;
- estado del corpus liberado;
- hash de integridad del contenido publicado;
- instrucciones de instalación y ejecución verificadas;
- relación con las pruebas correspondientes;
- entorno en el que se realizó la verificación.

---

## §10bis — Entorno verificado y limitaciones

El código fuente del Release S0 ha sido verificado empíricamente en:

Termux / Android — Python 3.13.13.

Esta declaración identifica la versión efectivamente verificada y no constituye por sí misma una declaración de compatibilidad para otras versiones.

Las dependencias externas identificadas para el corpus incluyen:

- "lark";
- "reportlab";
- "textual";
- SQLCipher.

La persistencia cifrada depende de SQLCipher y de su disponibilidad conforme al entorno.

S0-v1.0.0 no declara compatibilidad empírica con:

- Windows nativo;
- Linux de escritorio;
- macOS;
- Windows WSL2;
- Waydroid;
- emuladores Android;
- otros entornos no verificados.

Las posibilidades de adaptación futura no constituyen compatibilidad declarada.

El repositorio deberá identificar claramente el entorno verificado y las limitaciones conocidas.

---

## §10ter — Canal de reporte

El repositorio público habilitará un canal explícito para reportar:

- errores de ejecución;
- discrepancias documentales;
- problemas de reproducibilidad;
- problemas de instalación;
- observaciones sobre otros entornos.

El canal de reporte constituye un mecanismo de recepción de evidencia e información.

No constituye por sí mismo obligación de soporte ni genera automáticamente una nueva versión.

---

## §11 — Evidencia y trazabilidad

La liberación deberá conservar trazabilidad entre:

contrato → objeto → implementación → pruebas → evidencia → materialización.

Los materiales históricos no deberán presentarse como resultados posteriores a la materialización.

La evidencia deberá permitir distinguir estado anterior, estado liberado y actos posteriores.

---

## §12 — Relación con H9

H9 constituye antecedente contractual y evaluativo del Gate S0.

El presente contrato no reabre retroactivamente H9.

La primera aplicación del Protocolo sobre este contrato constituye un acto posterior.

---

## §13 — Primera aplicación del Protocolo

El Release S0 constituye la primera aplicación operacional del:

"DOCS/PROTOCOLO_REVISION_ACTOS.md"

La aplicación seguirá el procedimiento vigente.

La primera aplicación producirá los artefactos documentales establecidos en §24.

La revisión del contrato precede a la emisión del dictamen.

---

## §14 — Unidad de revisión

La unidad primaria de revisión será el presente contrato como acto sometido al Protocolo.

La revisión deberá distinguir:

- disposición contractual;
- supuesto;
- evidencia;
- decisión del Operador;
- condición;
- resultado de falsación.

La ausencia de un material no constituye automáticamente objeción.

---

## §15 — IPVE

El Release será trazable mediante:

- I — Invariantes
- P — Propiedades
- V — Validaciones
- E — Evidencias

IPVE registra documentalmente los resultados.

No constituye un eje adicional de juicio.

---

## §16 — Janus ∞

Janus ∞ constituye el metamarco permanente de observación.

Opera dentro del acto bajo revisión, incluida la autoaplicación del Protocolo, pero no sustituye los resultados de primer orden.

No genera por sí mismo:

- PASS;
- OBJECIÓN;
- NO DETERMINADO.

---

## §17 — Horizonte Rodriguiano

El Release conserva el horizonte:

Dogma → Disciplina → Economía.

La revisión deberá poder confrontarlo además con:

- Educación Popular;
- destinación a ejercicios útiles;
- aspiración fundada a la propiedad;
- O Inventamos o Erramos.

La aplicación deberá distinguir cita, interpretación y decisión metodológica.

---

## §18 — Corpus S0 sin deudas

El corpus público S0 se define bajo una condición estricta:

cero deudas abiertas.

Los límites declarados, exclusiones, condiciones de entorno y líneas de fuga no constituyen deudas.

Las deudas del Programa permanecen en el corpus privado correspondiente y no forman parte del corpus público S0.

Por tanto, antes de la publicación deberá comprobarse que cada documento seleccionado:

1. pertenece directamente a S0;
2. se encuentra vigente para el Release;
3. es necesario para comprender, ejecutar, verificar o reproducir S0;
4. no contiene una deuda abierta;
5. es coherente con este contrato.

---

## §19 — Versionado y evolución

El Release S0-v1.0.0 constituye la versión inicial.

Las modificaciones posteriores deberán distinguir entre:

- errata;
- corrección documental;
- corrección técnica;
- nueva versión;
- modificación sustantiva.

La nueva versión no elimina la trazabilidad histórica de la anterior.

---

## §20 — Binarios ejecutables

El Release S0-v1.0.0 no incluye binarios ejecutables.

La eventual publicación futura de binarios no constituye compromiso contractual de S0.

Una futura publicación deberá contar con verificación empírica y declaración explícita del entorno correspondiente.

---

## §21 — Visibilidad y materialización pública

El Release tendrá carácter público.

El repositorio destinado a la publicación es:

SCFV_S0_V1.0.0

La publicación no implica hacer público todo el corpus privado del Programa.

El corpus público estará limitado a los materiales definidos en este contrato.

---

## §22 — Condición D-1

La corrección D-1 en "H9_GATE_S0_EVALUACION.md", §10, deberá ejecutarse antes de la materialización definitiva del Release.

El Operador ha decidido que esta corrección no quede como deuda.

Una vez realizada deberá existir verificación de que:

- §7 y §10 de la evaluación son coherentes;
- el estado C2 corresponde al estado formal vigente del Gate;
- la contradicción detectada ha desaparecido.

El Release no se declarará materializado mientras D-1 no haya sido corregida y verificada.

---

## §23 — Giro 02

Este contrato no cierra por sí mismo el Giro 02.

Release S0 ≠ cierre automático del Giro 02.

El cierre del Giro requerirá el acto correspondiente.

---

## §24 — Artefactos de la primera aplicación del Protocolo

La primera aplicación del Protocolo produce tres artefactos diferenciados:

### §24.1 — Contrato de Release

El presente documento constituye el contrato de Release.

Su régimen es privado.

Se materializará en el corpus de investigación.

### §24.2 — Dictamen de IA-2

IA-2 emitirá un dictamen sobre el contrato después de la finalización de la revisión correspondiente.

Su régimen es privado.

Se materializará en el corpus de investigación.

### §24.3 — Bitácora de ejecuciones del Protocolo

La primera aplicación produce además una bitácora de ejecuciones del Protocolo.

Su función es:

- preservar la genealogía de las aplicaciones del Protocolo;
- conservar evidencia empírica de su operación;
- proveer evidencia para la evaluación de la hipótesis de antifragilidad establecida en el Protocolo §11.

La bitácora tiene régimen privado y se materializará en el corpus de investigación.

La materialización efectiva de esta bitácora constituye un acto separado.

### §24.4 — Relación con el repositorio público

El contrato, el dictamen de IA-2 y la bitácora permanecen fuera del repositorio público S0.

El EA 2.0, en cambio, forma parte del corpus público S0 conforme al §5.1.

La materialización de cada artefacto es un acto del Operador.

Los momentos de materialización corresponden a su decisión.

---

## §25 — Condiciones previas a la materialización definitiva

Antes de la materialización definitiva deberán estar satisfechas:

1. revisión del contrato mediante el Protocolo;
2. resolución por el Operador de las objeciones que permanezcan abiertas;
3. corrección y verificación de D-1;
4. comprobación del licenciamiento AGPL-3.0;
5. comprobación final del corpus;
6. comprobación del estado y composición del EA 2.0;
7. comprobación de que los documentos seleccionados no contienen deudas abiertas;
8. generación y conservación de la evidencia de materialización.

---

## §26 — Acto de liberación

La aprobación del contrato no equivale por sí misma a publicación.

El Release se considerará materializado únicamente cuando el Operador autorice y ejecute el acto correspondiente y exista evidencia verificable de dicha materialización.

---

## §27 — Enmiendas

Toda modificación previa a la aprobación definitiva deberá conservar trazabilidad:

versión anterior → objeción o motivo → modificación → nueva revisión → decisión del Operador.

Después de la materialización, cualquier modificación deberá distinguirse entre cambio del contrato y cambio del artefacto liberado.

---

## §28 — Estado del presente documento

Este documento constituye el estado consolidado del contrato después de las decisiones P1–P6, de las correcciones F-22–F-25 y F-27, y de la micro-integración F-29–F-31.

F-26 y F-28 fueron retiradas por IA-2 tras revisión metodológica (HL-45); no se integran al contrato.

Permanece sometido a verificación mecánica final por IA-2.

No constituye todavía declaración de publicación ni materialización del Release.

---

## CONSTANCIAS

### Operador

El Operador suscribe el presente contrato como autoridad decisoria y ejecutora del Programa.

El Operador declara:

- que las decisiones P1–P6 fueron adoptadas y comunicadas expresamente a las IA;
- que las decisiones P-a, P-b y P-c quedan formalmente adoptadas;
- que la distinción metodológica constancia ≠ dictamen §24.2 queda fijada;
- que la autorización de materialización se ejerce conforme al Protocolo §19.3.

Nombre: Domingo Eduardo Díaz Navas
Rol: Operador / autoridad ejecutora y decisoria
Firma: DEDN
Fecha: 2026-09-17

---

### IA-1 — Investigador constructor

Declaro:

- haber construido y redactado el presente contrato;
- haber integrado las objeciones F-1 a F-25 y F-27;
- haber integrado las decisiones P1–P6 del Operador;
- haber integrado las decisiones P-a, P-b y P-c;
- haber integrado la distinción constancia ≠ dictamen §24.2;
- haber integrado las correcciones de consolidación F-29, F-30 y F-31;
- no haber introducido cambios no autorizados en el cuerpo contractual.

La presente versión queda sometida a la verificación mecánica final de IA-2 y, en su caso, a la decisión del Operador.

Esta constancia no constituye aprobación ni decisión.

Rol: Investigador constructor
Firma/constancia: IA-1
Fecha: 2026-09-17

---

### IA-2 — Investigador falsador

Declaro:

- haber aplicado el Protocolo de Revisión de Actos Materializados al presente contrato en sus iteraciones sucesivas;
- haber emitido las objeciones F-1 a F-31, de las cuales F-26 y F-28 fueron retiradas por revisión metodológica (HL-45);
- haber verificado mecánicamente la integración de F-29, F-30 y F-31, con resultado 4/4 PASS;
- que el contrato consolidado resulta APTO SIN OBJECIONES;
- no mantener objeciones abiertas que impidan la formalización del contrato.

Esta constancia no constituye co-decisión. La autoridad decisoria y de materialización permanece en el Operador.

El dictamen §24.2 —artefacto privado independiente— será emitido con posterioridad conforme al §24 del contrato.

Rol: Investigador falsador
Firma/constancia: IA-2
Fecha: 2026-09-17

---

**Fin del contrato.**

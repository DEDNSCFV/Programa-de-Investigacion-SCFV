════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON ANGRISANI 2019
DOCUMENTO: ACTAS/ACTO_6_0_03_AUDITORIA_ANGRISANI.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autores: Damián Roberto Antonio Angrisani · Claudia Lorena López
Obra: Sistemas de Información Contable 2: SIC 2
Editorial: Angrisani Editores · Buenos Aires, 2019
Raw: ~/.angrisani_raw.txt · 8.562 líneas · 497.608 bytes
Naturaleza: canon disciplinar contable contemporáneo en español

Loci invocados:
  L386-390   · ENTRADA → PROCESAMIENTO → SALIDA
  L415-417   · 6 tareas del procesamiento de datos
  L489-500   · concepto de contabilidad · funciones
  L502-530   · Sistemas de Información Contable · subsistemas
  L748-760   · formas de registración contable
  L834-900   · proceso manual directo · subdiarios

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Contabilidad como sistema de información
  Esquema canónico ENTRADA → PROCESAMIENTO DE LOS DATOS → SALIDA.
  Del sistema contable surge la información para usuarios internos
  y externos — L386-390.

C2 · Procesamiento de datos (6 tareas)
  "reconocimiento, clasificación, identificación, registración,
  comprobación y almacenamiento" — L415-417.

C3 · Subsistemas
  Los diferentes subsistemas suministran datos al SIC para
  procesamiento, almacenamiento y emisión de informes — L502-530.

C4 · Funciones de la contabilidad
  Captación de datos · teneduría de libros · análisis e
  interpretación · planificación y control — L489-500.

C5 · Formas de registración
  Proceso Manual Directo · Registración Descentralizada/Centralizada
  con subdiarios y asiento resumen — L748-760, L834-900.

C6 · Nuevo Marco Conceptual
  La contabilidad no es solo teneduría de libros. Como sistema
  incluye captación, teneduría, análisis e interpretación — L502-507.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · CONTABILIDAD COMO SISTEMA DE INFORMACIÓN

  C1-E1 · E3 tiene entrada → procesamiento → salida
    Resultado: resiste
    Cita: L386-390 "ENTRADA / PROCESAMIENTO DE LOS DATOS / SALIDA"
    Ubicación: cli.py → integrador.py → motor.py

  C1-E2 · No hay "sector contable" explícito separado del resto
    Resultado: falla parcial
    Cita: L390 "Sector Contable"
    Ubicación: arquitectura global

  C1-E3 · Usuarios (internos/externos) no declarados
    Resultado: no aplica
    Cita: L386-390
    Ubicación: global

C2 · PROCESAMIENTO DE DATOS · 6 TAREAS

  C2-E1 · Reconocimiento
    Resultado: resiste
    Cita: L415 "reconocimiento, clasificación, identificación..."
    Ubicación: extractor.evidencia_desde_evento

  C2-E2 · Clasificación
    Resultado: resiste
    Cita: L415-416 "clasificación, identificación"
    Ubicación: evaluador.evaluar_fractal

  C2-E3 · Identificación
    Resultado: resiste
    Cita: L416 "identificación, registración"
    Ubicación: evaluador.parsear_accion

  C2-E4 · Registración
    Resultado: resiste
    Cita: L416 "registración, comprobación"
    Ubicación: motor.generar_asiento

  C2-E5 · Comprobación
    Resultado: resiste alto
    Cita: L416 "comprobación y almacenamiento"
    Ubicación: motor.py · invariantes I1-I6 · XNOR triple

  C2-E6 · Almacenamiento
    Resultado: resiste alto
    Cita: L416-417 "almacenamiento"
    Ubicación: event_store.guardar · hash chain

C3 · SUBSISTEMAS

  C3-E1 · No hay subsistemas explícitos que alimenten al SIC
    Resultado: falla
    Cita: L524-530 "Los diferentes subsistemas suministran datos"
    Ubicación: arquitectura global

  C3-E2 · Los cinturones internos cumplen roles análogos
    Resultado: parcial
    Cita: L530 "suministran datos al sistema... para su procesamiento"
    Ubicación: scfv_dsr/ estructura de cinturones

C4 · FUNCIONES DE LA CONTABILIDAD

  C4-E1 · Captación (metodología)
    Resultado: resiste
    Cita: L505-507 "metodología para la captación de datos"
    Ubicación: parser + evaluador + extractor

  C4-E2 · Teneduría de libros
    Resultado: resiste
    Cita: L507 "la teneduría de libros"
    Ubicación: motor.py + event_store.py

  C4-E3 · Análisis e interpretación
    Resultado: falla
    Cita: L508-509 "El análisis y la interpretación de la información"
    Ubicación: global (no existe módulo)

  C4-E4 · Planificación y control
    Resultado: falla
    Cita: L509-511 "para planificar la marcha de la empresa y
          controlar la adecuada ejecución de las decisiones"
    Ubicación: global (no existe módulo)

C5 · FORMAS DE REGISTRACIÓN

  C5-E1 · Proceso Manual Directo (documentos → asiento → mayor)
    Resultado: resiste
    Cita: L834-838 "una registración manual directa"
    Ubicación: pipeline E3 sigue este patrón

  C5-E2 · Descentralizada/Centralizada con subdiarios
    Resultado: no aplica
    Cita: L850-870 "Subdiarios... asiento resumen"
    Ubicación: E3 es volumen-agnóstico

  C5-E3 · Mayorización
    Resultado: parcial
    Cita: L834-838 "Libro Diario / Libro Mayor"
    Ubicación: EventStore actúa como diario, no mayor

  C5-E4 · Reportes (mayor, balances)
    Resultado: falla
    Cita: L502-504 "emisión de la totalidad de los informes"
    Ubicación: reportes_motor.py · huérfano

C6 · NUEVO MARCO CONCEPTUAL

  C6-E1 · Adopta 5 elementos del MC NIIF
    Resultado: resiste
    Cita: L502-507 "La contabilidad no es solo registro..."
    Ubicación: categorias.json · §elementos

  C6-E2 · No declara el ciclo completo de funciones
    Resultado: falla
    Cita: L502-511 "Como sistema incluye:... análisis... planificar... controlar"
    Ubicación: global

  C6-E3 · E3 es "registro de operaciones y hechos económicos" sin
          los otros componentes
    Resultado: falla
    Cita: L504 "La contabilidad no es sólo registro de operaciones
          y de hechos económicos"
    Ubicación: autodefinición de E3

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · SIC                      1        0       1       1
  C2 · Procesamiento 6 tareas   6        0       0       0
  C3 · Subsistemas              0        1       1       0
  C4 · Funciones                2        0       2       0
  C5 · Registración             1        1       1       1
  C6 · Marco conceptual         1        0       2       0
  ──────────────────────────────────────────────────────────────
  Total                        11        2       7       2

  Emergencias registradas: 22

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  El E3 resiste las 6 tareas del procesamiento de datos exactamente
  como Angrisani las enumera: reconocimiento, clasificación,
  identificación, registración, comprobación, almacenamiento.
  También resiste el esquema ENTRADA → PROCESAMIENTO → SALIDA.
  Y resiste la forma "Proceso Manual Directo".

D · Divergencia
  El E3 es un SIC de registro, no un SIC completo. Angrisani
  distingue funciones: captación + teneduría + análisis +
  interpretación + planificación + control. El E3 solo cubre las
  dos primeras.

E · Emergencia
  El E3 es un SIC truncado. Angrisani da un marco claro: un SIC
  contemporáneo no es solo registro. Es registro + análisis +
  planificación + control. La deuda no es código: es declaración
  de alcance. El E3 no declara qué funciones cubre y cuáles no.

E · Enriquecimiento
  Angrisani da vocabulario preciso en español: E3 es "teneduría de
  libros automatizada con comprobación fuerte". El módulo
  reportes_motor huérfano es precisamente la pieza que Angrisani
  identificaría como faltante. El huérfano no es basura: es la
  promesa de un SIC completo sin cumplir.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Angrisani 2019 (SIC 2) × SCFV_DSR E3.
No emite veredicto global de aptitud del artefacto.
No anticipa el diagnóstico L4/L5.
El diagnóstico es competencia exclusiva de ACTO 6.0.CONV.

────────────────────────────────────────────────────────────────────────

§8 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: DEDN · C.P.C. Nº 183594
  Fecha: 2026-09-26

IA-1 · Constructor · constancia de interpretación arquitectónica
  Firma: IA-1 · Constructor
  Constancia: acta 6.0.03 redactada conforme al protocolo 6.0 §5,
  con emergencias ancladas a loci del raw y a ubicaciones del E3.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

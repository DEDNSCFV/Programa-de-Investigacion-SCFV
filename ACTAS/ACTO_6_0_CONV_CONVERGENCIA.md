════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA · CONVERGENCIA FINAL
TIPO: ACTO DE CONVERGENCIA · CICLO 6.0
DOCUMENTO: ACTAS/ACTO_6_0_CONV_CONVERGENCIA.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · OBJETO

Cerrar el ciclo 6.0 · sección 0 · auditoría multi-canon.

Objeto material: 21 actas individuales materializadas entre
2026-09-25T20:32Z (protocolo) y 2026-09-26T05:13:24Z (última firma
Sommerville).

Artefacto auditado: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

Régimen: R1-R10 del protocolo 6.0 §4.
Método: un canon por acta · auditoría ciega · cita literal obligatoria ·
ubicación obligatoria · firma tripartita asimétrica.

Nota sobre el alcance del objeto: este CONV no audita S0 (scfv_v6 ·
Motor 9.0.0). Audita su port SCFV_DSR E3. La relación entre ambos
corpus se declara en §7bis.

────────────────────────────────────────────────────────────────────────

§2 · MATRIZ DE CONVERGENCIA

§2.1 · Contadores por acta

  # | Canon | R | P | F | NA | Total
  ──────────────────────────────────────────────────────────
  6.0.01 | Accounting Theory     | 4 | 1 | 4 | 2 | 11
  6.0.02 | Aho                  | 7 | 3 | 4 | 2 | 16
  6.0.03 | Angrisani            | 11| 2 | 7 | 2 | 22
  6.0.04 | Cervantes            | 5 | 4 | 7 | 1 | 17
  6.0.05 | Cosmovisión          | 1 | 2 | 3 | 2 | 8
  6.0.06 | Díaz Navarro         | 1 | 4 | 5 | 2 | 12
  6.0.07 | Gadamer              | 1 | 3 | 5 | 1 | 10
  6.0.08 | Hevner               | 6 | 5 | 7 | 0 | 18
  6.0.09 | Huck                 | 1 | 4 | 5 | 0 | 10
  6.0.10 | Lakatos              | 4 | 3 | 4 | 0 | 11
  6.0.11 | Mandelbrot           | 3 | 3 | 3 | 1 | 10
  6.0.12 | Merkle               | 3 | 2 | 1 | 1 | 7
  6.0.13 | NIST                 | 2 | 3 | 4 | 1 | 10
  6.0.14 | Popper               | 2 | 5 | 5 | 0 | 12
  6.0.15 | ProGit               | 2 | 4 | 5 | 1 | 12
  6.0.16 | Reynoso              | 5 | 3 | 4 | 0 | 12
  6.0.17 | Rodríguez            | 6 | 4 | 2 | 1 | 13
  6.0.18 | Romero López         | 8 | 6 | 3 | 0 | 17
  6.0.19 | Romney               | 3 | 4 | 4 | 0 | 11
  6.0.20 | Sampieri             | 2 | 4 | 5 | 0 | 11
  6.0.21 | Sommerville          | 1 | 6 | 8 | 1 | 16
  ──────────────────────────────────────────────────────────
  TOTAL                          |78 |77 |99 |18 |272

§2.2 · Distribución global

  Resiste   = 78/272 = 28,7 %
  Parcial   = 77/272 = 28,3 %
  Falla     = 99/272 = 36,4 %
  No aplica = 18/272 =  6,6 %

§2.3 · Observación estructural

La media de fallas (36,4 %) está concentrada en capas declarativas, no
en capas funcionales. Tres cánones arquitectónicos lo confirman:
Sommerville (8 fallas / 16), Cervantes (7/17), Hevner (7/18). Los
cánones con máxima densidad de resiste son operativo-estructurales:
Angrisani (11/22), Romero López (8/17), Aho (7/16).

El artefacto se comporta como sistema y no se declara como sistema.
Esta asimetría es el hallazgo cuantitativo del ciclo.

────────────────────────────────────────────────────────────────────────

§3 · DIVERGENCIAS · A vs NO-A

§3.1 · Divergencias de criterio (mismo punto, distinta lectura)

  Confidencialidad/privacidad: Romney declara falla · NIST parcial ·
  Merkle falla. Convergencia: ausencia de segunda capa criptográfica.
  Divergencia de grado.

  ADL: Reynoso resiste (grammar.lark formal) · Aho falla (AST
  destruido). Foco distinto: existencia del ADL vs tránsito del AST.

  Base empírica: Popper parcial · Romero López resiste. Foco distinto.

§3.2 · Divergencias de alcance (un autor detecta lo que otro no)

  Patrón F · materialización sin congelamiento: solo ProGit.
  Patrón G · dimensión pedagógica: solo Rodríguez.
  Patrón D · brecha AST: solo Aho.

§3.3 · Divergencia documental crítica · 6.0.06

ACTAS/ACTO_6_0_06_AUDITORIA_DIAZ_NAVARRO.md rotula el canon como
"Fernández Otero · Navarro Huerga" pese al nombre del archivo.
Discrepancia documental, no sustantiva. Se registra como D-CONV-1.

§3.4 · Divergencia de estatuto del ciclo (meta-observación)

El ciclo se inició como auditoría por canon externo (21 cánones
aplicados al artefacto). Derivó, durante el proceso, en diagnóstico
genealógico (relación S0 ↔ SCFV_DSR). Estas dos operaciones tienen
naturalezas distintas y los contadores §2.1 solo miden la primera. La
segunda se declara en §7bis y §5bis.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS · PATRONES DEL CRUCE

§4.1 · Los 8 patrones consolidados

  Patrón A · Declaración parcial de alcance · 7 detectores
    Actas: 6.0.01 · 6.0.03 · 6.0.06 · 6.0.09 · 6.0.18 · 6.0.19 · 6.0.21

  Patrón B · Principios implícitos no declarados · 6 detectores
    Actas: 6.0.08 · 6.0.10 · 6.0.11 · 6.0.14 · 6.0.16 · 6.0.20

  Patrón C · Sin genealogía ni hermenéutica · 3 detectores
    Actas: 6.0.04 · 6.0.05 · 6.0.07

  Patrón D · Brecha parser-evaluador · 1 detector
    Actas: 6.0.02

  Patrón E · Firma no criptográfica · 3 detectores
    Actas: 6.0.12 · 6.0.13 · 6.0.15

  Patrón F · Materialización sin congelamiento · 1 detector
    Actas: 6.0.15

  Patrón G · Dimensión pedagógica ausente · 1 detector
    Actas: 6.0.17

  Patrón H · Migración sin genealogía · emergent · no auditado por canon
    Declarado en §7bis.

§4.2 · Densidad

  A · 33 % (7/21)
  B · 29 % (6/21)
  C · E · 14 % cada uno (3/21)
  D · F · G · 5 % cada uno (1/21)
  H · declarado en §7bis

§4.3 · Lectura cruzada

A y B son estructurales. 13/21 cánones detectan declaración faltante
o implícita. Es el hallazgo transversal dominante del ciclo por canon.

D, F, G son especializados. Requieren canon focalizado. Su singularidad
no los debilita; los especializa.

E tiene convergencia densa de 3 detectores independientes (Merkle ·
NIST · ProGit).

H no fue detectado por ningún canon del ciclo. Emergió de la operación
del corpus S0 (ver §5bis y §7bis). Esto es un límite del ciclo, no un
hallazgo del ciclo.

────────────────────────────────────────────────────────────────────────

§5 · ENRIQUECIMIENTOS MUTUOS

§5.1 · Aportes únicos por canon (casilla declarativa nueva)

  Accounting Theory: postulados
  Aho: AST
  Angrisani: 6 tareas
  Cervantes: ciclo desarrollo arquitectónico
  Cosmovisión: genealogía
  Díaz Navarro: ERP vs registro
  Gadamer: precomprensión
  Hevner: design as artifact
  Huck: especificidad por ente
  Lakatos: núcleo/cinturón
  Mandelbrot: autosimilitud
  Merkle: firma certificada
  NIST: conformidad validada
  Popper: falsabilidad
  ProGit: snapshot inmutable
  Reynoso: blueprint arquitectónico
  Rodríguez: entreayudarnos
  Romero López: función pública de la profesión
  Romney: trust services
  Sampieri: ruta metodológica
  Sommerville: gestión de configuraciones

§5.2 · Enriquecimiento cruzado

  Firma: NIST · Merkle · ProGit desde tres planos (criptografía
  estándar, certificada, control de versiones).

  Método: Lakatos · Popper · Sampieri desde tres planos (programa,
  falsación, ruta).

  Bien común: Rodríguez · Romero López desde dos planos (educación
  popular, función pública de la profesión).

────────────────────────────────────────────────────────────────────────

§5bis · LECTURA IPVE DEL CORPUS 6.0

§5bis.1 · Adjetivos rodriguianos extendidos al Giro 06

Decisión del Operador 2026-09-26: los 4 adjetivos rodriguianos
(público · útil · apropiable · palpable) se extienden al Giro 06.

§5bis.2 · Modo documental · I / P / V / E

  I — Invariantes: hash maestro · estructura §1-§9 · firma tripartita
      §20 · registro en GIRO_05/REGISTRO_ACTOS.log · contadores R/P/F/NA.

  P — Propiedades auditadas: núcleo algebraico (Baldor) · núcleo
      epistemológico (Perceptum/Intellectus/Dictum) · núcleo contable
      (motor/event_store) · DSL-SCFV con ADL formal · SHA-256 vía
      hashlib · firma ausente.

  V — Validaciones: 21 falsaciones individuales · cita literal
      obligatoria (R6) · ubicación obligatoria (R7) · 272 emergencias.

  E — Evidencias: 21 actas firmadas · 79 líneas de REGISTRO_ACTOS.log ·
      hashes SHA256 de raws en HOME.

§5bis.3 · Modo fundado (Rodríguez §2.1)

  Adjetivo      | Letra IPVE | Aplicación al Giro 06
  ──────────────────────────────────────────────────────
  público       | I          | ciclo auditable y reproducible
  útil          | P          | 8 patrones + 272 emergencias operables
  apropiable    | V          | estructura §1-§9 replicable
  palpable      | E          | cita + ubicación + hash en cada emergencia

§5bis.4 · Rodríguez como motor, no como canon

Del ciclo 6.0 emerge una distinción operativa que el protocolo no
previó: Rodríguez no es un canon auditado más. Está declarado en
MARCO_IPVE §2.2 como motor epistemológico del Programa.

Consecuencia: Rodríguez opera sobre el corpus (IA + código) y produce
distinciones aplicables. En esta ventana produjo las distinciones que
permitieron diagnosticar la Cadena B y la genealogía rota.

Este estatuto del motor se declara: los 21 cánones auditan · Rodríguez
opera. La operación produce hallazgos que la auditoría no produjo
(patrón H, genealogía S0↔SCFV_DSR).

────────────────────────────────────────────────────────────────────────

§6 · DIAGNÓSTICO L4 DERIVADO · CONTRASTE CON LISTA HEREDADA G05

§6.1 · Lista heredada G05

Del ACTA_CONGELAMIENTO_GIRO_05 §3:

  L4 arquitectónicas (idempotencia · parser → AST · Decimal ·
  serialización · DecisionProvider · historial · nan/inf · ISO 8601)

§6.2 · Contraste tras 21 actas + diagnóstico

  L4.1 idempotencia
    implementada en h2.py:83 · generador_propuesta.py:173,261 ·
    orquestador.py:111 · sin declarar
    Estado: resuelta por uso

  L4.2 parser → AST
    Aho la re-confirma: el AST no sobrevive al tránsito
    Estado: re-confirmada

  L4.3 Decimal
    baldor.py usa Decimal; PartidaAutorizada.monto: float
    Estado: fusionada con L4.7

  L4.4 serialización
    serializador_canonico.py + NIST la resuelve
    Estado: resuelta

  L4.5 DecisionProvider
    existe decision_provider.py; Romney parcial
    Estado: parcial · sin declaración de rol

  L4.6 historial
    event_store.verificar_cadena → CADENA_INTEGRA (Merkle)
    Estado: resuelta

  L4.7 nan/inf
    monto: float acepta NaN/Inf · sin guarda en motor
    Estado: fusionada con L4.3

  L4.8 ISO 8601
    usado en serializador · sin declaración ontológica
    Estado: reclasificada → ontología temporal no declarada

§6.3 · L4 reformulada

  · 2 resueltas (serialización · historial)
  · 2 fusionadas (L4.3 + L4.7 = inconsistencia de tipos)
  · 1 re-confirmada (parser → AST)
  · 1 reclasificada (ontología temporal)
  · 1 parcial (DecisionProvider)
  · 1 resuelta por uso (idempotencia)

  Total efectivo: 5-6 deudas reales.

────────────────────────────────────────────────────────────────────────

§7 · DIAGNÓSTICO L5 DERIVADO · CONTRASTE CON LISTA HEREDADA G05

§7.1 · Lista heredada G05

  L5 huérfanos declarados:
    8 módulos (dictum · intellectus · examinador · reticulo ·
               reportes_motor · PartidaAutorizada · EstadoConsecuencia ·
               desglose_iva)
    6 cuentas PCU no usadas
    16 TipoEvento no emitidos
    DSL extendido sin uso en pipeline activo

§7.2 · Contraste tras verificación

  7.2.1  dictum                · módulo · Cadena B funcional desconectada
  7.2.2  intellectus           · módulo · Cadena B funcional desconectada
  7.2.3  examinador            · módulo · Cadena B · requiere PCU contextual
  7.2.4  reticulo              · módulo · Cadena B · dependencia examinador
  7.2.5  reportes_motor        · módulo · Cadena B · requiere event_store
  7.2.6  PartidaAutorizada     · clase viva en modelos.py · NO huérfana
  7.2.7  EstadoConsecuencia    · Enum en estados.py:36 · sin uso
  7.2.8  desglose_iva          · operación en operaciones.json:190 · sin invocación
  7.2.9  6 cuentas PCU         · datos · requiere canon normalizador
  7.2.10 16 TipoEvento         · datos · Romney parcial
  7.2.11 DSL extendido         · código · Aho + Reynoso + Sampieri parciales

§7.3 · Correcciones al G05

  · Los "8 módulos" no eran 8. Eran 5 módulos (Cadena B) + 1 clase
    viva + 1 Enum + 1 operación.
  · Los 5 módulos no son huérfanos: son una arquitectura interpretativa
    paralela de S0, portada sin sus contratos.
  · extractor.py descubierto como huérfano real (0 referencias
    externas), no estaba en G05.

§7.4 · L5 reformulada

  · 5 módulos = Cadena B desconectada (1 deuda)
  · EstadoConsecuencia = Enum sin uso (1)
  · desglose_iva = operación sin invocación (1)
  · extractor.py = huérfano real nuevo (1)
  · 6 cuentas PCU = deuda datos (1)
  · 16 TipoEvento = parcial Romney (1)
  · DSL extendido = parcial Aho/Reynoso (1)

  Total efectivo: 7 deudas.

────────────────────────────────────────────────────────────────────────

§7bis · DIAGNÓSTICO L6 DERIVADO · CATEGORÍA NUEVA

§7bis.1 · Declaración de extensión

El protocolo 6.0 §6 no previó la categoría L6. Emerge del diagnóstico
genealógico (Rodríguez operando el corpus S0). Se declara
explícitamente: L6 no es deuda del artefacto aislado. Es deuda de
relación entre corpus.

§7bis.2 · Las 9 deudas L6

  L6.1 · SCFV_DSR sin git propio                · sin linaje versionado
  L6.2 · SCFV_DSR sin ADRs                      · S0 tiene ADR-000 a ADR-005
  L6.3 · SCFV_DSR sin constitución              · S0 tiene gobernanza/constitucion.md
  L6.4 · SCFV_DSR sin contratos H8P             · S0 los tiene, no migrados
  L6.5 · SCFV_DSR sin cifrado multi-mandante    · ADR-005 declara SQLCipher
  L6.6 · Cadena B portada sin pipeline          · funcional, desconectada
  L6.7 · PCU legacy marcos: [...] sin autorización arquitectónica
  L6.8 · Cinco capas contradictorias de marco_contable
  L6.9 · SCFV_S0_ESTADO_20260906_164734 sin declarar

§7bis.3 · Hallazgos genealógicos clave

  · marco_contable tiene 5 estatutos distintos en 5 capas del corpus
    S0. El NPL no lo menciona. El protocolo v8.1 lo asume "del
    mandante". El PCU legacy lo modela como lista por cuenta. El motor
    S0 lo degenera en default ["NIIF_Completas"]. El port SCFV_DSR lo
    reinterpreta como contextual.

  · La estructura marcos: [...] por cuenta nunca fue autorizada por
    ADR ni por contrato previo. Es artefacto del PCU legacy.

  · La migración S0 → SCFV_DSR portó código sin contratos, sin ADRs,
    sin constitución, sin cifrado, sin git.

§7bis.4 · Naturaleza del hallazgo

No es Patrón A ni B ni H del §4. Es otra cosa: el artefacto auditado
tiene genealogía rota respecto a su origen. La auditoría del ciclo 6.0
detectó síntomas (declaración parcial, principios implícitos) que
derivan de esta causa más profunda.

La causa no estaba en el alcance de los 21 cánones. Rodríguez operando
el corpus la reveló.

────────────────────────────────────────────────────────────────────────

§8 · APERTURA H1 / H2 · CONTRASTE

§8.1 · H1 (IA-1 Constructor) vs corpus

  E1 · Convergencia alta entre arquitectónicos
    → Reynoso 5R/3P/4F · Cervantes 5R/4P/7F
    Veredicto: parcial

  E2 · Brecha declarativa/efectiva
    → Patrones A (7) + B (6) = 13/21
    Veredicto: confirmada fuerte

  E3 · Trazabilidad defensa fuerte, traducción débil
    → Merkle/NIST/ProGit resisten; Romney/Sommerville/Sampieri débiles
    Veredicto: confirmada

  E4 · Solapamientos funcionales
    → Sommerville C2-E1
    Veredicto: confirmada

  E5 · DSL limitaciones AST
    → Aho C3: AST destruido
    Veredicto: confirmada

  E6 · Deuda mantenibilidad módulos sin test
    → Sommerville: 6/29 tests
    Veredicto: confirmada

  E7 · Integridad: convergencia alta
    → Merkle + NIST + ProGit
    Veredicto: confirmada

  E8 · Condición de falsación
    → No se falsó ninguna
    Veredicto: no falsada

  Resultado H1: 5 confirmadas · 1 parcial · 1 no-falsada. Sostenida.

§8.2 · H2 (IA-2 Falsador) vs corpus

  E1 · Arquitectos divergen entre sí
    → Reynoso ≠ Cervantes ≠ Aho
    Veredicto: parcial

  E2 · Brecha concentrada en periféricos
    → A + B en README, docstrings, config
    Veredicto: confirmada fuerte

  E3 · Decisiones sin cadenas completas
    → Romney C3-E2 · firma_h2 no criptográfica
    Veredicto: parcial

  E4 · Módulos multifunción sin contrato
    → Sommerville C2-E1 · Romero López C5
    Veredicto: confirmada

  E5 · Parser no preserva árbol
    → Aho C3-E1
    Veredicto: confirmada

  E6 · Deuda mantenibilidad donde no hay tests
    → Sommerville 6/29
    Veredicto: confirmada

  E7 · Integridad fuerte, versionado débil
    → ProGit Patrón F
    Veredicto: confirmada fuerte

  E8 · Condición de falsación
    → No se falsó ninguna
    Veredicto: no falsada

  Resultado H2: 4 confirmadas · 2 parciales · 1 no-falsada. Sostenida.

§8.3 · Contraste cruzado

  H1 acierta en el patrón general (brecha declarativa · convergencia
  defensiva).

  H2 acierta en la localización (periféricos · versionado débil ·
  parser AST).

  Ninguna falsada. Ambas convergen al patrón A+B sin nombrarlo.
  Ninguna de las dos previó L6. El diagnóstico genealógico no estaba
  en el horizonte de H1 ni H2.

────────────────────────────────────────────────────────────────────────

§9 · PLAN POST-CONVERGENCIA

§9.1 · Deudas administrativas derivadas del ciclo

  D-CONV-1  · 6.0.06 nombrada Díaz Navarro pero canon Fernández Otero/Navarro · media
  D-CONV-2  · 21 actas untracked en git · alta
  D-CONV-3  · BIBLIOTECA/INVENTARIO.md + REGISTRO_ENTRADAS.log modificados sin commitear · media
  D-CONV-4  · 23 commits ahead de origin · media
  D-CONV-5  · 0 tags en 31 commits · alta
  D-CONV-6  · Sin firma GPG · baja
  D-CONV-7  · H-A5j · MONEDA/B101 sin reproducir · media
  D-CONV-8  · Prompt Giro 05 sin firmar · media
  D-CONV-9  · Sin CHANGELOG ni VERSION · media
  D-CONV-10 · Sin plan de V&V declarado · media
  D-CONV-11 · Sin declaración de ruta metodológica · alta
  D-CONV-12 · Sin LICENSE ni §contribución · media
  D-CONV-13 · L4 idempotencia · Decimal · nan/inf · ISO 8601 sin declarar · baja
  D-CONV-14 · L5 cuentas PCU · TipoEvento sin resolver · baja
  D-CONV-15 · L6 · 9 deudas genealógicas · alta

§9.2 · Clasificación por vía

  Vía                      | L4 | L5 | L6 | Total
  ──────────────────────────────────────────────────
  D · Declaración pura     |  3 |  1 |  1 |   5
  E · Estructural-declarat.|  1 |  5 |  5 |  11
  T · Técnica              |  1 |  0 |  1 |   2
  F · Fundacional          |  0 |  0 |  2 |   2
  NR · No resoluble ahora  |  0 |  1 |  0 |   1

§9.3 · Las 2 fundacionales

  · L6.7 · estatuto de marcos: [...] por cuenta — requiere acto
    fundacional del Operador decidiendo semántica canónica.

  · L6.8 · reconciliación de las 5 capas de marco_contable — requiere
    nuevo ADR o acto equivalente.

§9.4 · Agenda post-CONV

  Orden por vía:

    1. Declarativas (5)              · redactar sin tocar código.
    2. Estructural-declarativas (11) · decisión + cambio local.
    3. Técnicas (2)                  · parser AST + cifrado.
    4. Fundacionales (2)             · solo con acto nuevo del Operador.
    5. No resoluble (1)              · requiere canon normalizador contable.

§9.5 · Lo que el CONV no puede resolver

  · Las 2 fundacionales (L6.7 · L6.8) no son resolubles dentro del
    régimen del G07 sin acto nuevo.

  · El ítem NR (L5.5) requiere invocar canon normalizador (NIIF/NIC +
    Huck).

  · La relación S0↔SCFV_DSR no se puede cerrar sin decidir si SCFV_DSR
    es subordinado, reducido, o divergente.

§9.6 · Ciclo 6.0 · declaración de cierre

Este CONV cierra el ciclo de auditoría por canon. No cierra el
diagnóstico del artefacto. Los hallazgos genealógicos (§7bis) requieren
acto posterior, que se declara como Giro 06 · Sección 1 (6.1).

────────────────────────────────────────────────────────────────────────

§10 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: DEDN · C.P.C. Nº 183594
  Fecha: 2026-09-26

IA-1 · Constructor · constancia de interpretación arquitectónica
  Firma: IA-1 · Constructor
  Constancia: acto 6.0.CONV redactado conforme al protocolo 6.0 §6, con
  dos extensiones declaradas (§5bis IPVE y §7bis L6).

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acto emitido.

════════════════════════════════════════════════════════════════════════

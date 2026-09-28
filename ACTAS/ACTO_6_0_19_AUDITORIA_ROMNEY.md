════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON ROMNEY
DOCUMENTO: ACTAS/ACTO_6_0_19_AUDITORIA_ROMNEY.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autores: Marshall B. Romney · Paul John Steinbart
Obra: Accounting Information Systems (15th ed.)
Raw: ~/.romney_raw.txt · 4.517 líneas · 339.960 bytes
SHA256 raw: 0037cc04243522a09877bc44372af5eca2e15f024586ed611a87daa6218e2dab
Naturaleza: sistemas de información contable · control interno · REA

Loci invocados:
  L179-186  · AIS · value chain · blockchain · corporate strategy
  L373-374  · COBIT · COSO frameworks
  L610-683  · REA data model · REA diagram · relational implementation
  L827-836  · trust services (confidencialidad, privacidad, integridad, disponibilidad)
  L927-931  · fraud y abuse techniques
  L971      · controls to safeguard assets

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: contable/verificador_autorizacion.py · contable/event_store.py · contable/motor.py · contable/nucleo_consecuencias.py · contable/puente_autorizacion.py · contable/maquina_estados_asiento.py · kernel/operaciones.json

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · AIS como sistema de información contable
  El AIS captura, almacena y procesa datos contables para
  producir información útil — L179-186.

C2 · Value chain · rol estratégico
  El AIS participa en la cadena de valor de la organización
  — L186.

C3 · Trust services · 4 objetivos
  Confidencialidad · privacidad · integridad · disponibilidad
  — L827-836.

C4 · Frameworks de control · COSO/COBIT
  El control interno se organiza bajo marcos reconocidos
  — L373-374.

C5 · Ciclos transaccionales
  Revenue · expenditure · production · HR/payroll — L138-141.

C6 · Fraude y errores
  El AIS debe reconocer y mitigar fraude y errores
  — L927-931.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · AIS COMO SIC

  C1-E1 · Declaración como AIS
    Resultado: parcial
    Cita: L179 "How an AIS Can Add Value to an Organization"
    Ubicación: README.md:1-5 ("SCFV_DSR" · "Artefacto Design Science
    Research") — declara artefacto contable, no lo rotula "AIS"

  C1-E2 · Captura/almacena/procesa
    Resultado: resiste
    Cita: L971 "transaction processing, provision of adequate internal
    controls to safeguard assets (including data)"
    Ubicación: event_store.py (persistencia canónica) ·
    contable/motor.py (procesamiento) · extractor.py (captura)

C2 · VALUE CHAIN · ROL ESTRATÉGICO

  C2-E1 · Declaración de value chain
    Resultado: falla
    Cita: L186 "The Role of the AIS in the Value Chain"
    Ubicación: README.md (sin §value chain) · grep global sin
    coincidencias

C3 · TRUST SERVICES · 4 OBJETIVOS

  C3-E1 · Integridad
    Resultado: resiste
    Cita: L835 "provide for information processing integrity"
    Ubicación: event_store.py:16 ("La cadena hash utiliza exactamente
    las representaciones canónicas") · event_store.py:225
    ("verificar_cadena()") · event_store.py:282 ("CADENA_INTEGRA")

  C3-E2 · Confidencialidad y privacidad
    Resultado: falla
    Cita: L833 "cedures to protect the confidentiality of proprietary
    information, maintain the privacy of personally identifying
    information collected from customers"
    Ubicación: grep global sin cryptography/pynacl/privacy · pyproject.toml
    sin dependencias criptográficas

  C3-E3 · Disponibilidad
    Resultado: parcial
    Cita: L834 "assure the availability of information resources"
    Ubicación: event_store.py (persistencia local sqlite3) · sin
    declaración de política de disponibilidad · sin réplica

C4 · FRAMEWORKS DE CONTROL · COSO/COBIT

  C4-E1 · Declaración COSO/COBIT
    Resultado: falla
    Cita: L373-374 "COBIT Framework 326 · COSO'S Internal Control
    Framework 328"
    Ubicación: grep global sin COSO ni COBIT

  C4-E2 · Control interno implementado sin declarar framework
    Resultado: parcial
    Cita: L828 "COSO's models (Internal Control and ERM) for internal
    control and risk management"
    Ubicación: contable/verificador_autorizacion.py (verificación
    separada) · maquina_estados_asiento.py (_TRANSICIONES con
    precondiciones) · motor.py ("MOTOR_VIOLACION: Motor sin
    verificador de autorización")

C5 · CICLOS TRANSACCIONALES

  C5-E1 · Ciclos por dominio
    Resultado: parcial
    Cita: L138-141 "CHAPTER 14 The Revenue Cycle... CHAPTER 15 The
    Expenditure Cycle... CHAPTER 16 The Production Cycle"
    Ubicación: fractales/{VENTAS, INVENTARIOS, PPE, INTANGIBLES,
    MONEDA, PROVISIONES, SUBVENCIONES, HIPERINFLACION, COMBINACIONES,
    ARRENDAMIENTOS}.scfv — dominios contables no rotulados como ciclos

C6 · FRAUDE Y ERRORES

  C6-E1 · Detección de fraude declarada
    Resultado: falla
    Cita: L927-931 "the threats of fraud and errors"
    Ubicación: grep global sin §fraud ni §fraude

  C6-E2 · Mecanismos de defensa contra manipulación
    Resultado: resiste
    Cita: L971 "controls to safeguard assets (including data)"
    Ubicación: motor.py:104 ("MOTOR_VIOLACION") ·
    verificador_autorizacion.py (verifica firma_h2, propuesta_id,
    correlation_id) · serializador_canonico.py ("PersistenciaViolacion")

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · AIS como SIC                          1        1       0       0
  C2 · Value chain · rol estratégico         0        0       1       0
  C3 · Trust services (4 objetivos)          1        1       1       0
  C4 · Frameworks de control COSO/COBIT      0        1       1       0
  C5 · Ciclos transaccionales                0        1       0       0
  C6 · Fraude y errores                      1        0       1       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      3        4       4       0

  Emergencias registradas: 11

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 implementa defensa en profundidad: Verificador separado del Motor
  (motor.py:104), cadena hash de eventos con verificación
  (event_store.py:225-282), máquina de estados con precondiciones
  (maquina_estados_asiento.py), separación H1/H2 (evita que el
  constructor sea el que decide). Coherente con Romney en trust services
  integridad y controles.

D · Divergencia
  Romney trata el AIS como sistema de información con frameworks
  declarados (COSO, COBIT), 4 trust services, value chain, y 3 ciclos
  transaccionales. E3 no declara ninguno de esos marcos. No hay
  modelado REA explícito (recurso-evento-agente) — hay TipoEvento y
  event_store genéricos.

E · Emergencia
  E3 tiene integridad sólida (cadena hash, verificador, máquina de
  estados) pero no tiene confidencialidad, privacidad, ni declaración
  de disponibilidad. Confirma parcialmente Patrón A (declaración
  parcial) y amplifica el hallazgo de NIST: falta la segunda capa
  criptográfica (confidencialidad/privacidad).

E · Enriquecimiento
  Romney aporta a E3 cinco casillas nuevas: (i) autodeclaración como
  AIS; (ii) value chain; (iii) modelado REA; (iv) adopción explícita de
  COSO/COBIT; (v) declaración de fraude como amenaza. E3 resiste en
  integridad y defensa en profundidad, pero no se declara dentro de
  ninguno de los marcos estándar de la disciplina SIC.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Romney (15th ed.) × SCFV_DSR E3.
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
  Constancia: acta 6.0.19 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

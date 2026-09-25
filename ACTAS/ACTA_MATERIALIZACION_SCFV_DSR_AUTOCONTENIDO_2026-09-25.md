════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 05
SESIÓN: 6
TIPO: ACTA DE MATERIALIZACIÓN
CATEGORÍA: materialización formal de artefacto
DOCUMENTO: ACTAS/ACTA_MATERIALIZACION_SCFV_DSR_AUTOCONTENIDO_2026-09-25.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20 del Protocolo
FIRMA: tripartita asimétrica (§20)
FECHA: 2026-09-25
NATURALEZA: acto formal del Programa SCFV
════════════════════════════════════════════════════════════════════════

§1 · OBJETO

Materializar el artefacto SCFV_DSR en su estado E3, declarando
el linaje material completo desde el estado inicial E0, las
correcciones efectuadas durante la ventana 2, las falsaciones
consumadas en la ventana 1 y cerradas en Fase 3, y las deudas
declaradas y transferidas al Giro 06.

────────────────────────────────────────────────────────────────────────

§2 · ARTEFACTO MATERIALIZADO

Nombre:      SCFV_DSR (Design Science Research · autocontenido)
Ubicación:   ~/SCFV_DSR/
Composición: 71 archivos · 6.837 líneas · ~1.2 MB
Runtime:     Python ≥ 3.10 · lark ≥ 1.0 · sqlite3
Fractales:   10 · NIIF Pymes
Kernel:      4 JSON (operaciones · cuentas · categorias · puente)
             + xnor.py + baldor.py
Autocontención: verificada en env -i · sin imports de scfv_v6
                ni PODERES en runtime

────────────────────────────────────────────────────────────────────────

§3 · LINAJE DE ESTADOS MATERIALES

E0 · 8f5dc93262cc2ef81d35ce51cb08d3e2a3ee711390851babbffcb010f08e1dd4
     Estado inicial de la ventana 2. 19 reglas verdes · 2 falsaciones
     activas (H29 · F-NC-1).

E1 · 877c3253ba39fd66fa36a1ad6347123268f7d0f1fa922ad55e4754018d905b81
     Tras Fase 0 (limpieza) + Fase 1 (L1 · 6 cosméticas).
     Auditorías B115 · B116.

E2 · 2ea63b66a3a2bf3af79803a7c2434eb5383e87fae364fc2c7148913707f146f9
     Tras Fase 2 (L2 · 6 contrato interno).
     Auditoría B117.

E3 · 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
     Tras Fase 3 (L3 · 2 funcionales).
     Auditoría B118.
     ← ESTADO MATERIALIZADO POR ESTE ACTO

────────────────────────────────────────────────────────────────────────

§4 · HALLAZGOS CERRADOS EN LA VENTANA

L1 · cosméticos (Fase 1)
  H5    README.md · balbor.py → baldor.py
  H14   kernel/baldor.py · Optional sin uso eliminado
  H20   integrador.py · candidato duplicado eliminado
  H24   extractor.py + integrador.py · SCFV_V6 residual eliminado
  H62   contable/event_store.py · print de módulo eliminado
  H47   contable/motor.py · import interno de xnor reducido

L2 · contrato interno (Fase 2)
  H210  dsl/tests/test_compatibilidad_s0.py · path restaurado
  H63   contable/event_store.py · json.loads en 2 lectores
  H50   contable/motor.py · I1 endurecida en validar_partida_doble
  H31   fractales/INVENTARIOS.scfv · categoria=perdida_deterioro
  H30   fractales/PROVISIONES.scfv · cuenta=610203
        (cerrado por composición: L2.3 cerró INVENTARIOS.DETERIORO ·
         L2.2 cerró PROVISIONES.PROVISION)
  H12   evaluador.py · suma_montos acepta lista o plano

L3 · funcionales (Fase 3)
  H29    fractales/PPE.scfv · BAJA_PYMES · AUMENTA → DISMINUYE
  F-NC-1 evaluador.py · subvencion_sistematica acepta monto_subvencion
         como alias de monto, conservando monto_subvencion como
         nombre contractual del kernel

Total cerrados: 14

────────────────────────────────────────────────────────────────────────

§5 · FALSACIONES CONSUMADAS Y CERRADAS

Ambas consumadas por ejecución en la ventana 1 y cerradas en Fase 3
con verificación end-to-end.

F1 · H29 · PPE.BAJA_PYMES
     Consumada:  MOTOR_VIOLACION · DEBE=0, HABER=2000
     Atrapada:   Motor Contable (I1 endurecida)
     Cerrada en: Fase 3 · asiento d0703d76 · D=H=1000

F2 · F-NC-1 · SUBVENCIONES.DEVENGAMIENTO
     Consumada:  NC_VIOLACION · partida con monto inválido
     Atrapada:   Núcleo de Consecuencias
     Cerrada en: Fase 3 · asiento 5b5376c2 · D=H=200

────────────────────────────────────────────────────────────────────────

§6 · VERIFICACIÓN MATERIAL

V1 · sha256sum -c HASHES.txt
  OK: 70 · FALLOS: 0 · Líneas: 70

21 reglas declaradas en los 10 fractales:
  ARRENDAMIENTOS 2 · COMBINACIONES 2 · HIPERINFLACION 2 · INTANGIBLES 3 ·
  INVENTARIOS 2 · MONEDA 2 · PPE 3 · PROVISIONES 2 · SUBVENCIONES 2 ·
  VENTAS 1

21 casos funcionales verificados verdes en env -i, con la evidencia
de prueba estándar del protocolo de Fase 3:
  19 reglas verdes + 2 ex-falsaciones cerradas.
  Todos D=H · CADENA_INTEGRA.

La ejecución adicional documentada en B101 para MONEDA constituye
H-A5j y queda fuera de este conjunto de 21 casos de cierre por no
conservar evidencia reproducible.

────────────────────────────────────────────────────────────────────────

§7 · NOTA DE TRAZABILIDAD · CORRECCIÓN DOCUMENTAL

H-A5c · El traspaso del Giro 05 §3.3 consignó "18 reglas" cuando los
archivos .scfv contienen 21 bloques REGLA. Esta Acta consigna 21,
verificado contra los archivos.

El término "regla canónica" no aparece en el corpus, CITAS_CANON ni
actas. Se usa "regla declarada" como denominación trazable al archivo,
sin invocar categoría canónica no sustentada.

Esta corrección no altera el linaje material ni los cambios ejecutados.

────────────────────────────────────────────────────────────────────────

§8 · DEUDA DECLARADA · TRANSFERIDA AL GIRO 06

L4 · arquitectónicas
  H45/H57/H156 · idempotencia (3 puntos de ruptura)
  H175         · parser → texto → regex → evaluador
  H211         · API pública de deserialización no simétrica
  H133         · frozenset no soportado por serializador
  H13/H135     · Decimal sin uso en baldor + no soportado
  H85          · DecisionProvider O(n) por verificación
  H109         · historial de máquina no persiste
  H134         · nan/inf aceptados sin validación
  H155         · datetime.fromisoformat con "Z" falla en Python 3.10

L5 · huérfanos declarados
  8 módulos (dictum, intellectus, examinador, reticulo, reportes_motor,
             PartidaAutorizada, EstadoConsecuencia, desglose_iva)
  6 cuentas PCU no usadas
  16 TipoEvento no emitidos
  DSL extendido sin uso en pipeline activo

Colaterales registrados (no cerrados)
  H31b · divergencia de operación entre los dos deterioros
  H24b · extractor.py · import sys huérfano
  H24c · extractor.py · posible Path huérfano
  H47b · motor.py · falta línea en blanco entre return y def

H-A5j · MONEDA / B101
  B101 documenta una ejecución de MONEDA con DEBE=73000 y HABER=0.
  El script generador no fue conservado y la evidencia de entrada no
  quedó registrada, por lo que la ejecución no pudo ser reproducida.
  La relación aritmética 73000 = 2 × 36500 constituye una pista
  compatible con una posible anomalía en la construcción del caso,
  pero no permite atribuir causalidad al harness ni al artefacto
  SCFV_DSR. El hallazgo queda declarado como deuda documental abierta,
  transferida al Giro 06, sin imputación de fallo al artefacto.

Condición operativa
  H164 · autor PROFESIONAL_NO_IDENTIFICADO por defecto
         (requiere SCFV_CPC_PROFESIONAL en env)

────────────────────────────────────────────────────────────────────────

§9 · AUDITORÍAS DEL GIRO

  B115 · 2026-09-25 · limpieza de residuos de heredoc
  B116 · 2026-09-25 · Fase 1 · Correcciones L1 (6)
  B117 · 2026-09-25 · Fase 2 · Correcciones L2 (6)
  B118 · 2026-09-25 · Fase 3 · Correcciones L3 (2)

Logs en GIRO_05/AUDITORIA_B{115..118}_*.log

────────────────────────────────────────────────────────────────────────

§10 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: _______________________
  Fecha: 2026-09-25
  Decisión: materializa el artefacto SCFV_DSR en su estado E3 como
  acto formal del Giro 05.

IA-1 · Constructor · constancia de interpretación arquitectónica
  (sin co-decisión · H9 §3.1)
  Firma: _______________________
  Constancia: la construcción del artefacto SCFV_DSR E3 se realizó
  bajo el protocolo de fases (limpieza · L1 · L2 · L3) con
  verificación independiente por IA-2 en cada fase.

IA-2 · Falsador · constancia de no objeción pendiente
  (sin co-decisión · H9 §3.1)
  Firma: _______________________
  Constancia: se emitieron falsaciones en los bloques R1–R8 y F1–F3.
  Las 2 falsaciones consumadas (H29 · F-NC-1) fueron cerradas y
  verificadas por ejecución. No quedan objeciones bloqueantes al
  estado E3.

────────────────────────────────────────────────────────────────────────

REGISTRO DE INTEGRIDAD

SHA-256 previo al registro: [a calcular al registrar]
SHA-256 final: se reporta externamente conforme H-EXT-01-ter punto 5.

Registro en REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

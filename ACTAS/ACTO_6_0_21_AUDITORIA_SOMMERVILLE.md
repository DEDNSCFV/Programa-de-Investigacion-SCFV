════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON SOMMERVILLE 2005
DOCUMENTO: ACTAS/ACTO_6_0_21_AUDITORIA_SOMMERVILLE.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Ian Sommerville
Obra: Ingeniería del software (7ª ed., 2005)
Raw: ~/.sommerville_raw.txt · 30.869 líneas · 2.432.761 bytes
SHA256 raw: c0f834de12c0fb92e086b9c52609cf504d34055145de858195fc2b316aa7f5a5
Naturaleza: ingeniería del software · proceso · V&V · configuración

Loci invocados:
  L95-96    · proceso del software / modelo de proceso
  L100      · atributos de un buen software
  L132      · modelos del proceso del software
  L230      · decisiones de diseño arquitectónico
  L348-370  · verificación y validación · planificación · automatización
  L437-448  · gestión de configuraciones · planificación · herramientas
  L1132     · atributos de un buen software
  L1355     · mantenibilidad, confiabilidad, eficiencia, aceptabilidad
  L3084     · ética del ingeniero
  L3588-3637 · especificación, diseño, implementación, evolución
  L9787-9823 · diseño arquitectónico
  L23595    · gestión de configuraciones detallada

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: pyproject.toml · README.md · dsl/README.md · grep global · estructura de tests · estructura de módulos · event_store.py · motor.py · maquina_estados_asiento.py

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Proceso del software declarado
  El proyecto declara su modelo de proceso (cascada, espiral,
  iterativo, ágil, etc.) — L95-96, L132.

C2 · Requerimientos explícitos
  Requerimientos funcionales y no funcionales documentados
  — L178, L5032, L5095.

C3 · Diseño arquitectónico
  La arquitectura del software se decide, documenta y justifica
  tempranamente — L230, L9800-9823.

C4 · Atributos del buen software
  Mantenibilidad · confiabilidad · eficiencia · aceptabilidad
  — L100, L1132, L1355.

C5 · Verificación y validación
  Proceso planificado de V&V con automatización de pruebas
  — L348-350, L370.

C6 · Gestión de configuraciones
  Control de versiones, línea base, planificación de cambios
  — L437-448, L23595.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · PROCESO DEL SOFTWARE DECLARADO

  C1-E1 · Modelo de proceso declarado
    Resultado: falla
    Cita: L96 "¿Qué es un modelo de procesos del software?"
    Ubicación: README.md (sin §proceso) · pyproject.toml (sin §proceso) ·
    dsl/README.md (sin §proceso) · grep global sin waterfall/espiral/
    agile

C2 · REQUERIMIENTOS EXPLÍCITOS

  C2-E1 · Requerimientos funcionales
    Resultado: falla
    Cita: L5095 "requerimientos del software"
    Ubicación: sin requirements.md · sin §requisitos en README.md

  C2-E2 · Requerimientos no funcionales
    Resultado: falla
    Cita: L5221 "Los requerimientos no funcionales... son aquellos
    requerimientos que..."
    Ubicación: sin §atributos de calidad declarados · sin §performance,
    §seguridad, §escalabilidad

  C2-E3 · Documento de requerimientos
    Resultado: falla
    Cita: L5087 "El documento de requerimientos del software"
    Ubicación: ausente

C3 · DISEÑO ARQUITECTÓNICO

  C3-E1 · Arquitectura declarada
    Resultado: parcial
    Cita: L9800 "el diseño arquitectónico es la primera etapa"
    Ubicación: README.md:26-39 (declara estructura de capas: kernel,
    epistemológico, contable, profesional, dsl, fractales,
    infraestructura) · sin ADR ni §arquitectura explícito

  C3-E2 · Justificación de decisiones arquitectónicas
    Resultado: parcial
    Cita: L9823 "la arquitectura del software puede servir"
    Ubicación: dsl/README.md:1-17 (§1 Propósito + §2 Autoridad) ·
    kernel/baldor.py:15-20 (frontera declarada) — hay justificación
    local pero no global

C4 · ATRIBUTOS DEL BUEN SOFTWARE

  C4-E1 · Mantenibilidad
    Resultado: parcial
    Cita: L1355 "mantenibilidad, confiabilidad, eficiencia y
    aceptabilidad"
    Ubicación: pyproject.toml (requires-python ">=3.10" — declaración de
    compatibilidad) · sin política de mantenibilidad · 6 tests sobre 29
    módulos (~17% de cobertura)

  C4-E2 · Confiabilidad
    Resultado: resiste
    Cita: L2329 "La propiedad más importante de un sistema crítico es su
    confiabilidad"
    Ubicación: event_store.py:225-282 (verificar_cadena → CADENA_INTEGRA)
    · motor.py:104 ("MOTOR_VIOLACION") · verificador_autorizacion.py
    (defensa en profundidad)

  C4-E3 · Eficiencia
    Resultado: no aplica
    Cita: L1355 "eficiencia"
    Ubicación: sin benchmarks · sin §performance

  C4-E4 · Aceptabilidad
    Resultado: falla
    Cita: L1355 "aceptabilidad"
    Ubicación: sin declaración de usuarios objetivo · sin §UAT

C5 · VERIFICACIÓN Y VALIDACIÓN

  C5-E1 · Planificación de V&V
    Resultado: falla
    Cita: L350 "Planificación de la verificación y validación"
    Ubicación: sin §plan de pruebas · sin §V&V

  C5-E2 · Suite de pruebas automatizadas
    Resultado: parcial
    Cita: L370 "Automatización de las pruebas"
    Ubicación: 6 tests (dsl/tests/* + soporte_minimo) sobre 29 módulos
    productivos (~17% de cobertura declarada)

  C5-E3 · Validación de sistemas críticos
    Resultado: parcial
    Cita: L175 (índice §9) "Especificación de sistemas críticos"
    Ubicación: maquina_estados_asiento.py (transiciones gobernadas) ·
    sin declaración de criticidad del sistema

C6 · GESTIÓN DE CONFIGURACIONES

  C6-E1 · Política de versiones
    Resultado: parcial
    Cita: L437 "Planificación de la gestión de configuraciones"
    Ubicación: pyproject.toml:7 ("version = 0.1.0") · kernel/*.json
    ("version": "1.0") — múltiples versiones sin política unificada

  C6-E2 · Línea base (baseline)
    Resultado: falla
    Cita: L437-448 (índice §29.1-29.5)
    Ubicación: 0 tags en 31 commits (reafirma hallazgo ProGit 6.0.15)

  C6-E3 · CHANGELOG
    Resultado: falla
    Cita: L448 "Herramientas CASE para gestión de configuraciones"
    Ubicación: sin CHANGELOG/VERSION/HISTORY en ~/SCFV_DSR/

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · Proceso del software                  0        0       1       0
  C2 · Requerimientos explícitos             0        0       3       0
  C3 · Diseño arquitectónico                 0        2       0       0
  C4 · Atributos del buen software           1        1       1       1
  C5 · Verificación y validación             0        2       1       0
  C6 · Gestión de configuraciones            0        1       2       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      1        6       8       1

  Emergencias registradas: 16

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 tiene arquitectura declarada por capas (README.md:26-39),
  confiabilidad fuerte (verificar_cadena, MOTOR_VIOLACION,
  verificación H2), fronteras declaradas localmente
  (dsl/README.md §2, baldor.py:15-20), y un pequeño núcleo de tests
  automatizados (6 tests).

D · Divergencia
  Sommerville exige declarar el proceso (cascada/iterativo/ágil),
  documentar requerimientos funcionales y no funcionales, planificar
  V&V, y gestionar configuraciones con baselines. E3 no declara
  ninguno de los cuatro. El ratio 6/29 tests indica baja cobertura
  declarada; no hay CHANGELOG, ni tags, ni política de versiones
  unificada (0.1.0 vs kernel 1.0).

E · Emergencia
  E3 tiene confiabilidad y arquitectura, pero no tiene proceso,
  requerimientos, V&V planificada, ni gestión de configuración.
  Es la confirmación del Patrón A desde el canon de ingeniería de
  software: no es solo la declaración parcial de alcance; es la
  ausencia de las cuatro capas declarativas que la disciplina SE
  considera obligatorias.

E · Enriquecimiento
  Sommerville aporta el marco completo de la ingeniería del software
  como casillas declarativas: proceso, requerimientos (funcionales y
  no funcionales), arquitectura justificada, atributos de calidad,
  V&V planificada, gestión de configuraciones. De las 6, E3 resiste
  1 (confiabilidad), parcial en 2 (arquitectura, V&V), falla en 3.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Sommerville 2005 × SCFV_DSR E3.
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
  Constancia: acta 6.0.21 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

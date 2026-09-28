════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON REYNOSO/KICILLOF
DOCUMENTO: ACTAS/ACTO_6_0_16_AUDITORIA_REYNOSO.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Carlos Billy Reynoso · Edgardo Kicillof
Obra: Introducción a la Arquitectura de Software (UBA · 2004)
Raw: ~/.reynoso_raw.txt · 10.794 líneas · 767.300 bytes
SHA256 raw: f13b7b62feafb1f433c4862c76dda64ecc57eae7d68e3fc5bc0c633a765c8226
Naturaleza: arquitectura de software · ADL · estilos · vistas

Loci invocados:
  L82-99      · §1 Arquitectura de Software (definiciones, delimitación)
  L100-140    · §2 Estilos · §3 ADLs · §4 Modelos de proceso · §5 Herramientas
  L445        · reutilización de patrones
  L528        · principios de diseño y evolución
  L576        · alto nivel de abstracción
  L1234       · arquitectónico = más alto nivel de abstracción
  L1286       · extracción, generalización, reutilización
  L1481       · AS evolucionó de la observación de principios
  L1593-1630  · comunicación mutua · decisiones tempranas · restricciones · reutilización · evolución · administración

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: dsl/grammar.lark · dsl/README.md · dsl/parser.py · kernel/baldor.py · kernel/xnor.py · grep global · README.md

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Alto nivel de abstracción
  La AS representa un alto nivel de abstracción común que
  conecta stakeholders — L576, L1593.

C2 · Decisiones tempranas de diseño
  La AS encarna las decisiones arquitectónicas tomadas
  tempranamente — L1599.

C3 · Restricciones constructivas · blueprints
  La descripción arquitectónica provee planos de construcción
  y delimita lo permitido — L1607.

C4 · Reutilización transferible
  La AS encarna modelos reutilizables entre sistemas
  análogos — L1612, L445.

C5 · Evolución declarada
  La AS expone las dimensiones de evolución del sistema
  — L1619, L528.

C6 · ADL como lenguaje formal
  Los lenguajes de descripción arquitectónica tienen criterios
  de definición propios — índice §3.1-3.6.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · ALTO NIVEL DE ABSTRACCIÓN

  C1-E1 · Nivel de abstracción declarado
    Resultado: falla
    Cita: L576 "un alto nivel de abstracción"
    Ubicación: grep global en ~/SCFV_DSR/scfv_dsr/ (0 coincidencias
    relevantes) · README.md (ausencia de §arquitectura)

  C1-E2 · Capas como abstracción funcional
    Resultado: resiste
    Cita: L1593 "Comunicación mutua. La AS representa un alto nivel de
    abstracción común"
    Ubicación: estructura scfv_dsr/{kernel, epistemologico, contable,
    profesional, dsl, fractales, infraestructura} · README.md:26-39

C2 · DECISIONES TEMPRANAS DE DISEÑO

  C2-E1 · Decisiones arquitectónicas no declaradas
    Resultado: parcial
    Cita: L1599 "Decisiones tempranas de diseño. La AS representa la
    encarnación de las decisiones"
    Ubicación: dsl/README.md:1-17 (declara propósito y frontera, no
    historial de decisiones) · sin ADR

C3 · RESTRICCIONES CONSTRUCTIVAS · BLUEPRINTS

  C3-E1 · Fronteras declaradas explícitamente
    Resultado: resiste
    Cita: L1607 "Restricciones constructivas. Una descripción arquitectónica
    proporciona blueprints"
    Ubicación: dsl/README.md:16-28 ("NO constituye por sí mismo:
    autoridad normativa, decisión profesional, motor contable") ·
    kernel/baldor.py:15-20 ("NO decide DEBE/HABER")

  C3-E2 · Grammar como blueprint formal
    Resultado: resiste
    Cita: L1607 "blueprints"
    Ubicación: dsl/grammar.lark:1-51 (gramática LALR completa con
    tokens CONTEXTO/MANDANTE/FRACTAL/CONTRATO/INVARIANTE/
    ASIENTO_DECLARADO)

C4 · REUTILIZACIÓN TRANSFERIBLE

  C4-E1 · Patrones reutilizables declarados
    Resultado: parcial
    Cita: L1612 "Reutilización, o abstracción transferible de un sistema"
    Ubicación: kernel/xnor.py:1-16 ("tres representaciones equivalentes de
    la misma regla estructural") · sin declarar patrón reutilizable

  C4-E2 · Sin catálogo de patrones
    Resultado: falla
    Cita: L445 "reutilización de patrones guarda estrecha relación con la
    tradición del diseño concreto"
    Ubicación: ausencia de catálogo de patrones en README.md ·
    grep global sin coincidencias

C5 · EVOLUCIÓN DECLARADA

  C5-E1 · Dimensiones de evolución
    Resultado: falla
    Cita: L1619 "Evolución. La AS puede exponer las dimensiones a lo
    largo de las cuales puede [evolucionar]"
    Ubicación: sin declaración de roadmap arquitectónico ·
    CHANGELOG inexistente · README.md (ausencia)

  C5-E2 · Versionado semántico de modelos
    Resultado: resiste
    Cita: L528 "principios que orientan su diseño y evolución"
    Ubicación: modelos.py (F3B.3-D) · dsl/README.md (§4 invariantes del
    módulo) · kernel/*.json ("version": "1.0", "reglas": aditivo/versionado)

C6 · ADL COMO LENGUAJE FORMAL

  C6-E1 · ADL-SCFV declarado
    Resultado: resiste
    Cita: L101-105 "Lenguajes de descripción arquitectónica (ADLs)"
    Ubicación: dsl/grammar.lark · dsl/README.md:1 ("Gramática extendida y
    parser ADL-SCFV")

  C6-E2 · Criterios de definición del ADL
    Resultado: parcial
    Cita: L103 "Criterios de definición de un ADL"
    Ubicación: dsl/README.md:1-60 (declara propósito, entradas/salidas,
    invariantes, dependencias permitidas/prohibidas; no cita criterios
    ADL estándar de la literatura)

  C6-E3 · Modelos computacionales declarados
    Resultado: falla
    Cita: L106 "Modelos computacionales y paradigmas de modelado"
    Ubicación: ausencia en dsl/README.md · grammar.lark sin §modelo
    computacional explícito

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · Alto nivel de abstracción             1        0       1       0
  C2 · Decisiones tempranas                  0        1       0       0
  C3 · Restricciones constructivas           2        0       0       0
  C4 · Reutilización transferible            0        1       1       0
  C5 · Evolución declarada                   1        0       1       0
  C6 · ADL como lenguaje formal              1        1       1       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      5        3       4       0

  Emergencias registradas: 12

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 tiene ADL-SCFV funcional (grammar.lark), frontera declarada
  (dsl/README.md §2 "Autoridad" y §6 "Dependencias prohibidas"),
  invariantes del módulo (§4), y modelo de versionado aditivo en los
  JSON del kernel (reglas.aditivo / reglas.versionado). El blueprint
  formal existe.

D · Divergencia
  Reynoso/Kicillof tratan la AS como disciplina que declara
  explícitamente: nivel de abstracción, decisiones tempranas, dimensiones
  de evolución, catálogo de patrones. E3 no declara esos cuatro puntos.
  La ausencia no es funcional — el código se ejecuta — es declarativa.

E · Emergencia
  E3 hace arquitectura sin declararse arquitectura. Coincide con el
  Patrón B detectado por Lakatos, Mandelbrot, Hevner y Popper.
  Reynoso/Kicillof lo confirman desde un canon de AS explícita.
  El vocabulario "componente / conector / estilo" está ausente del
  código (grep devuelve 0 coincidencias relevantes).

E · Enriquecimiento
  Reynoso/Kicillof dan a E3 tres casillas: (i) las decisiones
  arquitectónicas tempranas deberían registrarse como ADR; (ii) la
  evolución del sistema debería declararse, no inferirse; (iii) el ADL
  debería citar criterios estándar (Medvidovic & Taylor 2000, etc.) para
  autocualificarse. E3 tiene 3 de los 6 criterios fuertes (abstracción,
  restricciones, ADL formal), pero le faltan los 3 declarativos.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Reynoso/Kicillof 2004 × SCFV_DSR E3.
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
  Constancia: acta 6.0.16 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

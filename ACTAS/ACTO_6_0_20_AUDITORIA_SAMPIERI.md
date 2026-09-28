════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON SAMPIERI 2018
DOCUMENTO: ACTAS/ACTO_6_0_20_AUDITORIA_SAMPIERI.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Roberto Hernández-Sampieri
Obra: Metodología de la investigación: las rutas cuantitativa, cualitativa y mixta
Raw: ~/.sampieri_raw.txt · 45.863 líneas · 3.573.525 bytes
SHA256 raw: ead94ac047d7ec5dea49ace201c8481c3b43b3a4e27d2eca149c10840e6d9939
Naturaleza: metodología de la investigación · 3 rutas · diseños

Loci invocados:
  L418-639 · índice de las 5 partes
  L424-426 · las 3 rutas de la investigación
  L446-458 · planteamiento del problema cuantitativo
  L474-505 · alcance · hipótesis
  L510-534 · diseño y muestra
  L542-552 · recolección y análisis
  L562-567 · fases del proceso cuantitativo
  L630     · reporte de resultados

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: README.md · dsl/README.md · dsl/tests/* · BIBLIOTECA/INVENTARIO.md · ACTAS/ACTA_ACTIVACION_HEVNER_GIRO_03.md · grep global en ACTAS/GIRO_04/GIRO_05/GIRO_06

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Declaración de ruta
  Toda investigación se declara en una de tres rutas:
  cuantitativa, cualitativa o mixta — L418-426.

C2 · Planteamiento del problema
  El problema se plantea explícitamente antes de investigar
  — L446-458.

C3 · Marco teórico
  Revisión de literatura y antecedentes como fase explícita
  — L472-473.

C4 · Hipótesis
  La ruta cuantitativa formula hipótesis (nula, alternativa,
  de investigación) — L488-505.

C5 · Diseño declarado
  El diseño (experimental, no experimental, etc.) se declara
  antes de recoger datos — L510-534.

C6 · Reporte de resultados
  La investigación culmina en un reporte explícito — L630.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · DECLARACIÓN DE RUTA

  C1-E1 · Ruta metodológica declarada
    Resultado: falla
    Cita: L418 "Parte 1. Las rutas de la investigación"
    Ubicación: README.md (no declara ruta) ·
    ACTA_ACTIVACION_HEVNER_GIRO_03.md:42 ("No se adopta DSR como
    metodología rectora")

  C1-E2 · DSR como marco parcial
    Resultado: parcial
    Cita: L418 (declaración de ruta)
    Ubicación: README.md:3 ("Artefacto Design Science Research") —
    declara DSR sin integrarlo a las rutas de Sampieri

C2 · PLANTEAMIENTO DEL PROBLEMA

  C2-E1 · Problema de investigación
    Resultado: parcial
    Cita: L446 "El planteamiento del problema en la ruta cuantitativa"
    Ubicación: README.md (declara propósito funcional, no pregunta de
    investigación) · ACTAS de giro (registran actividad, no planteamiento)

C3 · MARCO TEÓRICO

  C3-E1 · Revisión de literatura materializada
    Resultado: resiste
    Cita: L472-473 "¿Qué es el marco teórico? … ¿Cuál es la utilidad del
    marco teórico?"
    Ubicación: BIBLIOTECA/INVENTARIO.md (41 entradas · 6 secciones) ·
    BIBLIOTECA/*/CITAS.md (787 B para Popper, etc.) · GIRO_05,
    GIRO_06 (registros de auditoría)

  C3-E2 · Declaración explícita de marco teórico
    Resultado: falla
    Cita: L471 "¿El marco teórico es necesario en cualquier
    investigación?"
    Ubicación: README.md (sin §marco teórico) · sin docs/metodología.md

C4 · HIPÓTESIS

  C4-E1 · Hipótesis operativas (H1/H2)
    Resultado: resiste
    Cita: L488-505 "Formulación de hipótesis en la ruta cuantitativa"
    Ubicación: modelos.py (PropuestaH1) · generador_propuesta.py
    (construcción de PropuestaH1) · h2.py (DecisionProfesional H2)

  C4-E2 · Hipótesis metodológicas declaradas (nula/alternativa)
    Resultado: falla
    Cita: L498-499 "¿Qué son las hipótesis nulas? … hipótesis
    alternativas?"
    Ubicación: sin declaración de hipótesis nula/alternativa de la
    investigación · grep global sin "hipótesis nula" ni "hipótesis
    alternativa"

C5 · DISEÑO DECLARADO

  C5-E1 · Diseño de investigación
    Resultado: falla
    Cita: L510-511 "Concepción o elección del diseño de investigación en
    la ruta cuantitativa"
    Ubicación: sin documento de diseño de investigación · sin
    §metodología en README.md

  C5-E2 · Instrumentos de recolección
    Resultado: parcial
    Cita: L542-546 "instrumentos de medición o recolección de datos"
    Ubicación: dsl/tests/* (5 tests como instrumentos de verificación) ·
    sin §instrumentos ni protocolo declarado

C6 · REPORTE DE RESULTADOS

  C6-E1 · Reporte explícito
    Resultado: parcial
    Cita: L630 "Elaboración del reporte de resultados del proceso"
    Ubicación: ACTAS/ACTO_6_0_*.md (18 actas como reporte secuencial) ·
    REGISTRO_ACTOS.log (líneas acumuladas) · GIRO_05/AUDITORIA_B*.log
    (logs por bloque) — el reporte existe pero no se declara como tal

  C6-E2 · Reporte final consolidado
    Resultado: falla
    Cita: L713 "reporte de resultados del proceso cuantitativo y del
    proceso cualitativo"
    Ubicación: pendiente 6.0.CONV · sin informe global del programa

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · Declaración de ruta                   0        1       1       0
  C2 · Planteamiento del problema            0        1       0       0
  C3 · Marco teórico                         1        0       1       0
  C4 · Hipótesis                             1        0       1       0
  C5 · Diseño declarado                      0        1       1       0
  C6 · Reporte de resultados                 0        1       1       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      2        4       5       0

  Emergencias registradas: 11

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 tiene marco teórico materializado (BIBLIOTECA con 41 entradas),
  hipótesis operativas (H1/H2), y reporte secuencial (18 actas +
  REGISTRO_ACTOS.log). El corpus de auditoría es trazable.

D · Divergencia
  Sampieri exige declarar la ruta metodológica, el planteamiento del
  problema, el diseño de investigación, el reporte final. E3 no declara
  ninguno de los cuatro de manera explícita. La ACTA_ACTIVACION_HEVNER
  incluso declara explícitamente "No se adopta DSR como metodología
  rectora" — lo que deja el programa sin ruta declarada.

E · Emergencia
  E3 investiga sin declarar método. El Patrón B (principios implícitos
  no declarados) se cumple también a nivel metodológico, no solo
  técnico-arquitectónico. Sampieri es el quinto canon que lo detecta,
  desde la metodología de la investigación.

E · Enriquecimiento
  Sampieri aporta a E3 el vocabulario de las 3 rutas y los 6
  componentes del proceso. E3 hace algo análogo a una ruta mixta
  (cuantitativa por invariantes, cualitativa por interpretación
  contextual, DSR como marco), pero no la declara. La casilla
  declarativa "ruta metodológica" es la más urgente de las abiertas.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Sampieri 2018 × SCFV_DSR E3.
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
  Constancia: acta 6.0.20 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

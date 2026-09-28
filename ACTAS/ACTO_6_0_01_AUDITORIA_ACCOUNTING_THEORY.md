════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON ACCOUNTING THEORY 2004
DOCUMENTO: ACTAS/ACTO_6_0_01_AUDITORIA_ACCOUNTING_THEORY.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-25
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Accounting Theory — Paper-8, M.Com (Final)
Institución: Maharshi Dayanand University · Excel Books, 2004
Naturaleza: material educativo posgrado · tradición anglosajona + Commonwealth
Raw: ~/.accounting_theory_raw.txt · 35.669 líneas · 1.502.226 bytes
Función declarada: interlocutor metodológico anglosajón de teoría contable

Loci invocados:
  L385-390   · Moonitz · 5 funciones de la contabilidad
  L740-745   · postulados como bases contables
  L889-893   · postulado monetario
  L2720-2760 · serie ARS (Accounting Research Studies) 1961-1965
  L2824-2872 · proyecto marco conceptual FASB · 6 SFAC 1978-1985
  L3680-3713 · teorías descriptivas vs normativas
  L4023-4035 · enfoque matemático-axiomático
  L4891-4900 · postulados de Paton

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Postulados axiomáticos
  Moonitz (ARS No.1, 1961) y Paton enuncian postulados básicos que
  fundamentan la teoría contable. La contabilidad se apoya en
  "concepts, postulates, conventions, and assumptions" (L740-741).
  El postulado monetario es explícito (L889-891).

C2 · Distinción normativa / positiva
  Descriptive: describe sin juicio de valor, extrae teoría de la práctica
  (Grady · Sanders-Hatfield-Moore · Littleton · Ijiri) — L3690-3699.
  Normative: "tend to justify what ought to be, rather than what it is"
  (Canning · Paton · Sweeney · McNeal · Edwards-Bell · Sprouse-Moonitz)
  — L3700-3713.

C3 · Marco conceptual FASB / IASB
  FASB 1973 · proyecto marco conceptual · 6 SFAC 1978-1985.
  SFAC 1 Objectives · SFAC 2 Qualitative Characteristics ·
  SFAC 3 Elements · SFAC 4 Non-business · SFAC 5 Recognition and
  Measurement · SFAC 6 Elements — L2848-2872.

C4 · Enfoque matemático-axiomático
  "mathematical symbols are given to certain ideas and concepts"
  (L4025-4026). El enfoque aísla la parte lógica de la empírica
  (L4027-4029). Mattessich · Chambers · Ijiri (L4033-4035).

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · POSTULADOS

  C1-E1 · El artefacto declara un axioma puntual (XNOR contable)
    Resultado: no aplica · es axioma operativo, no postulado
    Cita: L740-741 "concepts, postulates, convention and assumptions...
          collectively known as accounting bases"
    Ubicación: scfv_dsr/kernel/xnor.py

  C1-E2 · El artefacto no declara postulados de entidad, continuidad
          ni estabilidad de la unidad de medida
    Resultado: falla
    Cita: L4894-4900 · Paton enuncia 6 postulados
    Ubicación: global (no existe declaración)

  C1-E3 · El artefacto aplica postulado monetario (VES funcional)
    Resultado: resiste
    Cita: L889-891 "money is regarded as the ubiquituous measuring unit"
    Ubicación: scfv_dsr/contable/motor.py · invariante I13

C2 · NORMATIVA / POSITIVA

  C2-E1 · El artefacto es explícitamente normativo
    Resultado: resiste
    Cita: L3700-3703 "Normative Theories tend to justify what ought
          to be, rather than what it is"
    Ubicación: scfv_dsr/kernel/operaciones.json · categorias.json

  C2-E2 · No hay componente descriptivo
    Resultado: no aplica
    Cita: L3690-3693 "describes a particular phenomenon as it is,
          without any value judgment"
    Ubicación: global

C3 · MARCO CONCEPTUAL

  C3-E1 · El artefacto adopta los 5 elementos del marco conceptual
          (activo · pasivo · patrimonio · ingreso · gasto)
    Resultado: resiste parcial
    Cita: L2862 "SFAC No. 3: Elements of Financial Statements of
          Business Enterprise, published in December, 1980"
    Ubicación: scfv_dsr/kernel/categorias.json · §elementos

  C3-E2 · Falta SFAC 1 (Objectives of Financial Reporting) y
          SFAC 2 (Qualitative Characteristics)
    Resultado: falla
    Cita: L2848-2857
    Ubicación: global (no declarados)

  C3-E3 · Falta SFAC 5 (Recognition and Measurement) explícito
    Resultado: falla
    Cita: L2867-2871
    Ubicación: parcialmente cubierto por operaciones.json
               pero no declarado como SFAC 5

C4 · MATEMÁTICO-AXIOMÁTICO

  C4-E1 · xnor.py es matemático-axiomático
    Resultado: resiste
    Cita: L4023-4025 "mathematical symbols are given to certain
          ideas and concepts"
    Ubicación: scfv_dsr/kernel/xnor.py (3 vistas equivalentes)

  C4-E2 · baldor.py computa sin axiomatizar
    Resultado: parcial
    Cita: L4026-4029 "the logical part of the theory can be
          abstracted and studied in isolation from the empirical part"
    Ubicación: scfv_dsr/kernel/baldor.py

  C4-E3 · El artefacto no axiomatiza el conjunto
    Resultado: falla
    Cita: L4032 "amenable to mathematical operations and
          independent proof"
    Ubicación: global

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                   Resiste  Parcial  Falla  No aplica
  ─────────────────────────────────────────────────────────────
  C1 · Postulados              1        0       1       1
  C2 · Normativa/positiva      1        0       0       1
  C3 · Marco conceptual        1        0       2       0
  C4 · Matemático-axiomático   1        1       1       0
  ─────────────────────────────────────────────────────────────
  Total                        4        1       4       2

  Emergencias registradas: 11

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  El artefacto resiste en sus componentes localmente correctos:
  XNOR como axioma puntual · VES funcional como postulado monetario
  aplicado · elementos del MC en categorias.json · enfoque normativo
  coherente con su naturaleza de motor.

D · Divergencia
  Accounting Theory trata "postulado" como categoría central y
  "marco conceptual" como sistema integrado. El E3 no usa postulados
  declarados y toma fragmentos del MC sin declarar sus SFAC.

E · Emergencia
  El E3 es normativo sin fundación declarada. Aplica normas NIIF/Pymes
  sin declarar los postulados sobre los que esas normas se apoyan.
  Esta ausencia es una deuda estructural del kernel.

E · Enriquecimiento
  La distinción descriptiva/normativa del raw ubica con claridad al
  E3 como normativo puro, sin componente descriptivo. Coherente con
  su naturaleza de motor de consecuencias.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Accounting Theory 2004 × SCFV_DSR E3.
No emite veredicto global de aptitud del artefacto.
No anticipa el diagnóstico L4/L5.
El diagnóstico es competencia exclusiva de ACTO 6.0.CONV.

────────────────────────────────────────────────────────────────────────

§8 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: DEDN · C.P.C. Nº 183594
  Fecha: 2026-09-25

IA-1 · Constructor · constancia de interpretación arquitectónica
  Firma: IA-1 · Constructor
  Constancia: acta 6.0.01 redactada conforme al protocolo 6.0 §5,
  con emergencias ancladas a loci del raw y a ubicaciones del E3.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

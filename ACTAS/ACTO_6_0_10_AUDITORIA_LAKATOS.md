════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON LAKATOS 1976+1989
DOCUMENTO: ACTAS/ACTO_6_0_10_AUDITORIA_LAKATOS.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Imre Lakatos
Obras:
  Proofs and Refutations (1976) — raw ~/.lakatos_raw.txt · 9.372 líneas
  La metodología de los programas de investigación científica (1989)
    — raw ~/.lakatos_metodologia_raw.txt · 11.438 líneas
Naturaleza: metodología de programas de investigación científica

Loci invocados:
  Proofs 1976:
    L69, L82  · method of proof and refutations
    L74       · increasing content by deeper proofs
    L91       · logical and heuristic refutations revisited
  Metodología 1989:
    L239      · programa de investigación
    L244-246  · núcleo firme protegido por cinturón protector
    L247      · heurística
    L264      · progresivo vs regresivo
    L290-291  · programas progresivos generan hechos nuevos

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Programa de investigación
  La unidad de evaluación científica es el programa, no la
  hipótesis aislada. Tiene núcleo firme, cinturón protector,
  heurística — L239-247.

C2 · Núcleo firme vs cinturón protector
  El núcleo firme está protegido por el cinturón de hipótesis
  auxiliares — L244-246.

C3 · Progresivo vs regresivo
  Un programa progresivo descubre hechos nuevos. Un programa
  regresivo solo fabrica teorías para defender el núcleo — L264,
  L290-291.

C4 · Método de pruebas y refutaciones
  Conjeturas → pruebas → refutaciones → teoremas con contenido
  creciente — L69, L82.

C5 · Contenido creciente por pruebas más profundas
  Cada prueba más profunda incrementa el contenido — L74.

C6 · Refutaciones lógicas vs heurísticas
  Distinción entre refutación lógica y refutación heurística
  — L91.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · PROGRAMA DE INVESTIGACIÓN

  C1-E1 · E3 forma parte del Programa de Investigación SCFV
    Resultado: resiste
    Cita: L239 "un programa de investigación"
    Ubicación: global

  C1-E2 · E3 no declara su núcleo firme
    Resultado: falla
    Cita: L244 "esas cuatro leyes sólo constituyen el núcleo firme"
    Ubicación: README.md

  C1-E3 · E3 tiene cinturones internos
    Resultado: parcial
    Cita: L246 "cinturón protector de hipótesis auxiliares"
    Ubicación: scfv_dsr/ cinturones

  C1-E4 · E3 no declara heurística propia
    Resultado: falla
    Cita: L247 "el programa tiene también una heurística"
    Ubicación: global

C2 · NÚCLEO FIRME vs CINTURÓN

  C2-E1 · Kernel JSON + Motor operan como núcleo firme de facto
    Resultado: parcial
    Cita: L244-245
    Ubicación: kernel/ + motor.py

  C2-E2 · El cinturón defensivo es cinturón protector de facto
    Resultado: parcial
    Cita: L246
    Ubicación: contable/

C3 · PROGRESIVO vs REGRESIVO

  C3-E1 · El Programa no declara si es progresivo o regresivo
    Resultado: falla
    Cita: L264 "investigación progresivo... pseudocientífico o regresivo"
    Ubicación: global

  C3-E2 · Cada giro agrega contenido nuevo (progresivo de facto)
    Resultado: resiste
    Cita: L290-291
    Ubicación: Giro 05-06

C4 · MÉTODO DE PRUEBAS Y REFUTACIONES

  C4-E1 · La falsación IA-2 implementa el método de pruebas
          y refutaciones
    Resultado: resiste
    Cita: L69 "method of proof and refutations"
    Ubicación: ACTAS/ registros

C5 · CONTENIDO CRECIENTE

  C5-E1 · Cada giro incrementa contenido sobre el anterior
    Resultado: resiste
    Cita: L74 "increasing content by deeper proofs"
    Ubicación: linaje Giro 01-06

C6 · REFUTACIONES LÓGICAS vs HEURÍSTICAS

  C6-E1 · E3 no distingue refutaciones lógicas de heurísticas
    Resultado: falla
    Cita: L91 "Logical and heuristic refutations revisited"
    Ubicación: global

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Programa                 1        1       2       0
  C2 · Núcleo/cinturón          0        2       0       0
  C3 · Progresivo/regresivo     1        0       1       0
  C4 · Pruebas/refutaciones     1        0       0       0
  C5 · Contenido creciente      1        0       0       0
  C6 · Refut. lógica/heurís.    0        0       1       0
  ──────────────────────────────────────────────────────────────
  Total                         4        3       4       0

  Emergencias registradas: 11

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  El Programa SCFV es un programa de investigación lakatosiano de
  facto. Núcleo firme (kernel + Motor + XNOR), cinturón protector
  (cinturones internos), heurística (falsación + verificación).

D · Divergencia
  Lakatos exige distinguir núcleo firme de cinturón explícitamente.
  E3 no lo hace. Funciona como programa sin declararse programa.

E · Emergencia
  E3 es lakatosiano sin saberlo. El patrón núcleo-cinturón-heurística
  aparece en su arquitectura pero no en su documentación. Es un
  hallazgo estructural: la arquitectura heredó un patrón que no
  declaró.

E · Enriquecimiento
  Lakatos da vocabulario para preguntar: es el Programa SCFV
  progresivo o regresivo. Sin respuesta declarada, el criterio
  no se puede aplicar.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Lakatos 1976+1989 × SCFV_DSR E3.
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
  Constancia: acta 6.0.10 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON COSMOVISIÓN 2004
DOCUMENTO: ACTAS/ACTO_6_0_05_AUDITORIA_COSMOVISION.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Dirección: Jesús Alberto Suárez Pineda
Obra: Cosmovisión Histórica y Prospectiva de la Contabilidad · Tomo I
Subtítulo: Arqueología e historia de la contabilidad
Ciudad: Bogotá, 2004
Raw: ~/.cosmovision_raw.txt · 11.140 líneas
Naturaleza: ancla genealógica · arqueología contable pre-Pacioli

Loci invocados:
  L464      · crítica al inicio en Pacioli
  L477      · Escuela Italiana · partida doble
  L489      · papel de la contabilidad en la sociedad moderna
  L621      · doble origen de la disciplina
  L743-744  · ruta Sumeria → Roma → Florencia → Venecia → Génova
  L827-837  · Pacioli como descriptor del método veneciano
  L871      · huellas del origen de la contabilidad
  L996-998  · serendipity arqueológica
  L4819     · función de la contabilidad en los estados

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Origen histórico de la contabilidad
  La contabilidad tiene doble origen documentado. Su ruta técnica
  pasa por Sumeria, Caldea, Egipto, Roma, Florencia, Venecia,
  Génova — L621, L743-744.

C2 · Escuelas y evolución del pensamiento contable
  La evolución técnica pasa por escuelas: Italiana clásica, legado
  de Pacioli por partida doble — L477, L741-754.

C3 · Función social de la contabilidad
  La contabilidad juega papel fundamental en la sociedad y en
  la administración de los estados — L489, L4819.

C4 · Pre-Pacioli vs Pacioli
  Comenzar en Pacioli deja de lado la evolución previa. Pacioli
  describió el método veneciano, no lo inventó — L464, L827-837.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · ORIGEN HISTÓRICO

  C1-E1 · E3 no declara origen ni contexto histórico
    Resultado: no aplica
    Cita: L621 "doble origen de la disciplina"
    Ubicación: global

  C1-E2 · E3 carece de narrativa genealógica del doble registro
    Resultado: falla
    Cita: L871 "las huellas del origen de la Contabilidad"
    Ubicación: global

C2 · ESCUELAS Y EVOLUCIÓN

  C2-E1 · E3 no declara escuela contable (anglosajona vs continental)
    Resultado: falla
    Cita: L477 "Escuela Italiana de la Contabilidad clásica"
    Ubicación: global

  C2-E2 · E3 adopta NIIF sin declararlo como elección de escuela
    Resultado: parcial
    Cita: L754 "evolucionando de la pragmática al pensamiento"
    Ubicación: kernel/categorias.json

C3 · FUNCIÓN SOCIAL

  C3-E1 · E3 no declara función social
    Resultado: no aplica
    Cita: L489 "papel fundamental en la sociedad moderna"
    Ubicación: global

  C3-E2 · E3 sirve a usuarios internos pero no los declara
    Resultado: parcial
    Cita: L4819 "jugó un papel importante en el funcionamiento
          de los estados"
    Ubicación: cli.py

C4 · PRE-PACIOLI VS PACIOLI

  C4-E1 · E3 es post-Pacioli puro sin marcar el paso
    Resultado: resiste
    Cita: L827-833 "Pacioli afirmó que constituye una descripción
          del método veneciano"
    Ubicación: motor.py + xnor.py

  C4-E2 · E3 no declara la arqueología de sus propios mecanismos
    Resultado: falla
    Cita: L464 "una cosmovisión que comience con Luca Pacioli
          deja de lado la evolución de"
    Ubicación: global

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Origen histórico         0        0       1       1
  C2 · Escuelas/evolución       0        1       1       0
  C3 · Función social           0        1       0       1
  C4 · Pre-Pacioli vs Pacioli   1        0       1       0
  ──────────────────────────────────────────────────────────────
  Total                         1        2       3       2

  Emergencias registradas: 8

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 usa partida doble correctamente (post-Pacioli). El motor
  aplica el método veneciano descripto por Pacioli.

D · Divergencia
  E3 no se ubica en ninguna tradición histórica. No declara
  de dónde viene ni a qué escuela responde.

E · Emergencia
  E3 opera como si la contabilidad no tuviera genealogía.
  Funciona sin declarar su tradición. La ausencia no es
  accidental — es constitutiva del enfoque "motor".

E · Enriquecimiento
  Cosmovisión da vocabulario para preguntar: qué implica que un
  motor contable ignore la historia disciplinar. No es error
  técnico, es déficit cultural declarado.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Cosmovisión 2004 × SCFV_DSR E3.
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
  Constancia: acta 6.0.05 redactada conforme al protocolo 6.0 §5,
  con emergencias ancladas a loci del raw y a ubicaciones del E3.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

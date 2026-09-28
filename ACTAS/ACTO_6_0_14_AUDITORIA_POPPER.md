════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON POPPER 1980
DOCUMENTO: ACTAS/ACTO_6_0_14_AUDITORIA_POPPER.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Karl R. Popper
Obra: La lógica de la investigación científica (5ª reimpresión, 1980)
Raw: ~/.popper_raw.txt · 22.039 líneas · 1.362.880 bytes
SHA256 raw: e81dc225885e039f6232d67cc9f74441d22efa159eee3350c78d49b22c961331
Naturaleza: epistemología · demarcación · falsabilidad

Loci invocados:
  L100-108   · índice cap. I
  L121-123   · cap. II (decisiones metodológicas)
  L151-155   · cap. IV (falsabilidad)
  L167-170   · cap. V (base empírica)
  L977       · enunciados universales
  L1234      · falsación revela
  L1266      · vocabulario falsar/falsable/falsador
  L1298-1306 · problema de la demarcación
  L1448      · criterio de demarcación propuesto
  L1656-1669 · asimetría verificabilidad/falsabilidad
  L1674-1680 · método empírico = exponer a falsación
  L1703-1706 · enunciados singulares disponibles
  L1716-1734 · enunciado básico
  L1915-1925 · base empírica e intersubjetividad
  L455       · tradición de auto-exégesis metodológica

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: dictum.py · intellectus.py · perceptum.py · models.py · evidencia.py · generador_propuesta.py · maquina_estados_asiento.py · test_invariant_def.py · test_contract_def.py · grep global

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Falsabilidad como criterio de demarcación
  El método empírico se caracteriza por exponer a falsación el
  sistema — L1448, L1679-1680.

C2 · Asimetría verificabilidad/falsabilidad
  Enunciados universales: falsables por contraejemplo, no
  verificables por acumulación — L1656-1669.

C3 · Enunciados básicos
  Enunciado singular que sirve de premisa en una falsación
  empírica — L1734.

C4 · Base empírica intersubjetiva
  La base empírica debe ser objetiva, contrastable
  intersubjetivamente — L1916-1918.

C5 · No hay enunciados últimos
  Todo enunciado científico es refutable en principio — L1922-1925.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · FALSABILIDAD COMO CRITERIO DE DEMARCACIÓN

  C1-E1 · Vocabulario popperiano
    Resultado: falla
    Cita: L106 "6. La falsabilidad como criterio de demarcación"
    Ubicación: grep global en ~/SCFV_DSR/scfv_dsr/ y README.md (vacío)

  C1-E2 · Criterio de demarcación declarado
    Resultado: falla
    Cita: L1448 "Mi criterio de demarcación, por tanto, lia de considerarse
    como"
    Ubicación: README.md (ausencia de §método)

  C1-E3 · Tests como falsación funcional
    Resultado: parcial
    Cita: L1680 "manera de exponer a falsación el sistema"
    Ubicación: test_invariant_def.py:7-13 · test_contract_def.py:7-21

  C1-E4 · Contratos DSL pre/post
    Resultado: parcial
    Cita: L1734 "enunciado que puede servir de premisa en una falsación
    empírica"
    Ubicación: test_contract_def.py:18-19 (VENTA pre="x > 0" post="y == 1")

C2 · ASIMETRÍA VERIFICABILIDAD/FALSABILIDAD

  C2-E1 · Precondiciones de transición como enunciado falsable
    Resultado: parcial
    Cita: L1734 "enunciación de un hecho singular"
    Ubicación: maquina_estados_asiento.py:53-75

  C2-E2 · Evaluación AND/OR sin declarar contrastación
    Resultado: parcial
    Cita: L103 "3. Contrastación deductiva de teorías"
    Ubicación: intellectus.py:14-30

C3 · ENUNCIADOS BÁSICOS

  C3-E1 · Evidencia con hash determinista
    Resultado: resiste
    Cita: L1916-1918 "base empírica… objetiva, es decir, contrastable
    intersubjetivamente"
    Ubicación: evidencia.py:44-45, 110, 160-169

  C3-E2 · Dictum sin declarar universalidad
    Resultado: parcial
    Cita: L977 "enunciados universales, tales como hipótesis o teorías"
    Ubicación: dictum.py:10-30

C4 · BASE EMPÍRICA INTERSUBJETIVA

  C4-E1 · Intersubjetividad declarada
    Resultado: falla
    Cita: L1918 "contrastables intersubjetivamente"
    Ubicación: README.md (ausencia)

  C4-E2 · Declaración de prohibición de alcance
    Resultado: resiste
    Cita: L1407 "trazar una línea divisoria entre los sistemas científicos
    y los metafísicos"
    Ubicación: maquina_estados_asiento.py:7 ("PROHIBIDO: No contiene
    lógica contable, fiscal ni normativa.")

C5 · NO HAY ENUNCIADOS ÚLTIMOS

  C5-E1 · Declaración de no-últimos
    Resultado: falla
    Cita: L1922 "no puede haber enunciados últimos en la ciencia"
    Ubicación: ausencia de declaración en E3

  C5-E2 · Postscript metodológico
    Resultado: falla
    Cita: L455 "Dos notas sobre inducción y demarcación, 1933-1934"
    Ubicación: README.md (ausencia de auto-exégesis metodológica)

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · Falsabilidad como criterio            0        2       2       0
  C2 · Asimetría verificab./falsab.          0        2       0       0
  C3 · Enunciados básicos                    1        1       0       0
  C4 · Base empírica intersubjetiva          1        0       1       0
  C5 · No hay enunciados últimos             0        0       2       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      2        5       5       0

  Emergencias registradas: 12

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 ejecuta estructura popperiana sin nombrarla: los tests DSL
  operan como falsación funcional (asserts que rompen el sistema);
  los contratos pre/post son enunciados falsables; la evidencia con
  hash determinista es base empírica objetivada; maquina_estados_asiento
  declara PROHIBIDO su alcance, trazando línea divisoria.

D · Divergencia
  Popper exige que el criterio de demarcación, la intersubjetividad
  y la no-última-instancia se declaren. E3 no declara ninguno de los
  tres en vocabulario popperiano ni en vocabulario equivalente.

E · Emergencia
  E3 hace contrastación sin declararse contrastacionista. Confirma y
  refuerza el Patrón B del traspaso ("aplicación implícita de principios
  no declarados"). Popper es el cuarto canon que lo detecta, tras
  Lakatos, Mandelbrot y Hevner.

E · Enriquecimiento
  Popper aporta el vocabulario que E3 no tiene: falsabilidad,
  enunciado básico, intersubjetividad y no-última-instancia.
  Son cuatro casillas donde E3 hace sin declarar. La ausencia no es
  funcional (E3 no falla en ejecución), es declarativa.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Popper 1980 × SCFV_DSR E3.
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
  Constancia: acta 6.0.14 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

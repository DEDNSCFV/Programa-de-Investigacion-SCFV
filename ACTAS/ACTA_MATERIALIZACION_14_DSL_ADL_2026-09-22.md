════════════════════════════════════════════════════════════════════════
ACTA DE MATERIALIZACIÓN — ACTO 14
Módulo de gramática extendida y parser ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)
Estado efectivo: MATERIALIZADO Y FIRMADO
Régimen: §19.3-bis del Protocolo de Revisión de Actos

Hash previo al registro: 7dac4cac52c6a9600cffbe54c33341b295479e56988e4263537a1f486cf93e14
Hash final registrado:   854eb838b08b65455eb00bd0358a1cd3904ac7be1bc312aedd7c0521153754dc
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

La presente acta registra la materialización del Acto 14
(GIRO_04/14_materializacion_dsl_adl.md) y de los artefactos del módulo
~/SCFV_DSR/dsl/ conforme a la especificación del Acto 13.

Cierra D-12.2 (implementación del parser extendido) y D-13.1 (verificación
efectiva de la construcción LALR).


────────────────────────────────────────────────────────────────────────
§2. EVIDENCIA DE EJECUCIÓN
────────────────────────────────────────────────────────────────────────

Fase A (README del módulo): emitido y aplicado.

Fase B (código + pruebas): ejecutado.

Suite de pruebas: 7 passed / 7 total (1.47 s).

Tests:
- test_grammar_lalr::test_lalr_construye: PASSED
- test_compatibilidad_s0::test_historico_parsea: PASSED
- test_contract_def::test_contract_minimo: PASSED
- test_contract_def::test_contract_completo: PASSED
- test_contract_def::test_contract_negativo: PASSED
- test_invariant_def::test_invariant_completo: PASSED
- test_asiento_declarado_def::test_asiento_minimo: PASSED

La construcción LALR se verificó mediante `lark.Lark(grammar, start="start",
parser="lalr")` sin excepción. No se observaron conflictos shift/reduce ni
reduce/reduce durante la construcción.

El número de estados del autómata no fue observable a través de la
interfaz pública de Lark 1.3.1; se registra la ausencia de observación,
conforme a §9 del Acto 14.


────────────────────────────────────────────────────────────────────────
§3. HASHES DEL MÓDULO MATERIALIZADO
────────────────────────────────────────────────────────────────────────

Acto 14 (documento):
  GIRO_04/14_materializacion_dsl_adl.md
  Hash previo:  cb63154a5c34626524ffe6d810861c410182fdd3d327bb049d1ae626a6e88269

Artefactos del módulo ~/SCFV_DSR/dsl/:

  README.md
  bd82d55eae8ec0d1c27d71ca0af37c1650cc4e5877e70117d2ca2eed200c47de

  grammar.lark
  4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7

  parser.py
  94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2

  __init__.py
  e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
  (archivo vacío)

  tests/__init__.py
  e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
  (archivo vacío)

  tests/test_grammar_lalr.py
  1469828d21c48ea2ff4cedc8764b87f15616f0a0892a7d8a5629b785a55ae6b9

  tests/test_compatibilidad_s0.py
  039d7aecfed4b490f6fd2480eb70341f5aec53fff59068988ba1d9938b4384bb

  tests/test_contract_def.py
  9344ecdc47afdde7bd0489d03ad01c993b7798536b09913f45ed5033e02380c0

  tests/test_invariant_def.py
  3a8cf8c773c07c370fe25a1599e1689dbf01a755609e370441afbe0dc5835269

  tests/test_asiento_declarado_def.py
  2f3f7ce3530e60d0757214958b3aaa1dfe365b64adea164fb59728d13aab9a18


────────────────────────────────────────────────────────────────────────
§4. VERIFICACIÓN DE NO REGRESIÓN SOBRE S0
────────────────────────────────────────────────────────────────────────

Los archivos fuente de S0 permanecen intactos tras la materialización:

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/grammar.lark
  3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/parser.py
  eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

Ambos coinciden con las baselines declaradas en el Acto 14 §2. S0 no
fue modificado.


────────────────────────────────────────────────────────────────────────
§5. ALCANCE
────────────────────────────────────────────────────────────────────────

La materialización del Acto 14:

- NO modifica S0.
- NO modifica grammar.lark ni parser.py de S0.
- NO modifica los 4 .scfv históricos.
- NO escribe .scfv extendidos (eso corresponde al Acto 15).
- NO cierra I-3.
- NO cierra D-12.3.
- NO cierra H-EMG-1 ni H-EMG-2.
- NO cierra Giro 04.

Los archivos del módulo viven exclusivamente en ~/SCFV_DSR/dsl/.


────────────────────────────────────────────────────────────────────────
§6. TRAZABILIDAD DEL CICLO BILATERAL
────────────────────────────────────────────────────────────────────────

Ciclo IA-1 (constructor) ↔ IA-2 (falsador).

Iteraciones del Acto 14:
- Versión A — borrador inicial. IA-2 emitió O-368 a O-376.
- Versión B — integración de las nueve observaciones. IA-2 emitió
  O-378, O-379, O-380 (no bloqueantes).
- Versión C — integración de O-378 a O-380. Aprobación del Operador.

Ejecución: Fase A (README) y Fase B (código + suite).

Durante la Fase B se detectó y corrigió una falla en
`_handle_contract` y `_handle_invariant` (extracción de campos por
iteración incremental, frágil ante campos opcionales ausentes).
Se reescribieron ambos handlers con extracción por posiciones de keywords.
Re-ejecución: 7/7 tests aprobados sin regresión.

Ninguna objeción activa al momento de la materialización.


────────────────────────────────────────────────────────────────────────
§7. ACTOS POSTERIORES
────────────────────────────────────────────────────────────────────────

D-12.3 (correspondencia arquitectura ↔ ejecución) permanece abierta;
corresponde al Acto 16.

D-13.2 (semántica extendida de asiento_declarado_def) permanece abierta.

La escritura de .scfv extendidos corresponde al Acto 15.


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD DEL ACTA
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 7dac4cac52c6a9600cffbe54c33341b295479e56988e4263537a1f486cf93e14
Hash final:              854eb838b08b65455eb00bd0358a1cd3904ac7be1bc312aedd7c0521153754dc

════════════════════════════════════════════════════════════════════════
FIN DEL ACTA — MATERIALIZACIÓN DEL ACTO 14
════════════════════════════════════════════════════════════════════════

════════════════════════════════════════════════════════════════════════
ACTA DE MATERIALIZACIÓN — ACTO 15
Escritura de documentos .scfv extendidos en ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)
Estado efectivo: MATERIALIZADO Y FIRMADO
Régimen: §19.3-bis del Protocolo de Revisión de Actos

Hash previo al registro: 34df6d3eae3016af4121d375faf0e0367fc94fa6b27c1e0d8dc50f4795f19704
Hash final registrado:   791543b2dc806d944e19a102de9ac985a4a12dbd6db5b96320bfe795a6ee0b0e
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

La presente acta registra la materialización del Acto 15
(GIRO_04/15_scfv_extendidos.md) y de los cuatro documentos .scfv
sintéticos en ~/SCFV_DSR/dsl/ejemplos/.

Cierra la parte de escritura documental de D-12.3.
La correspondencia arquitectura ↔ ejecución queda reservada al Acto 16.


────────────────────────────────────────────────────────────────────────
§2. EVIDENCIA DE EJECUCIÓN
────────────────────────────────────────────────────────────────────────

Verificación efectuada durante la materialización:

Documento                       Resultado  Claves observadas
ejemplo_contrato.scfv           PASS       contratos{CONTROL_VENTA}
ejemplo_invariante.scfv         PASS       invariantes{MONTO_POSITIVO}
ejemplo_asiento.scfv            PASS       asientos_declarados{VENTA}
ejemplo_integrado.scfv          PASS       contratos + invariantes + asientos_declarados

No-regresión sobre los cuatro históricos:

Archivo      5 claves históricas  3 claves extendidas vacías
ventas       presentes            vacías
compras      presentes            vacías
inventario   presentes            vacías
fiscal       presentes            vacías

Caso integrado: confirmado. Procesa simultáneamente CONTRATO, INVARIANTE y
ASIENTO_DECLARADO. Cierra el requisito declarado en Acto 14 §8.6, no
ejecutado conjuntamente por la suite de ese acto.

Sin invocación al Motor Contable. Sin escritura a Diario o Mayor.


────────────────────────────────────────────────────────────────────────
§3. HASHES DE LOS ARTEFACTOS MATERIALIZADOS
────────────────────────────────────────────────────────────────────────

Acto 15 (documento):
  GIRO_04/15_scfv_extendidos.md
  Hash previo: 35ce5516c73d9ae480ca4e34702f8491b2f5929e23379b7f22f0abcc292cb12d

Documentos .scfv en ~/SCFV_DSR/dsl/ejemplos/:

  ejemplo_asiento.scfv
  fef6d977c1dca957f0e834eef5ed3bfc0084eeace743e2185cf0c26a37f1bd17

  ejemplo_contrato.scfv
  3719c198119a3ce2e121d08128c3912882ed26b3a3052d0a72a3ad41db067dc4

  ejemplo_integrado.scfv
  8f44d360693514aa9af0c58198fd2166d975e91cf823ae148424cd8c7b6f1331

  ejemplo_invariante.scfv
  6de771eb8cacb3b83bcf189e230bfe5b81ee739e6530b12dde26adbabe5e82f8


────────────────────────────────────────────────────────────────────────
§4. VERIFICACIÓN DE NO REGRESIÓN
────────────────────────────────────────────────────────────────────────

Hashtags del módulo materializado en Acto 14, sin modificación:

  ~/SCFV_DSR/dsl/grammar.lark
  4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7

  ~/SCFV_DSR/dsl/parser.py
  94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2

Hashes de S0, sin modificación:

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/grammar.lark
  3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/parser.py
  eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

Hashes de los cuatro .scfv históricos, sin modificación:

  ventas     ba647a58f9e210bed46109bf52c2247d971ae5c7e91e8a663c8a826c08cde16f
  compras    9e834aa220d94945c617ec3f2e9be7999dcbfcb57d121c6ec161d2cc55cdd339
  inventario 016fb0d2123efbfcbd0e3185b4544200e437b837c21fd84d9749542f15b1d058
  fiscal     f7e37f713f178dba9b7d03623dfbb3211e3e011ad929986205972d4cfdad8d1a

Todos coinciden con las baselines declaradas.


────────────────────────────────────────────────────────────────────────
§5. TRAZABILIDAD DEL CICLO BILATERAL
────────────────────────────────────────────────────────────────────────

Ciclo IA-1 (constructor) ↔ IA-2 (falsador).

Iteraciones:
- Versión A — borrador inicial. IA-2 emitió O-381 a O-385.
- Versión B — integración de O-381 a O-385. IA-2 emitió O-386, O-387
  (bloqueantes) y O-388, O-389 (no bloqueantes).
- Versión C — integración de O-386 a O-389. IA-2 emitió O-390, O-391
  (no bloqueantes).
- Versión D — integración de O-390 y O-391. Aprobación del Operador.

Ninguna objeción activa al momento de la materialización.


────────────────────────────────────────────────────────────────────────
§6. ALCANCE DE LA MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

La materialización del Acto 15:

- NO modifica S0.
- NO modifica grammar.lark ni parser.py del módulo.
- NO modifica los cuatro .scfv históricos.
- NO cierra I-3.
- NO cierra D-12.3.
- NO cierra Giro 04.
- NO invoca al Motor Contable.
- NO escribe en Diario ni Mayor.


────────────────────────────────────────────────────────────────────────
§7. DEUDAS
────────────────────────────────────────────────────────────────────────

D-12.3 · correspondencia arquitectura ↔ ejecución · abierta · Acto 16.
D-13.2 · semántica extendida de asiento_declarado_def · abierta.
D-11.x · del Acto 11 (soporte mínimo U-SEQ-01).


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD DEL ACTA
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 34df6d3eae3016af4121d375faf0e0367fc94fa6b27c1e0d8dc50f4795f19704
Hash final:              791543b2dc806d944e19a102de9ac985a4a12dbd6db5b96320bfe795a6ee0b0e

════════════════════════════════════════════════════════════════════════
FIN DEL ACTA — MATERIALIZACIÓN DEL ACTO 15
════════════════════════════════════════════════════════════════════════

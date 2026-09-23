════════════════════════════════════════════════════════════════════════
ACTA DE MATERIALIZACIÓN — ACTO 16
Verificación de correspondencia arquitectura ↔ ejecución en ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)
Estado efectivo: MATERIALIZADO Y FIRMADO
Régimen: §19.3-bis del Protocolo de Revisión de Actos

Hash previo al registro: aba9df492fe29f7961fdc147393909c8cb95e9a93d4449efb932fa18fad61e2a
Hash final registrado:   875eeff11cacbb1491a0c2ccf241927ff81107e2f5d7db164b25457cdebab5a4
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

La presente acta registra la materialización del Acto 16
(GIRO_04/16_correspondencia_arquitectura_ejecucion.md).

El Acto 16 verifica la correspondencia entre:

- los tres constructos arquitectónicos declarados en Acto 10 §5.0-bis
  (CONTRATO, INVARIANTE, ASIENTO_DECLARADO);
- las tres producciones sintácticas del Acto 13 (contract_def,
  invariant_def, asiento_declarado_def);
- el parser extendido materializado en el Acto 14;
- los documentos sintéticos escritos en el Acto 15.

**Cierra D-12.3.**


────────────────────────────────────────────────────────────────────────
§2. EVIDENCIA EMPÍRICA
────────────────────────────────────────────────────────────────────────

Documentos extendidos:

  OK  ejemplo_contrato:    ['contratos']
  OK  ejemplo_invariante:  ['invariantes']
  OK  ejemplo_asiento:     ['asientos_declarados']
  OK  ejemplo_integrado:   ['contratos', 'invariantes', 'asientos_declarados']

Caso integrado: coexistencia de los tres constructos confirmada.
Cierra el requisito declarado en Acto 14 §8.6 (por contenido).

Documentos históricos:

  OK  ventas:      históricas=True extendidas_vacías=True
  OK  compras:     históricas=True extendidas_vacías=True
  OK  inventario:  históricas=True extendidas_vacías=True
  OK  fiscal:      históricas=True extendidas_vacías=True

Las cinco claves históricas (fractales, contexto, mandante, tetrada,
booleano) preservadas. Las tres claves extendidas vacías. Sin regresión.


────────────────────────────────────────────────────────────────────────
§3. HASHES DE VERIFICACIÓN
────────────────────────────────────────────────────────────────────────

Acto 16:
  Hash previo:   62947de4ee082c39ea0890afa8b1b63018abdc4cafbd0474a76c5751640b8f74
  Hash declarado: 57cfc8b5aa5bc45824e778799e69aa352b64349dd6fff2ab973244457da38793

Integridad post-verificación:

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/grammar.lark
  3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850

  ~/SCFV_S0_V1.0.0/PODERES/FORMAL/dsl/parser.py
  eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

  ~/SCFV_DSR/dsl/grammar.lark
  4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7

  ~/SCFV_DSR/dsl/parser.py
  94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2

Todos coinciden con las baselines declaradas. Sin modificación.


────────────────────────────────────────────────────────────────────────
§4. CIERRE DE D-12.3
────────────────────────────────────────────────────────────────────────

La deuda D-12.3 (correspondencia arquitectura ↔ ejecución) queda cerrada
por la evidencia consignada en §2 y §3, conforme a las condiciones
declaradas en el Acto 16 §9.

Las nueve condiciones se encuentran verificadas:

1. matrices §4-§6 establecen correspondencia estructural — CUMPLE.
2. caso integrado contiene los tres constructos — CUMPLE.
3. ejecución empírica §8 sin regresión — CUMPLE.
4. cinco campos históricos conservan su contenido — CUMPLE.
5. hashes conformes — CUMPLE.
6. sin tokens inventados — CUMPLE.
7. sin constructos sin declaración de origen — CUMPLE.
8. sin ejecución contable — CUMPLE.
9. sin escritura en Diario o Mayor — CUMPLE.


────────────────────────────────────────────────────────────────────────
§5. ALCANCE
────────────────────────────────────────────────────────────────────────

La materialización del Acto 16:

- NO modifica S0.
- NO modifica grammar.lark ni parser.py del módulo.
- NO modifica los cuatro .scfv históricos.
- NO cierra I-3.
- NO cierra Giro 04.
- NO resuelve D-13.2.
- NO cierra D-11.x.


────────────────────────────────────────────────────────────────────────
§6. DEUDAS ACTUALIZADAS
────────────────────────────────────────────────────────────────────────

D-12.1  cerrada por Acto 13.
D-12.2  cerrada por Acto 14.
D-12.3  **CERRADA POR ACTO 16**.
D-13.1  cerrada por Acto 14.
D-13.2  abierta.
D-11.x  abierta.
O-164 / U-SEQ-01  abierta.


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD DEL ACTA
────────────────────────────────────────────────────────────────────────

Hash previo al registro: aba9df492fe29f7961fdc147393909c8cb95e9a93d4449efb932fa18fad61e2a
Hash final:              875eeff11cacbb1491a0c2ccf241927ff81107e2f5d7db164b25457cdebab5a4

════════════════════════════════════════════════════════════════════════
FIN DEL ACTA — MATERIALIZACIÓN DEL ACTO 16
════════════════════════════════════════════════════════════════════════

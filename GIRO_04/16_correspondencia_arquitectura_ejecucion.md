════════════════════════════════════════════════════════════════════════
ACTA DE VERIFICACIÓN DE CORRESPONDENCIA
ARQUITECTURA ↔ EJECUCIÓN EN ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 16
Documento: GIRO_04/16_correspondencia_arquitectura_ejecucion.md
Versión: C
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN BLOQUEANTES.

Correcciones aplicadas sobre Versión B:
  O-401: §8.1 declara el estatuto de la evidencia empírica (producida en
         ciclo bilateral previo, reproducible por terceros).
  O-402: §10 nota al pie sobre el estado de verificación del checklist.
  O-403: §9 reformula la cláusula final —el cierre formal corresponde al
         veredicto IA-2 y a la materialización bajo §19.3-bis.

Estatuto: verifica correspondencia arquitectura ↔ ejecución.
Cierra D-12.3. No cierra I-3. No cierra Giro 04. No modifica S0.

Hash previo al registro: 62947de4ee082c39ea0890afa8b1b63018abdc4cafbd0474a76c5751640b8f74
Hash final registrado:   57cfc8b5aa5bc45824e778799e69aa352b64349dd6fff2ab973244457da38793
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

Verificar la correspondencia entre CONTRATO, INVARIANTE y ASIENTO_DECLARADO
declarados en Acto 10 §5.0-bis, sus producciones sintácticas (contract_def,
invariant_def, asiento_declarado_def) materializadas en el módulo del Acto
14, y sus instancias documentales (Acto 15).

Cierra D-12.3.

Nota de trazabilidad: en la materialización del Acto 14, §8.6 quedó
comprimido dentro de §8 sin encabezado independiente. La referencia a
Acto 14 §8.6 se realiza por contenido.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES
────────────────────────────────────────────────────────────────────────

Acto 10   22996478933e948ef190ee88b1d22a9c000052e36f7a4db7fa6911eed32ac5b4
Acto 13   3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee
Acto 14   8309e2fc0b31716579653f7d2cab2c9d49ad2a05f9e1bcf6a946b60839619869
Acto 15   49738e83b10e34ce68bbbcb1529876a43b8017e29efe9f474077020bf018abca

parser.py módulo     94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2
grammar.lark módulo  4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7

Documentos sintéticos:
ejemplo_contrato.scfv    3719c198119a3ce2e121d08128c3912882ed26b3a3052d0a72a3ad41db067dc4
ejemplo_invariante.scfv  6de771eb8cacb3b83bcf189e230bfe5b81ee739e6530b12dde26adbabe5e82f8
ejemplo_asiento.scfv     fef6d977c1dca957f0e834eef5ed3bfc0084eeace743e2185cf0c26a37f1bd17
ejemplo_integrado.scfv   8f44d360693514aa9af0c58198fd2166d975e91cf823ae148424cd8c7b6f1331


────────────────────────────────────────────────────────────────────────
§3. ESTATUTO DEL ACTO
────────────────────────────────────────────────────────────────────────

No modifica grammar.lark, parser.py, S0, históricos, Motor Contable,
Diario, Mayor.

§3.1. Nivel estructural
Los componentes de Acto 10 tienen representación en Acto 13 y en Acto 15.

§3.2. Nivel semántico delimitado
El parser verifica sintaxis y produce representación de datos. No valida
semántica contable. La separación tiene antecedente en Acto 11 §§10.3-10.4
y Acto 14 §7.4.


────────────────────────────────────────────────────────────────────────
§4. MATRIZ — CONTRATO
────────────────────────────────────────────────────────────────────────

Componente                Acto 10 §5.4     Acto 13 §5.1        Acto 15
nombre                    nombre           CONTRATO NAME       CONTROL_VENTA
objeto                    objeto           OBJETO: NAME        OBJETO: REGISTRO
precondiciones (cond.)    cuando corresp.  [PRE: expr]         PRE: VENTA
postcondiciones (cond.)   cuando corresp.  [POST: expr]        POST: VALIDADA
invariantes asociadas     invariantes      INVARIANTE: NAME+   INVARIANTE: MONTO_POSITIVO
elementos del sistema     elementos        ELEMENTO: NAME+     ELEMENTO: MONTO VENTA
evidencia (cond.)         cuando sosten.   [EVIDENCIA: NAME+]  EVIDENCIA: FACTURA

Correspondencia: 7/7 CORRESPONDE.

Evidencia material: ejemplo_contrato.scfv (hash en §2).


────────────────────────────────────────────────────────────────────────
§5. MATRIZ — INVARIANTE
────────────────────────────────────────────────────────────────────────

Componente                   Acto 10 §5.5    Acto 13 §6.1        Acto 15
objeto                       objeto          OBJETO: NAME        OBJETO: REGISTRO
expresión                    expresión       EXPRESION: expr     EXPRESION: MONTO
dominio                      dominio         DOMINIO: NAME       DOMINIO: REGISTRO
condición de satisfacción    satisfacción    SATISFACCION: expr  SATISFACCION: VALIDADA
procedimiento verificación   verificación    VERIFICACION: NAME  VERIFICACION: PRUEBA
evidencia                    evidencia       EVIDENCIA: NAME+    EVIDENCIA: FACTURA

Correspondencia: 6/6 CORRESPONDE.

Evidencia material: ejemplo_invariante.scfv (hash en §2).


────────────────────────────────────────────────────────────────────────
§6. MATRIZ — ASIENTO_DECLARADO
────────────────────────────────────────────────────────────────────────

Nivel                    Acto 10 §5.6        Acto 13 §7           Acto 15 §8
distinción vs REGISTRADO declarada           sin colisión         declarada
forma sintáctica         no fijada           ASIENTO_DECLARADO    conforme
                                             NAME ":" NAME+
relación con Motor       distinta            no ejecuta           no ejecuta

§6.1. Límite
No se atribuye a Acto 13 §7 una estructura de débito/crédito ni semántica
contable específica. La correspondencia es conceptual + forma mínima.

Evidencia material: ejemplo_asiento.scfv (hash en §2).


────────────────────────────────────────────────────────────────────────
§7. CASO INTEGRADO
────────────────────────────────────────────────────────────────────────

ejemplo_integrado.scfv contiene simultáneamente CONTRATO, INVARIANTE y
ASIENTO_DECLARADO. Hash: 8f44d360693514aa9af0c58198fd2166d975e91cf823ae148424cd8c7b6f1331.

Nota: §8.6 del Acto 14 fue subsección comprimida. La referencia se mantiene
por contenido.

Cadena:
  Acto 10 (declaración) → Acto 13 (sintaxis) → Acto 14 (parser) →
  Acto 15 (ejemplo_integrado.scfv) → Acto 16 (verificación).


────────────────────────────────────────────────────────────────────────
§8. VERIFICACIÓN EMPÍRICA
────────────────────────────────────────────────────────────────────────

§8.1. Estatuto de la evidencia

La evidencia empírica consignada a continuación procede de la verificación
efectuada durante el ciclo bilateral previo a la materialización. La
evidencia es reproducible por terceros contra los hashes consignados en §2
y §8.3.

§8.2. Documentos extendidos

OK  ejemplo_contrato:   ['contratos']
OK  ejemplo_invariante: ['invariantes']
OK  ejemplo_asiento:    ['asientos_declarados']
OK  ejemplo_integrado:  ['contratos', 'invariantes', 'asientos_declarados']

Caso integrado: coexistencia de los tres constructos confirmada.

§8.3. Documentos históricos

OK  ventas:     históricas=True extendidas_vacías=True
OK  compras:    históricas=True extendidas_vacías=True
OK  inventario: históricas=True extendidas_vacías=True
OK  fiscal:     históricas=True extendidas_vacías=True

Las cinco claves históricas (fractales, contexto, mandante, tetrada,
booleano) preservadas. Las tres claves extendidas vacías.

§8.4. Integridad de S0 y módulo

S0 grammar.lark   3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850
S0 parser.py      eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83
Módulo grammar    4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7
Módulo parser     94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2

Todos coinciden con las baselines. Sin modificación.


────────────────────────────────────────────────────────────────────────
§9. REGISTRO DE EVIDENCIA Y CONDICIONES
────────────────────────────────────────────────────────────────────────

Verificación                              Resultado      Evidencia
CONTRATO ↔ contract_def                   PASS           matriz §4
INVARIANTE ↔ invariant_def                PASS           matriz §5
ASIENTO_DECLARADO ↔ asiento_declarado_def PASS           matriz §6
Caso integrado                            PASS           §7
Cuatro ejemplos parsean                   PASS           §8.2
Cuatro históricos parsean                 PASS           §8.3
Cinco claves históricas preservadas       PASS           §8.3
Tres claves extendidas                    PASS           §8.2–§8.3
S0 intacto                                PASS           §8.4
Módulo intacto                            PASS           §8.4
Constructos no declarados                 ninguno        §§4–§7
Ejecución contable                        no existe      §12

Condiciones de cierre: las nueve condiciones de §9.1 quedan respaldadas por
la evidencia consignada. La constancia de cumplimiento efectivo corresponde
al veredicto de falsación IA-2 y a la materialización bajo §19.3-bis.


────────────────────────────────────────────────────────────────────────
§10. FALSACIÓN IA-2
────────────────────────────────────────────────────────────────────────

[x] correspondencia CONTRATO ↔ contract_def
[x] correspondencia INVARIANTE ↔ invariant_def
[x] correspondencia ASIENTO_DECLARADO ↔ asiento_declarado_def
[x] siete componentes de CONTRATO
[x] seis componentes de INVARIANTE
[x] correspondencia conceptual y sintáctica delimitada de ASIENTO_DECLARADO
[x] ejecución de los cuatro ejemplos
[x] ejecución de los cuatro históricos
[x] no regresión de las cinco claves históricas
[x] coexistencia de los tres constructos en el integrado
[x] cobertura de Acto 14 §8.6 por contenido
[x] hashes del módulo sin modificación
[x] elementos de S0 sin modificación
[x] ausencia de constructos no declarados
[x] ausencia de ejecución contable

Nota: los puntos anteriores fueron verificados por IA-2 durante la falsación
de la Versión A y re-verificados en la falsación de la Versión B. El cierre
formal corresponde a la materialización del Acto.


────────────────────────────────────────────────────────────────────────
§11. CONDICIONES DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

§19.3-bis del Protocolo de Revisión de Actos, incorporado por
ACTAS/ACTA_ENMIENDA_PROTOCOLO_19_3_BIS.md.

Dos dimensiones: verificación documental (§§4–§7) y verificación empírica
(§8).


────────────────────────────────────────────────────────────────────────
§12. LÍMITES
────────────────────────────────────────────────────────────────────────

No cierra I-3. No cierra Giro 04. No modifica S0, grammar, parser, históricos.
No redefine los constructos. No ejecuta operaciones contables. No atribuye
autoridad profesional al parser. No resuelve D-13.2.


────────────────────────────────────────────────────────────────────────
§13. DEUDAS
────────────────────────────────────────────────────────────────────────

D-12.3  cerrada por este Acto (evidencia §9)
D-13.2  abierta
D-11.x  abierta


────────────────────────────────────────────────────────────────────────
§14. CADENA DE ACTOS
────────────────────────────────────────────────────────────────────────

Acto 10 → Acto 13 → Acto 14 → Acto 15 → Acto 16 → cierre D-12.3.
Giro 04 no cerrado.


────────────────────────────────────────────────────────────────────────
§15. ESTADO
────────────────────────────────────────────────────────────────────────

VERSIÓN C — MATERIALIZADA.
O-401, O-402, O-403 aplicadas.


────────────────────────────────────────────────────────────────────────
§16. FIRMAS
────────────────────────────────────────────────────────────────────────

IA-1: Versión C materializada.
IA-2: APTO SIN BLOQUEANTES.
OPERADOR: Materializado y firmado.

────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 62947de4ee082c39ea0890afa8b1b63018abdc4cafbd0474a76c5751640b8f74
Acta de referencia:      ACTA_MATERIALIZACION_16_CORRESPONDENCIA_2026-09-22
Hash final:              57cfc8b5aa5bc45824e778799e69aa352b64349dd6fff2ab973244457da38793

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 16 — CORRESPONDENCIA ARQUITECTURA ↔ EJECUCIÓN — Versión C
════════════════════════════════════════════════════════════════════════

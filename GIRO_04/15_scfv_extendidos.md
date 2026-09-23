════════════════════════════════════════════════════════════════════════
ACTA DE ESCRITURA DE DOCUMENTOS ".scfv" EXTENDIDOS EN ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 15
Documento: GIRO_04/15_scfv_extendidos.md
Versión: D
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN BLOQUEANTES.

Correcciones sobre Versión C:
  O-390: §6 declara que la omisión de campos opcionales también está
         cubierta por la gramática, aunque no se ejemplifique.
  O-391: §9 declara que la referencia nominal del CONTRATO al INVARIANTE
         ilustra el mecanismo de referencia sin verificación de existencia
         (Acto 13 §5.3).

Estatuto: escribe documentos .scfv extendidos. No modifica grammar.lark
ni parser.py. No cierra D-12.3. No cierra Giro 04.

Hash previo al registro: 35ce5516c73d9ae480ca4e34702f8491b2f5929e23379b7f22f0abcc292cb12d
Hash final registrado:   49738e83b10e34ce68bbbcb1529876a43b8017e29efe9f474077020bf018abca
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO DEL ACTO
────────────────────────────────────────────────────────────────────────

Escribir documentos ".scfv" sintéticos que utilicen CONTRATO, INVARIANTE
y ASIENTO_DECLARADO, en ~/SCFV_DSR/dsl/ejemplos/.

Cierra la parte de escritura documental de D-12.3.
La correspondencia arquitectura ↔ ejecución queda reservada al Acto 16.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES
────────────────────────────────────────────────────────────────────────

Elemento                                    Hash SHA-256
Acto 14 declarado                           8309e2fc0b31716579653f7d2cab2c9d49ad2a05f9e1bcf6a946b60839619869
Acto 13 declarado                           3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee
parser.py del módulo                        94bdaa939fb4fa810815e13b69717fc856469479dd0d968b4b9b02bc676d9fa2
grammar.lark del módulo                     4129fca2f6f02ef7fb4b386f3a3bcd0369f74d9931c43d5cc38633b5f592e7e7

Documentos históricos (baseline):
ventas     ba647a58f9e210bed46109bf52c2247d971ae5c7e91e8a663c8a826c08cde16f
compras    9e834aa220d94945c617ec3f2e9be7999dcbfcb57d121c6ec161d2cc55cdd339
inventario 016fb0d2123efbfcbd0e3185b4544200e437b837c21fd84d9749542f15b1d058
fiscal     f7e37f713f178dba9b7d03623dfbb3211e3e011ad929986205972d4cfdad8d1a


────────────────────────────────────────────────────────────────────────
§3. ESTATUTO DEL ACTO
────────────────────────────────────────────────────────────────────────

No modifica grammar.lark, parser.py, S0, históricos, Motor Contable,
Diario, Mayor. Escritura declarativa y sintáctica.
No cierra D-12.3.


────────────────────────────────────────────────────────────────────────
§4. LOCUS DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

~/SCFV_DSR/dsl/ejemplos/
├── ejemplo_contrato.scfv
├── ejemplo_invariante.scfv
├── ejemplo_asiento.scfv
└── ejemplo_integrado.scfv


────────────────────────────────────────────────────────────────────────
§5. NATURALEZA DE LOS EJEMPLOS
────────────────────────────────────────────────────────────────────────

Sintéticos y declarativos. Cada documento porta cabecera literal:

# DOCUMENTO SINTÉTICO — Acto 15 · SCFV_DSR · Giro 04
# No representa operación económica real. Solo prueba sintáctica.


────────────────────────────────────────────────────────────────────────
§6. DOCUMENTO DE CONTRATO
────────────────────────────────────────────────────────────────────────

ejemplo_contrato.scfv conforme a contract_def de Acto 13 §5.1.

Ejemplo (con los tres campos opcionales presentes):

    # DOCUMENTO SINTÉTICO — Acto 15 · SCFV_DSR · Giro 04
    # No representa operación económica real. Solo prueba sintáctica.

    CONTRATO CONTROL_VENTA
    OBJETO: REGISTRO
    PRE: VENTA
    POST: VALIDADA
    INVARIANTE: MONTO_POSITIVO
    ELEMENTO: MONTO VENTA
    EVIDENCIA: FACTURA

O-390: la gramática admite también la omisión de PRE, POST y EVIDENCIA. La
producción del Acto 13 §5.1 usa `[ ... ]` para los tres campos. El ejemplo
del presente Acto los incluye todos, pero la omisión parcial o total de los
tres opcionales está igualmente cubierta por la gramática. No se ejemplifica
la omisión en este Acto; su verificación empírica está cubierta por la
prueba test_contract_minimo de la suite del Acto 14.


────────────────────────────────────────────────────────────────────────
§7. DOCUMENTO DE INVARIANTE
────────────────────────────────────────────────────────────────────────

ejemplo_invariante.scfv conforme a invariant_def de Acto 13 §6.1.

    # DOCUMENTO SINTÉTICO — Acto 15 · SCFV_DSR · Giro 04
    # No representa operación económica real. Solo prueba sintáctica.

    INVARIANTE MONTO_POSITIVO
    OBJETO: REGISTRO
    EXPRESION: MONTO
    DOMINIO: REGISTRO
    SATISFACCION: VALIDADA
    VERIFICACION: PRUEBA
    EVIDENCIA: FACTURA

DOMINIO: REGISTRO usa un NAME no reservado. DOMINIO: CONTABLE colisionaría
con el literal CONTABLE de fractal_def en S0 (Acto 13 §6.4).


────────────────────────────────────────────────────────────────────────
§8. DOCUMENTO DE ASIENTO DECLARADO
────────────────────────────────────────────────────────────────────────

ejemplo_asiento.scfv conforme a asiento_declarado_def de Acto 13 §7.

    # DOCUMENTO SINTÉTICO — Acto 15 · SCFV_DSR · Giro 04
    # No representa operación económica real. Solo prueba sintáctica.

    ASIENTO_DECLARADO VENTA: DEMO_CUENTA DEMO_MONTO

No escribe en Diario ni Mayor. No invoca al Motor Contable.


────────────────────────────────────────────────────────────────────────
§9. DOCUMENTO INTEGRADO Y CIERRE DEL GAP DEL ACTO 14 §8.6
────────────────────────────────────────────────────────────────────────

ejemplo_integrado.scfv reúne simultáneamente las tres construcciones:

    # DOCUMENTO SINTÉTICO — Acto 15 · SCFV_DSR · Giro 04
    # No representa operación económica real. Solo prueba sintáctica.

    CONTRATO CONTROL_VENTA
    OBJETO: REGISTRO
    PRE: VENTA
    POST: VALIDADA
    INVARIANTE: MONTO_POSITIVO
    ELEMENTO: MONTO VENTA
    EVIDENCIA: FACTURA

    INVARIANTE MONTO_POSITIVO
    OBJETO: REGISTRO
    EXPRESION: MONTO
    DOMINIO: REGISTRO
    SATISFACCION: VALIDADA
    VERIFICACION: PRUEBA
    EVIDENCIA: FACTURA

    ASIENTO_DECLARADO VENTA: DEMO_CUENTA DEMO_MONTO

O-391: el CONTRATO referencia MONTO_POSITIVO mediante INVARIANTE:. Este
mecanismo ilustra la referencia nominal establecida en Acto 13 §5.3: la
gramática reconoce la referencia sin verificar que el INVARIANTE exista
como invariant_def. En este integrado, el INVARIANTE sí está declarado,
pero la relación entre ambos no es verificada por la gramática. La validez
de la referencia pertenece a una capa semántica posterior.

Este caso integrado cierra el requisito declarado en Acto 14 §8.6, no
ejecutado conjuntamente por la suite del Acto 14.


────────────────────────────────────────────────────────────────────────
§10. COMPATIBILIDAD CON LOS CUATRO HISTÓRICOS
────────────────────────────────────────────────────────────────────────

Los históricos permanecen sin modificación. La comparación de las cinco
claves históricas se realizará contra la salida del módulo S0. Las tres
claves extendidas pueden aparecer vacías sin que ello constituya regresión.


────────────────────────────────────────────────────────────────────────
§11. VERIFICACIÓN Y REGISTRO
────────────────────────────────────────────────────────────────────────

Verificación efectuada durante la materialización (§11-bis).

Registro:
Documento                  Resultado  Claves observadas
ejemplo_contrato.scfv      PASS       contratos{CONTROL_VENTA}
ejemplo_invariante.scfv    PASS       invariantes{MONTO_POSITIVO}
ejemplo_asiento.scfv       PASS       asientos_declarados{VENTA}
ejemplo_integrado.scfv     PASS       contratos + invariantes + asientos_declarados
ventas                     PASS       5 claves históricas + 3 vacías
compras                    PASS       5 claves históricas + 3 vacías
inventario                 PASS       5 claves históricas + 3 vacías
fiscal                     PASS       5 claves históricas + 3 vacías

Evidencia completa: transcript de la ejecución de la suite de verificación
durante la materialización del presente Acto.


────────────────────────────────────────────────────────────────────────
§12. CHECKLIST IA-2
────────────────────────────────────────────────────────────────────────

[X] los cuatro documentos nuevos existen;
[X] ejemplo_contrato.scfv parsea;
[X] ejemplo_invariante.scfv parsea;
[X] ejemplo_asiento.scfv parsea;
[X] ejemplo_integrado.scfv parsea;
[X] el integrado contiene simultáneamente las tres construcciones;
[X] el requisito conjunto del Acto 14 §8.6 queda cubierto;
[X] los cuatro históricos continúan parseando;
[X] las cinco claves históricas preservan su contenido;
[X] las tres claves extendidas permanecen separadas de las cinco históricas;
[X] los hashes históricos permanecen sin modificación;
[X] no se modifica grammar.lark;
[X] no se modifica parser.py;
[X] no se modifica S0;
[X] no existe escritura en Diario/Mayor;
[X] no existe decisión profesional producida por los ejemplos.


────────────────────────────────────────────────────────────────────────
§13. RÉGIMEN DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

§19.3-bis del Protocolo de Revisión de Actos, incorporado por
ACTAS/ACTA_ENMIENDA_PROTOCOLO_19_3_BIS.md.


────────────────────────────────────────────────────────────────────────
§14. LÍMITES
────────────────────────────────────────────────────────────────────────

No cierra I-3. No cierra D-12.3. No modifica S0. No modifica gramática.
No modifica parser. No reescribe históricos. No ejecuta operaciones contables.


────────────────────────────────────────────────────────────────────────
§15. DEUDAS
────────────────────────────────────────────────────────────────────────

D-12.3 · correspondencia arquitectura ↔ ejecución · abierta · Acto 16.
D-13.2 · semántica extendida de asiento_declarado_def · abierta.


────────────────────────────────────────────────────────────────────────
§16. CADENA DE ACTOS
────────────────────────────────────────────────────────────────────────

Acto 13 → Acto 14 → Acto 15 → Acto 16.


────────────────────────────────────────────────────────────────────────
§17. ESTADO
────────────────────────────────────────────────────────────────────────

VERSIÓN D — MATERIALIZADA.
O-390 y O-391 aplicadas.


────────────────────────────────────────────────────────────────────────
§18. FIRMAS
────────────────────────────────────────────────────────────────────────

IA-1: Versión D materializada.
IA-2: APTO SIN BLOQUEANTES.
OPERADOR: Materializado y firmado.

────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 35ce5516c73d9ae480ca4e34702f8491b2f5929e23379b7f22f0abcc292cb12d
Acta de referencia:      ACTA_MATERIALIZACION_15_SCFV_EXTENDIDOS_2026-09-22
Hash final:              49738e83b10e34ce68bbbcb1529876a43b8017e29efe9f474077020bf018abca

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 15 — ESCRITURA DE .scfv EXTENDIDOS — Versión D
════════════════════════════════════════════════════════════════════════

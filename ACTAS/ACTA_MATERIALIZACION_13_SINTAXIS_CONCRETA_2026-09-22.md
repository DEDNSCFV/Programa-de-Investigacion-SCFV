════════════════════════════════════════════════════════════════════════
ACTA DE MATERIALIZACIÓN — ACTO 13
Especificación de la sintaxis concreta ADL-SCFV y README del módulo
de gramática extendida

Programa: Investigación SCFV
Giro: 04 · Sesión: 4
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)
Estado efectivo: MATERIALIZADO Y FIRMADO
Régimen: §19.3-bis del Protocolo de Revisión de Actos

Hash previo al registro: 5bfda4c9f9726d3b84fe79eb34c62aaaa7c54aaca26fe79844fa537c56dd17da
Hash final registrado:   55c684bf94c5143bbfda92c1e260de63cd29dab89f11dcab3c41f3af69f031d1
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

La presente acta registra la materialización del Acto 13 en el archivo:

    GIRO_04/13_sintaxis_concreta_adl.md

El documento especifica la sintaxis concreta de las tres nuevas producciones
de ADL-SCFV (`contract_def`, `invariant_def`, `asiento_declarado_def`), la
extensión de `start`, y el contenido mínimo del README del módulo
`~/SCFV_DSR/dsl/` conforme a ADR-003.

Fue construido por IA-1, falsado bilateralmente por IA-2 en cinco rondas
(A→E), integrado hasta la Versión E y declarado APTO SIN BLOQUEANTES.

La materialización fue autorizada por el Operador.


────────────────────────────────────────────────────────────────────────
§2. VERIFICACIÓN DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Archivo materializado: GIRO_04/13_sintaxis_concreta_adl.md
Líneas: 667
Bytes:  27628

Hash previo al registro:
    5bfda4c9f9726d3b84fe79eb34c62aaaa7c54aaca26fe79844fa537c56dd17da

Hash declarado (campos "Hash final registrado" y "Hash final"):
    3fc8e7bd98ab49733bceeb673998337604f4f2721070c0cf3cf1cb0d0f0647ee

Hash en disco (post-sellado):
    e140099c9ea6d63661dd4a15f4d75374cc8a6b1c0a7bbd14536ab8d7cc853be0

Convención de verificación reproducible:

    1. Copiar el archivo.
    2. Reemplazar el valor de los campos "Hash final registrado" y
       "Hash final" por el literal 55c684bf94c5143bbfda92c1e260de63cd29dab89f11dcab3c41f3af69f031d1.
    3. Calcular SHA-256.
    4. El valor obtenido debe coincidir con el hash declarado.

Verificación ejecutada: APROBADA.


────────────────────────────────────────────────────────────────────────
§3. ALCANCE DE LA MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

La materialización del Acto 13:

- NO modifica S0.
- NO modifica grammar.lark de S0.
- NO modifica parser.py de S0.
- NO crea físicamente `~/SCFV_DSR/dsl/`.
- NO materializa código de gramática extendida.
- NO materializa parser extendido.
- NO verifica empíricamente la construcción LALR.
- NO cierra I-3.
- NO cierra D-12.2 ni D-12.3.
- NO cierra Giro 04.

Constituye, exclusivamente, la fijación documental de la especificación de
la sintaxis concreta ADL-SCFV y del README mínimo exigido por ADR-003.


────────────────────────────────────────────────────────────────────────
§4. TRAZABILIDAD DEL CICLO BILATERAL
────────────────────────────────────────────────────────────────────────

Ciclo IA-1 (constructor) ↔ IA-2 (falsador).

Iteraciones del acto:

- Versión A — borrador inicial. IA-2 emitió O-342, O-343, O-344, O-345 a
  O-349.
- Versión B — integración de O-342 a O-349. IA-2 emitió O-350, O-351, y
  no bloqueantes O-352 a O-354.
- Versión C — integración de O-350 a O-354. IA-2 emitió O-355 a O-360,
  más O-361 y O-363 tras falsación empírica con Lark 1.3.1.
- Versión D — integración de O-355 a O-364. IA-2 emitió O-365 a O-367.
- Versión E — integración de O-365 a O-367. IA-2 declaró APTO SIN
  BLOQUEANTES.

Ninguna objeción activa al momento de la materialización.

Deudas internas declaradas (§16): D-12.1 (cerrada por este Acto), D-12.2,
D-12.3, D-13.1, D-13.2.


────────────────────────────────────────────────────────────────────────
§5. ACTOS POSTERIORES DIFERIDOS
────────────────────────────────────────────────────────────────────────

La materialización del Acto 13 no implica:

- creación física de `~/SCFV_DSR/dsl/`;
- escritura de `grammar.lark` extendido;
- escritura de `parser.py` extendido;
- construcción LALR efectiva;
- verificación empírica de compatibilidad con los 4 `.scfv` históricos;
- parseo de los ejemplos de §5.6 y §6.4.

Estos actos quedan diferidos conforme a §13 del Acto 13 y al Protocolo
vigente. Corresponden al Acto 14.


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD DEL ACTA
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 9411853816a056d132226b089f9cab316df08864f1ee98f3e19fe85f48a98234
Hash final:              55c684bf94c5143bbfda92c1e260de63cd29dab89f11dcab3c41f3af69f031d1

════════════════════════════════════════════════════════════════════════
FIN DEL ACTA — MATERIALIZACIÓN DEL ACTO 13
════════════════════════════════════════════════════════════════════════

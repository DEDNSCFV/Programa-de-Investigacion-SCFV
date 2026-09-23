════════════════════════════════════════════════════════════════════════
ACTA DE EXTENSIÓN DE LA GRAMÁTICA ".scfv" PARA ADL-SCFV

Programa: Investigación SCFV
Giro: 04 · Sesión: 4 · Acto: 12
Documento: GIRO_04/12_extension_gramatica_adl.md
Versión: C
Estado efectivo: MATERIALIZADO Y FIRMADO
Fecha: 2026-09-22
Autoridad: Operador (DEDN, C.P.C. Nº 183594)

Ciclo bilateral: IA-1 (constructor) ↔ IA-2 (falsador)
Falsación cerrada: APTO SIN BLOQUEANTES.

Estatuto: este acto declara la especificación de la extensión de la
gramática ".scfv" para ADL-SCFV.
No modifica S0. No modifica grammar.lark de S0. No modifica parser.py de S0.
No materializa aún el código. No cierra I-3. No valida SCFV_DSR.
No cierra Giro 04.

Hash previo al registro: 5573324ec66f972b746a46bd63ce8f4a30a82d2a6fc83c2c35596577d938b1bc
Hash final registrado:   3e284483460a9d0cfd5506984e12b7027ce9f822417e0ec67d74cfae4018e49c
════════════════════════════════════════════════════════════════════════


────────────────────────────────────────────────────────────────────────
§1. OBJETO
────────────────────────────────────────────────────────────────────────

El presente acto tiene por objeto declarar la extensión de la gramática del
lenguaje ".scfv" para ADL-SCFV, mediante la incorporación de las formas
declarativas "contract_def", "invariant_def" y "asiento_declarado_def".

La extensión se materializará, si resulta aprobada tras la correspondiente
falsación y decisión del Operador, en el locus:

    ~/SCFV_DSR/dsl/

La extensión tiene carácter aditivo respecto de la gramática de S0. Su
finalidad es proporcionar una gramática local para ADL-SCFV capaz de
reconocer las nuevas declaraciones previstas por la arquitectura definida en
actos anteriores, sin modificar el árbol histórico de S0.

El acto declara la especificación que permitirá cerrar, previa falsación y
materialización, las deudas declaradas en §5.12 y §6.2 del Acto 10.


────────────────────────────────────────────────────────────────────────
§2. ANTECEDENTES DOCUMENTALES
────────────────────────────────────────────────────────────────────────

La construcción del presente borrador se ancla en los siguientes
antecedentes documentales:

1. Acto 10, "10_adl_scfv.md", cuyo hash registrado es
   "22996478933e948ef190ee88b1d22a9c000052e36f7a4db7fa6911eed32ac5b4",
   particularmente sus §§5.12 y 6.2.

2. Acto 08, §9.2, como antecedente de la separación entre el lenguaje
   declarado y su implementación.

3. Acto 11, "11_soporte_minimo.md", cuyo §5-bis establece el patrón de
   declaración de locus físico previsto sin materialización, reproducido
   por §4 del presente acto.

4. Parser de S0, "parser.py", cuyo hash registrado es:

   eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

5. Gramática de S0, "grammar.lark", cuyo hash registrado es:

   3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850

Estos documentos constituyen el marco documental de derivación del presente
acto.

El presente borrador no sustituye dichos documentos ni los modifica.


────────────────────────────────────────────────────────────────────────
§3. NECESIDAD
────────────────────────────────────────────────────────────────────────

El Acto 10 §5.12 declara como deuda la extensión efectiva de la gramática
".scfv" necesaria para representar las nuevas formas declarativas de
ADL-SCFV.

El Acto 10 §6.2 establece la forma conceptual de "start" como punto de
extensión de la gramática existente.

El presente acto transforma esa declaración conceptual en una propuesta de
estructura gramatical materializable, manteniendo separadas:

- la gramática histórica de S0;
- la gramática extendida de ADL-SCFV;
- las producciones existentes;
- las nuevas producciones;
- y la posterior implementación del parser.

La materialización efectiva queda subordinada a la falsación prevista en
este mismo acto.


────────────────────────────────────────────────────────────────────────
§4. LOCUS FÍSICO
────────────────────────────────────────────────────────────────────────

El locus físico previsto para la extensión es:

    ~/SCFV_DSR/dsl/grammar.lark
    ~/SCFV_DSR/dsl/parser.py
    ~/SCFV_DSR/dsl/__init__.py

El directorio:

    ~/SCFV_DSR/dsl/

se crea en este acto, únicamente si el acto supera las etapas de falsación,
integración y decisión previstas en §13.

Por tanto, en el estado actual de este documento, el locus constituye un
locus previsto y no materializado.

"grammar.lark" contendrá una copia local de la gramática de referencia y su
extensión.

"parser.py" contendrá, cuando corresponda, la adaptación del parser
necesaria para procesar la gramática extendida.

"__init__.py" se incorporará solamente si la estructura efectiva del módulo
lo requiere.

La extensión gramatical y su parser asociado se materializan exclusivamente
en `~/SCFV_DSR/dsl/`. El `parser.py` de S0 no se modifica ni se sustituye.

La existencia física de estos archivos no debe inferirse de la existencia
del presente borrador.


────────────────────────────────────────────────────────────────────────
§5. RÉGIMEN DE DERIVACIÓN
────────────────────────────────────────────────────────────────────────

La extensión se rige por el principio:

    «copia local, no importación entre gramáticas.»

La gramática extendida de ADL-SCFV deriva de la gramática existente mediante
copia local controlada y posterior extensión.

Este régimen se adopta porque el corpus técnico contiene varios árboles de
trabajo independientes, entre ellos:

    S0
    v6
    github
    entregable
    prueba_scfv

La comparación documental de las copias locales de "grammar.lark" queda
registrada de la siguiente manera:

    Árbol             Hash "grammar.lark"
    SCFV_S0_V1.0.0    3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850
    scfv_v6           3e859e0275656ef60ed20d67bbe0e080f2f9c3694cbcc098f7e0ec8da50d6850
    scfv_github       2dcbf39777f1055c46a9d540b8d59a41831b9030fac617465473ad77227f4b31
    scfv_entregable   6a12a7520ca5a398409d7534eef309187ea2eaa3f91290d0f2dd3eec76a60d1c
    prueba_scfv       6a12a7520ca5a398409d7534eef309187ea2eaa3f91290d0f2dd3eec76a60d1c

"scfv_v6" mantiene la misma gramática que S0.

"scfv_github" divergió: eliminó "mandante_def", "rule", "condition", "action"
y "generate", y reescribió "contexto_def".

Esta divergencia refuerza el principio de derivación local y la necesidad de
preservar explícitamente la gramática de S0 como baseline de compatibilidad.

La coexistencia de estas copias no constituye autorización para establecer
una dependencia de importación entre ellas.

En consecuencia, la extensión propuesta para "SCFV_DSR" no utilizará
"%import" para incorporar producciones desde la gramática de S0 ni desde
cualquiera de los otros árboles.

La procedencia deberá quedar demostrable mediante la documentación de la
copia fuente y su hash.


────────────────────────────────────────────────────────────────────────
§6. CONTENIDO DE LA EXTENSIÓN
────────────────────────────────────────────────────────────────────────

La extensión propuesta conserva la estructura general de "start" existente
en S0 y agrega las nuevas categorías declarativas.

La forma existente de S0 contiene:

    (contexto_def | mandante_def | booleano_def | tetrada_def | fractal_def)*

La extensión propuesta conceptualmente incorpora:

    contract_def
    invariant_def
    asiento_declarado_def

de modo que "start" pase a admitir dichas categorías además de las
producciones existentes.

La formulación anterior expresa únicamente la estructura de extensión. No
constituye todavía la especificación sintáctica definitiva de las tres
producciones nuevas.

La sintaxis concreta será objeto de determinación y falsación posterior.

§6.1. "contract_def"

"contract_def" deberá reconocer una declaración de contrato dentro del
lenguaje ".scfv".

La producción deberá permitir representar formalmente los componentes del
concepto CONTRATO previsto por la arquitectura ADL-SCFV, manteniendo una
relación verificable entre la declaración y las condiciones que
posteriormente deberá ejecutar el runtime.

La producción deberá integrarse con las producciones existentes sin alterar
su forma ni su significado.

No se fija en este borrador:

- la secuencia definitiva de tokens;
- los delimitadores;
- los nombres concretos de campos;
- la cardinalidad definitiva;
- ni la forma completa de anidamiento.

Estas decisiones permanecen abiertas a falsación.

§6.2. "invariant_def"

"invariant_def" deberá reconocer una declaración de invariante dentro del
lenguaje ".scfv".

La producción deberá permitir representar formalmente los INVARIANTES
previstos por la arquitectura ADL-SCFV y mantener una correspondencia
verificable entre lo declarado y las condiciones que el runtime deba
comprobar.

La producción deberá ser aditiva y no deberá modificar las producciones
existentes.

Al igual que en "contract_def", la sintaxis concreta permanece
deliberadamente abierta.

§6.3. "asiento_declarado_def"

"asiento_declarado_def" deberá reconocer una declaración formal de
ASIENTO_DECLARADO dentro del lenguaje ".scfv".

La producción deberá distinguir la declaración del asiento de la ejecución
contable efectiva.

En particular, su incorporación a la gramática no constituye autorización
para convertir la declaración en escritura efectiva del Diario o Mayor.

La relación entre "asiento_declarado_def" y el Motor Contable deberá
permanecer conforme a la arquitectura establecida en los actos precedentes.

La sintaxis concreta queda igualmente pendiente de falsación.


────────────────────────────────────────────────────────────────────────
§7. REGLAS DE COMPATIBILIDAD
────────────────────────────────────────────────────────────────────────

La extensión deberá satisfacer, como condiciones mínimas de compatibilidad:

1. Todo ".scfv" válido bajo S0 deberá continuar siendo válido bajo
   "SCFV_DSR".

2. Ninguna producción existente deberá cambiar de forma.

3. Ningún token existente deberá cambiar de significado.

4. Los cuatro ".scfv" históricos —ventas, compras, inventario y fiscal—
   deberán continuar parseando sin modificación de su contenido.

La compatibilidad se entenderá como preservación del lenguaje histórico, no
como mera ausencia de errores durante una ejecución aislada.

Una extensión que permita las nuevas declaraciones pero invalide una
construcción histórica será considerada incompatible.

Baseline verificada: los cuatro ".scfv" históricos (ventas, compras,
inventario, fiscal) parsean sin error con el "parser.py" vigente sobre
"grammar.lark" de S0 (hash "3e859e02…"). La condición §7.4 se falsará tras
la extensión contra esta baseline.


────────────────────────────────────────────────────────────────────────
§8. VERIFICACIÓN LALR
────────────────────────────────────────────────────────────────────────

La gramática extendida deberá ser verificable mediante el parser LALR de
Lark.

El criterio mínimo de verificación será equivalente a:

    lark.Lark(grammar, parser="lalr")

La construcción deberá completarse sin excepción atribuible a la gramática.

Conforme al marco de análisis de Aho, §4.7, la verificación deberá
considerar particularmente:

- ausencia de conflictos shift/reduce;
- ausencia de conflictos reduce/reduce;
- existencia finita del autómata LALR;
- y posibilidad de documentar los estados relevantes del autómata.

La ausencia de excepción de construcción del parser constituye una condición
necesaria, pero no sustituye la verificación de compatibilidad semántica y
de preservación del histórico.


────────────────────────────────────────────────────────────────────────
§9. PRESERVACIÓN DEL HISTÓRICO
────────────────────────────────────────────────────────────────────────

Los archivos originales de S0:

    ~/SCFV_S0_V1.0.0/

no deberán ser modificados.

En particular, no se modificará:

    grammar.lark
    parser.py

dentro del árbol S0.

La extensión propuesta utilizará una copia nueva en:

    ~/SCFV_DSR/dsl/grammar.lark

El hash de la gramática S0 utilizada como fuente deberá quedar registrado
para permitir la trazabilidad entre la gramática histórica y la extensión.

El hash del "parser.py" fuente también se registra para completar la cadena
de derivación:

    eebba48b751c0caf412cf9f09f712b2d393cc902ed0e46c210ecd50788f41e83

La copia extendida en "SCFV_DSR" tendrá hash propio, distinto del fuente.

La copia no implica identidad permanente: una vez extendida, la gramática de
"SCFV_DSR" será un artefacto distinto, con su propio estado y hash.


────────────────────────────────────────────────────────────────────────
§10. RELACIÓN CON S0
────────────────────────────────────────────────────────────────────────

El presente acto no modifica S0.

A efectos operativos, la expresión «no tocar S0» significa específicamente:

    «No editar, sustituir, eliminar, renombrar ni alterar archivos dentro
    del árbol "~/SCFV_S0_V1.0.0/".»

La extensión se desarrolla fuera de ese árbol.

S0 permanece como referencia histórica y técnica de la gramática base.

"SCFV_DSR" constituye, en consecuencia, un árbol separado para experimentar
y posteriormente materializar la extensión de ADL-SCFV.

La extensión de la gramática no constituye una nueva versión de S0.


────────────────────────────────────────────────────────────────────────
§11. RELACIÓN CON BIBLIOGRAFÍA
────────────────────────────────────────────────────────────────────────

La fundamentación técnica de la extensión deberá contrastarse con:

- Aho et al., §4.7 (More Powerful LR Parsers), en particular §4.7.4
  (Constructing LALR Parsing Tables) y §4.7.5 (Efficient Construction of
  LALR Parsing Tables).

- Thain, §4.4.5, relativo a LALR Parsing.

Los materiales RAW disponibles para verificación documental son:

    ~/.aho_compilers_raw.txt
    ~/.thain_compilers_raw.txt

El presente borrador no atribuye a dichas fuentes una sintaxis concreta que
todavía no haya sido verificada contra ellas.

La consulta bibliográfica deberá servir para falsar o corregir la propuesta,
no para justificar retrospectivamente una sintaxis previamente fijada.


────────────────────────────────────────────────────────────────────────
§12. FALSACIÓN IA-2
────────────────────────────────────────────────────────────────────────

IA-2 deberá falsar, como mínimo, los siguientes puntos:

1. Firma de "start" extendido.
   Verificar que la incorporación de las tres nuevas categorías sea
   estructuralmente correcta.

2. Compatibilidad con S0.
   Verificar que el lenguaje previamente aceptado no resulte restringido.

3. Ausencia de conflictos LALR.
   Verificar "shift/reduce" y "reduce/reduce".

4. Preservación de la semántica de las producciones existentes.
   Determinar que la extensión no produzca una reinterpretación involuntaria
   de las formas históricas.

5. Parseo de los cuatro ".scfv" históricos.
   Ventas, compras, inventario y fiscal deberán continuar siendo aceptados
   sin modificación.

6. Locus físico correcto.
   Verificar que la extensión corresponda a "~/SCFV_DSR/dsl/".

7. Ausencia de modificación de S0.
   Verificar mediante comparación y hashes que el árbol S0 permanezca
   intacto.

8. Correspondencia con Acto 10 §5.12 y §6.2.
   Verificar que el acto realmente materialice lo declarado allí y no una
   arquitectura diferente.

9. Ausencia de invención de tokens.
   Ningún token nuevo deberá aparecer sin justificación formal dentro de la
   extensión.

10. Cadena PDF → RAW verificable.
    Las afirmaciones bibliográficas relevantes deberán poder remontarse desde
    la fuente PDF hasta los archivos RAW correspondientes.

La aprobación del checklist no corresponde a IA-2 en forma unilateral. IA-2
produce la falsación; la decisión de formalización corresponde al Operador.


────────────────────────────────────────────────────────────────────────
§13. CONDICIONES DE MATERIALIZACIÓN
────────────────────────────────────────────────────────────────────────

La materialización física de "~/SCFV_DSR/dsl/" queda sometida al régimen
establecido en §19.3-bis:

    «Falsación → integración → decisión → materialización.»

Por tanto, el presente documento no constituye por sí mismo una orden de
creación de archivos.

La materialización solamente podrá producirse después de:

1. recibir la falsación de IA-2;
2. integrar las correcciones que correspondan;
3. recibir la decisión del Operador;
4. y ejecutar la materialización autorizada.

Hasta entonces:

    ~/SCFV_DSR/dsl/

debe considerarse previsto, no materializado.


────────────────────────────────────────────────────────────────────────
§14. LÍMITES
────────────────────────────────────────────────────────────────────────

El presente acto no autoriza:

- modificar S0;
- modificar el parser de S0;
- modificar los cuatro ".scfv" históricos;
- cerrar I-3;
- declarar validado "SCFV_DSR";
- declarar validada la sintaxis definitiva de las nuevas producciones;
- convertir una declaración gramatical en ejecución contable;
- ni considerar resueltas las deudas expresamente registradas en §15.

La extensión gramatical propuesta tampoco constituye por sí misma una
demostración de correspondencia completa entre ADL-SCFV y el runtime Python.


────────────────────────────────────────────────────────────────────────
§15. DEUDAS
────────────────────────────────────────────────────────────────────────

Quedan registradas las siguientes deudas:

D-12.1 — Sintaxis concreta

Determinar y formalizar la sintaxis concreta de:

    contract_def
    invariant_def
    asiento_declarado_def

previa consulta y contraste con la bibliografía técnica pertinente.

D-12.2 — Implementación efectiva

Implementar "parser.py" extendido conforme a la gramática finalmente
aprobada.

D-12.3 — Correspondencia arquitectónica

Demostrar la correspondencia entre las nuevas producciones y:

    CONTRATO
    INVARIANTE
    ASIENTO_DECLARADO

definidos en el Acto 10 §5.0-bis.

Estas deudas no deberán confundirse con defectos de S0.


────────────────────────────────────────────────────────────────────────
§16. CADENA DE TRAZABILIDAD
────────────────────────────────────────────────────────────────────────

La cadena documental y material propuesta es:

    Acto 10
       ↓
    §5.12 / §6.2
       ↓
    Acto 12
       ↓
    ~/SCFV_DSR/dsl/
       ↓
    grammar.lark extendida
       ↓
    parser.py extendido
       ↓
    .scfv extendidos

La cadena expresa dependencia documental y técnica, no todavía evidencia de
ejecución.

Cada transición deberá poder verificarse mediante el artefacto
correspondiente una vez materializado.


────────────────────────────────────────────────────────────────────────
§17. ESTADO
────────────────────────────────────────────────────────────────────────

VERSIÓN C — MATERIALIZADA.

El documento se encuentra:

- materializado;
- pendiente de autorización de implementación de código (D-12.2);
- sin autorización para modificar S0.

La materialización de este documento no constituye materialización del
código que implementará la gramática extendida ni del parser extendido.

La implementación material requiere acto separado conforme a §13 y al
Protocolo vigente.


────────────────────────────────────────────────────────────────────────
§18. FIRMAS
────────────────────────────────────────────────────────────────────────

IA-1 — Constructor
Estado: Versión C materializada.

IA-2 — Falsador
Estado: APTO SIN BLOQUEANTES.

OPERADOR
Estado: Materializado y firmado.
Firma: [Operador]


────────────────────────────────────────────────────────────────────────
REGISTRO DE INTEGRIDAD
────────────────────────────────────────────────────────────────────────

Hash previo al registro: 5573324ec66f972b746a46bd63ce8f4a30a82d2a6fc83c2c35596577d938b1bc
Acta de referencia:      ACTA_MATERIALIZACION_12_EXTENSION_GRAMATICA_2026-09-22
Hash final:              3e284483460a9d0cfd5506984e12b7027ce9f822417e0ec67d74cfae4018e49c

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 12 — EXTENSIÓN DE LA GRAMÁTICA ".scfv" PARA ADL-SCFV — Versión C
════════════════════════════════════════════════════════════════════════

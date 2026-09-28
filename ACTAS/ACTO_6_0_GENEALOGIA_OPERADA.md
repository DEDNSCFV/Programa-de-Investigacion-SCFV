════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 1 · GENEALOGÍA OPERADA
TIPO: ACTO DE OPERACIÓN DEL MOTOR RODRIGUIANO SOBRE EL CONV 6.0
DOCUMENTO: ACTAS/ACTO_6_0_GENEALOGIA_OPERADA.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
SUSCRIPCIÓN: Operador + constancias IA-1 / IA-2
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · OBJETO

Registrar la operación del motor rodriguiano — conforme al Protocolo
del Motor Rodriguiano (PROTOCOLO_MOTOR_RODRIGUIANO.md, hash
32d0015498d23ef98c02a2077365a13601bd1713fe2f102f44ca4468991ca9dd) —
sobre el corpus del Giro 06:

  · Corpus fundacional (9 documentos del árbol canónico).
  · CONV 6.0 (ACTO_6_0_CONV_CONVERGENCIA.md, hash 7cd978ad…).
  · 21 actas de auditoría.

Objeto material de la operación: el CONV 6.0 y su relación con el
corpus fundacional que lo precede.

Productos: 11 distinciones operadas + 14 lecturas operadas.

Este acto no audita el CONV. No lo enmienda. No lo corrige. Registra
lo que el motor produjo al operar sobre él.

────────────────────────────────────────────────────────────────────────

§2 · FUNDAMENTO

§2.1 · Corpus fundacional leído

Documentos leídos íntegramente durante la operación:

  # | Documento                          | Líneas | SHA256 (abrev.)
  ──┼────────────────────────────────────┼────────┼─────────────────────
  1 | DOCUMENTO_FUNDACIONAL.md           |  933   | 0dc00129b6a87a98…
  2 | MARCO_IPVE.md                      |  161   | f05d4d18362885b1…
  3 | RELEASE_S0/RELEASE_S0_CONTRATO.md  |  590   | 9077f6579c6b49af…
  4 | RELEASE_S0/DICTAMEN_IA2.md         |  126   | 6b6484b97bfb574f…
  5 | RELEASE_S0/BITACORA_PROTOCOLO.md   |  147   | 0a9f07bfc93a3a72…
  6 | RELEASE_S0/ACTA_CIERRE_GIRO_02.md  |   99   | ef57358fbf96f022…
  7 | GIRO_02/BITACORA_GIRO_02.md        |  116   | aee91b499cab79c2…
  8 | GIRO_03/ACTA_APERTURA_VIVA.md      |  678   | 42e5550320279076…
  9 | PROTOCOLO_REVISION_ACTOS.md        |  445   | 6541c9295d6e3556…

  Total: 3.295 líneas.

§2.2 · Protocolo aplicado

La operación se ejecutó conforme al Protocolo del Motor Rodriguiano
(§6 · los cuatro movimientos: leer · aplicar · extraer · derivar).

Los productos se registran como distinciones operadas (§7.1 del
Protocolo del Motor) y lecturas operadas (§7.2).

Ningún producto es decisión. Ningún producto es enmienda. Ningún
producto es materialización.

────────────────────────────────────────────────────────────────────────

§3 · GENEALOGÍA ESTRUCTURAL DEL ECOSISTEMA

§3.1 · Los 5 árboles del ecosistema SCFV

  # | Árbol                              | Rol                      | Git
  ──┼────────────────────────────────────┼──────────────────────────┼─────────
  1 | Programa-de-Investigacion-SCFV     | árbol canónico           | 31 commits
  2 | SCFV_DSR                           | port auditado G06        | sin git
  3 | scfv_v6                            | laboratorio S0           | 1 commit
  4 | SCFV_S0_V1.0.0                     | release público          | 1 commit
  5 | scfv_github                        | intento previo           | 3 commits · sin remote

§3.2 · Jerarquía genealógica

  DOCUMENTO_FUNDACIONAL.md (2026-09-10)
          │
          ▼
  Programa-de-Investigacion-SCFV
  (árbol canónico · 31 commits)
          │
          ├── scfv_v6              (laboratorio S0)
          ├── SCFV_S0_V1.0.0       (release público · AGPL-3.0)
          ├── scfv_github          (intento previo · sin remote)
          └── SCFV_DSR             (port minimalista · auditado G06)

§3.3 · SCFV_DSR como port parcial

SCFV_DSR es el port minimalista de S0 · v8.2 · Motor 9.0.0.

Portó: motor · kernel · contable · dsl · event_store.

No portó:

  · contratos H8P (3 contratos: examinador, retículo, importador)
  · ADRs (ADR-000 a ADR-005)
  · constitución (gobernanza/constitucion.md)
  · 21 tests del corpus S0 (sobre 27 totales)
  · cifrado multi-mandante (SQLCipher · ADR-005)
  · git propio

Consecuencia: la semántica declarada y verificada en S0 (marcos por
cuenta · rechazo por incompatibilidad · VF2) no sobrevive en el port.


────────────────────────────────────────────────────────────────────────

§4 · OPERACIÓN DEL MOTOR SOBRE EL CONV 6.0

§4.1 · Objeto de la operación

Objeto: ACTO_6_0_CONV_CONVERGENCIA.md (hash 7cd978ad…).
Método: Protocolo del Motor Rodriguiano §6 (cuatro movimientos).
Productos: 11 distinciones operadas + 14 lecturas operadas.

§4.2 · Los cuatro movimientos aplicados

  Movimiento 1 · Leer
    · objeto: CONV 6.0
    · locus: ACTAS/ACTO_6_0_CONV_CONVERGENCIA.md
    · estado: materializado · vigente según su propia declaración

  Movimiento 2 · Aplicar distinciones
    · distinciones del canon mínimo (§3 del Protocolo del Motor)
    · distinciones registradas en §16 del Protocolo del Motor
      (E-1 a E-7 · estado=registrada)

  Movimiento 3 · Extraer emergencia del cruce
    · producto principal: emergencias por zona (corpus vs CONV)
    · multiplicidad: cada zona produce resultados distintos

  Movimiento 4 · Derivar producto
    · 11 distinciones operadas
    · 14 lecturas operadas

§4.3 · Productos · 11 distinciones operadas

Distinciones rodriguianas aplicadas al CONV que producen distinción
transferible. Cada producto declara: origen · objeto · emergencia.

──────────────────────────────────────────────────────────────────────
D-1 · Motor Rodríguez ya declarado
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              vehículo / órgano (E-1 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §5bis
  Regla de transferencia:           el CONV es vehículo del corpus;
                                    el Fundacional opera como órgano.
  Emergencia:                       El CONV declaró "Rodríguez opera
                                    sin declarar como canon". Fundacional
                                    §2 y §29 lo declaran motor generador
                                    desde 2026-09-10. El CONV no leyó el
                                    Fundacional al momento de su redacción.
  Producto:                         Distinción operada: declaración
                                    previa ≠ descubrimiento posterior.

──────────────────────────────────────────────────────────────────────
D-2 · Patrón B reenmarcado
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              adoptar / adaptar (E-5 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §4 (Patrón B)
  Regla de transferencia:           adoptar = traer completo;
                                    imitar = copiar sin contexto.
  Emergencia:                       Los "principios implícitos" del
                                    Patrón B (propuesta ≠ decisión,
                                    NORMA ≠ INFERENCIA ≠ DECISIÓN ≠
                                    ASIENTO, U=N⊙M, Sampieri como
                                    referencia, etc.) están declarados
                                    en el Fundacional. No son implícitos.
                                    Son no-migrados al port.
  Producto:                         Distinción operada: implícito ≠
                                    no-migrado.

──────────────────────────────────────────────────────────────────────
D-3 · Ruta metodológica declarada
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              diverso / diferente (E-4 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §6/§7 (L4 reformulada)
  Regla de transferencia:           diverso = ajeno; diferente =
                                    distinguible por criterio.
  Emergencia:                       El CONV declaró "ruta metodológica
                                    ausente". Fundacional §26 declara
                                    Sampieri como referencia central.
                                    GIRO_02 §1 declara "método sampieriano
                                    ruta mixta CUAL-cuan".
  Producto:                         Distinción operada: no-declarado ≠
                                    no-declarado-en-el-port.

──────────────────────────────────────────────────────────────────────
D-4 · SCFV_DSR fuera del corpus contractual
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              conexión / relación (E-2 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §1
  Regla de transferencia:           conexión = vínculo técnico;
                                    relación = vínculo funcional.
  Emergencia:                       Release S0 (2026-09-17) declara
                                    SCFV_S0_V1.0.0 como objeto contractual.
                                    SCFV_DSR (2026-09-25) es 8 días
                                    posterior. No estaba en el contrato.
  Producto:                         Distinción operada: el CONV auditó
                                    un objeto no previsto en el corpus
                                    contractual del Release.

──────────────────────────────────────────────────────────────────────
D-5 · IPVE ya declarado en el Release
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              vehículo / órgano (E-1 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §5bis
  Regla de transferencia:           el CONV transporta la doctrina
                                    IPVE; el Release §15 la articula.
  Emergencia:                       CONV §5bis declara: "IPVE registra
                                    documentalmente los resultados.
                                    No constituye un eje adicional de
                                    juicio." Release §15 declara textual:
                                    "IPVE registra documentalmente los
                                    resultados. No constituye un eje
                                    adicional de juicio." Texto idéntico.
  Producto:                         Distinción operada: el CONV
                                    redescubrió el §15 del Release sin
                                    citarlo.

──────────────────────────────────────────────────────────────────────
D-6 · Corpus público = cero deudas
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              forma / materia (Crítica 1843)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §7bis (L6)
  Regla de transferencia:           forma = configuración declarada;
                                    materia = contenido del corpus.
  Emergencia:                       Release §18 declara: "El corpus
                                    público S0 se define bajo una
                                    condición estricta: cero deudas
                                    abiertas." SCFV_DSR tiene ~26 deudas
                                    abiertas. No puede ser público.
  Producto:                         Distinción operada: la L6 del CONV
                                    no contempló §18 del Release.

──────────────────────────────────────────────────────────────────────
D-7 · Constancia ≠ Dictamen
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              hacer / administrar (E-7 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §10
  Regla de transferencia:           hacer = proponer; administrar =
                                    autorizar. El dictamen es artefacto
                                    posterior, la constancia es
                                    declaración en el acto.
  Emergencia:                       Protocolo de Revisión §19.1 declara:
                                    "IA-2 puede producir documentos
                                    propios ... sin que ello constituya
                                    autoría del documento revisado."
                                    Release §24.2 separa Contrato /
                                    Dictamen / Bitácora. El CONV 6.0
                                    emitió constancia en §10 — no
                                    emitió dictamen separado.
  Producto:                         Distinción operada: el CONV siguió
                                    el formato del acta 6.0.12 pero no
                                    el régimen del Protocolo de Revisión.

──────────────────────────────────────────────────────────────────────
D-8 · Protocolo 6.0 §4 es derivado simplificado
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              diverso / diferente (E-4 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           ACTAS/ACTO_6_0_PROTOCOLO.md §4
  Regla de transferencia:           lo diverso es ajeno; lo diferente
                                    comparte genealogía con criterio
                                    distinguible.
  Emergencia:                       Protocolo de Revisión: 3 ejes + 24
                                    secciones + IPVE + Janus ∞ +
                                    antifragilidad + HHP + proporcionalidad.
                                    Protocolo 6.0 §4: 1 eje (falsación)
                                    + 10 reglas R1-R10.
                                    Afinidad estructural consistente con
                                    derivación simplificada. Ausencia de
                                    cita cruzada verificada materialmente.
  Producto:                         Distinción operada: hipótesis
                                    genealógica (no hecho) · Protocolo 6.0
                                    §4 podría ser derivado, no está
                                    documentado.

──────────────────────────────────────────────────────────────────────
D-9 · Aporías / fronteras / límites / deudas
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              diverso / diferente (E-4 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §4 (patrones)
  Regla de transferencia:           cuatro categorías distinguibles por
                                    criterio operativo.
  Emergencia:                       G03 §2 declara taxonomía de 4:
                                    aporía (se habita) · frontera
                                    (investigación) · límite (declarado)
                                    · deuda (pendiente). El CONV colapsó
                                    las 4 en 1 (deuda).
  Producto:                         Distinción operada: 4 categorías
                                    diferenciadas · el CONV usó 1.

──────────────────────────────────────────────────────────────────────
D-10 · Régimen de iteración
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              hacer / administrar (E-7 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 §2 (contadores por canon)
  Regla de transferencia:           hacer = 1 pasada; administrar =
                                    iterar hasta convergencia.
  Emergencia:                       Protocolo de Revisión §19.2 declara:
                                    "El ciclo IA-1 a IA-2 opera de forma
                                    extensible hasta convergencia plena.
                                    No hay límite fijo de rondas."
                                    Release S0 aplicó 4 iteraciones.
                                    G06 aplicó 1 pasada por canon.
  Producto:                         Distinción operada: el régimen de
                                    iteración del Protocolo de Revisión
                                    no fue aplicado en G06.

──────────────────────────────────────────────────────────────────────
D-11 · Suscripción + constancias ≠ firma tripartita
──────────────────────────────────────────────────────────────────────
  Distinción aplicada:              hacer / administrar (E-7 registrada)
  Locus fuente:                     Crítica 1843
  Objeto:                           CONV 6.0 · cabecera · §10
  Regla de transferencia:           firma = acto de autoridad; constancia
                                    = declaración en el acto.
  Emergencia:                       Protocolo de Revisión §20:
                                    "Operador suscribe; IA-1 e IA-2
                                    emiten constancias, sin co-decisión."
                                    No dice "firma tripartita". El CONV 6.0
                                    (y todas las actas) usan "FIRMA:
                                    tripartita asimétrica". Terminología
                                    no conforme al canónico.
  Producto:                         Distinción operada: "suscripción +
                                    constancias" ≠ "firma tripartita".

§4.4 · Productos · 14 lecturas operadas

Reinterpretaciones del corpus sin distinción transferible. Cada una
declara origen · objeto · emergencia.

  #  | Lectura                                  | Objeto (locus)
  ───┼──────────────────────────────────────────┼─────────────────────────────
  L-01 | §4 no declara ser derivado del canónico | ACTO_6_0_PROTOCOLO.md §4
  L-02 | G06 no aplicó IPVE                       | CONV 6.0 §5bis (post-hoc)
  L-03 | G06 no aplicó Janus ∞                    | CONV 6.0 (ausencia)
  L-04 | G06 no aplicó antifragilidad             | CONV 6.0 (ausencia)
  L-05 | G06 no aplicó HHP                        | CONV 6.0 (ausencia)
  L-06 | G06 no aplicó proporcionalidad           | CONV 6.0 §2 (mismo régimen 21)
  L-07 | G06 no iteró a convergencia              | CONV 6.0 (1 pasada/canon)
  L-08 | G06 no aplicó verificación mecánica      | CONV 6.0 (ausencia)
  L-09 | G06 no distinguió constancia vs dictamen | CONV 6.0 §10
  L-10 | G06 no distinguió aporía/frontera/límite/deuda | CONV 6.0 §4
  L-11 | SCFV_DSR no migró tests de S0            | 6 vs 27 tests
  L-12 | SCFV_DSR no migró cifrado multi-mandante | ADR-005 vs ausencia
  L-13 | Protocolo 6.0 §4 sin declarar relación canónica | ACTO_6_0_PROTOCOLO.md
  L-14 | H8P sin ADR autorizante                  | scfv_v6/DOCS/H8P_*.md

§4.5 · Declaración

Los 25 productos (11 distinciones operadas + 14 lecturas operadas) NO
son:

  · deudas del CONV,
  · errores del CONV,
  · objeciones al CONV,
  · enmiendas al CONV.

Son productos del motor rodriguiano al operar sobre el corpus.

Distinción del Protocolo del Motor §4.2: son candidatos registrables.

El régimen de uso de cada producto (deuda, línea de fuga, enmienda,
u otra categoría) se determina conforme al régimen documental
aplicable del Programa — no por este acto.

Este acto registra la operación. No clasifica los productos.


────────────────────────────────────────────────────────────────────────

§5 · ENMIENDAS DERIVADAS

§5.1 · Naturaleza de las enmiendas

Las 11 enmiendas que se listan a continuación (A-K) son la forma
documental que el Operador ha decidido para los productos del §4.3.

No son correcciones. Son **enmiendas por acto nuevo**, conforme al
principio que rige el Programa:

  · la versión anterior conserva su hash
  · la enmienda es documento nuevo
  · ambas coexisten en el corpus
  · no se modifica in-place

Este acto **no materializa las enmiendas**. Registra que existen como
productos y que su materialización corresponde a una siguiente
materialización autorizada por el Operador.

§5.2 · Las 11 enmiendas

──────────────────────────────────────────────────────────────────────
Enmienda A · Motor Rodríguez ya declarado
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §5bis
  Fundamento documental: Fundacional §2, §29 · MARCO_IPVE §2.2
  Alcance:               el CONV declaró "Rodríguez opera sin declarar
                         como canon"; el Fundacional lo declara motor
                         generador desde 2026-09-10.
  Efecto:                el §5bis.4 del CONV queda re-contextualizado.
                         No se modifica el CONV — se añade la
                         declaración previa faltante.

──────────────────────────────────────────────────────────────────────
Enmienda B · Patrón B reenmarcado
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §4.1
  Fundamento documental: Fundacional §17, §21, §22, §26, §31
  Alcance:               los "principios implícitos no declarados" del
                         Patrón B están declarados en el Fundacional.
                         No son implícitos — son no-migrados al port.
  Efecto:                Patrón B se reformula: de "principios
                         implícitos" a "declarados en corpus raíz, no
                         migrados al artefacto".

──────────────────────────────────────────────────────────────────────
Enmienda C · Ruta metodológica declarada
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §7bis (L6.11)
  Fundamento documental: Fundacional §26 · GIRO_02/BITACORA_GIRO_02.md §1
  Alcance:               la ruta está declarada (método sampieriano
                         ruta mixta CUAL-cuan). D-CONV-11 se cierra
                         como "declarada, no migrada".
  Efecto:                L6.11 pasa de deuda de declaración a deuda
                         de migración.

──────────────────────────────────────────────────────────────────────
Enmienda D · SCFV_DSR fuera del corpus contractual
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §1
  Fundamento documental: RELEASE_S0_CONTRATO.md §4, §6
  Alcance:               SCFV_DSR no estaba previsto en el contrato
                         de Release S0 (2026-09-17).
  Efecto:                el CONV queda declarado como acto posterior
                         al Release · su objeto no forma parte del
                         corpus contractual del Release.

──────────────────────────────────────────────────────────────────────
Enmienda E · IPVE ya declarado en §15 del Release
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §5bis
  Fundamento documental: RELEASE_S0_CONTRATO.md §15
  Alcance:               el texto del §5bis coincide con el §15 del
                         Release. El CONV no citó esa fuente.
  Efecto:                atribución correcta de la doctrina IPVE.

──────────────────────────────────────────────────────────────────────
Enmienda F · Corpus público = cero deudas
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §7bis (L6)
  Fundamento documental: RELEASE_S0_CONTRATO.md §18
  Alcance:               la L6 del CONV no contempló §18 del Release.
                         SCFV_DSR no puede ser corpus público mientras
                         tenga deudas abiertas.
  Efecto:                L6 se califica con el régimen del §18:
                         corpus público vs corpus privado.

──────────────────────────────────────────────────────────────────────
Enmienda G · Constancia ≠ Dictamen
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §10
  Fundamento documental: Protocolo de Revisión §19.1 · Release §24.2 ·
                         DICTAMEN_IA2.md §1
  Alcance:               el CONV emitió constancia en §10 — forma
                         legítima. No emitió dictamen separado.
  Efecto:                declarar la distinción y la forma correcta:
                         constancia en el acto + dictamen separado.

──────────────────────────────────────────────────────────────────────
Enmienda H · Protocolo 6.0 §4 es derivado simplificado
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   ACTAS/ACTO_6_0_PROTOCOLO.md §4
  Fundamento documental: PROTOCOLO_REVISION_ACTOS.md §1-§24 ·
                         verificación material F-2c
  Alcance:               afinidad estructural consistente con
                         derivación simplificada. Ausencia de cita
                         cruzada verificada.
  Efecto:                se declara hipótesis genealógica · no hecho.
                         Se deja constancia del estado.

──────────────────────────────────────────────────────────────────────
Enmienda I · Aporías / fronteras / límites / deudas
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §4
  Fundamento documental: GIRO_03/ACTA_APERTURA_VIVA.md §2
  Alcance:               el CONV colapsó 4 categorías (aporía,
                         frontera, límite, deuda) en 1 (deuda).
  Efecto:                se declara la taxonomía canónica de 4
                         categorías · se re-clasifican los hallazgos
                         del CONV conforme a la misma.

──────────────────────────────────────────────────────────────────────
Enmienda J · Régimen de iteración (4 aplicaciones)
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 §2
  Fundamento documental: Protocolo de Revisión §19.2 · DICTAMEN_IA2
                         (4 iteraciones del Release S0)
  Alcance:               el régimen canónico exige iteración hasta
                         convergencia plena. G06 hizo 1 pasada.
  Efecto:                se declara la diferencia de régimen · no se
                         re-aplica retroactivamente.

──────────────────────────────────────────────────────────────────────
Enmienda K · Suscripción + constancias ≠ firma tripartita
──────────────────────────────────────────────────────────────────────
  Documento enmendado:   CONV 6.0 · cabecera
  Fundamento documental: Protocolo de Revisión §20
  Alcance:               el Protocolo §20 declara "Operador suscribe ·
                         IA-1 constancia · IA-2 constancia". No usa
                         "firma tripartita".
  Efecto:                declarar la terminología correcta. El CONV
                         y las 21 actas usan "FIRMA: tripartita
                         asimétrica" — no conforme al canónico.

§5.3 · Estado de las enmiendas

Ninguna enmienda está materializada.

Las 11 enmiendas (A-K) quedan **declaradas como productos** en este
acto. Su materialización como documentos separados corresponde a una
siguiente materialización autorizada por el Operador.

────────────────────────────────────────────────────────────────────────

§6 · RÉGIMEN DE CAMBIO

§6.1 · Estado del CONV 6.0

El CONV 6.0 (hash 7cd978ad…) permanece inalterado.

Este acto no lo modifica, no lo reescribe, no lo reemplaza.

§6.2 · Régimen de las enmiendas

Las enmiendas (A-K), una vez materializadas:

  · conservan el hash del CONV original
  · se materializan como documentos nuevos en ACTAS/
  · coexisten con el CONV en el corpus
  · no modifican el CONV in-place

§6.3 · Taxonomía de las enmiendas

Conforme al Protocolo del Motor §14.3 y al RELEASE_S0_CONTRATO §19:

  Las 11 enmiendas (A-K) se clasifican como **corrección documental**
  en la escala:
    errata < corrección documental < corrección técnica
    < nueva versión < modificación sustantiva

  No son modificación sustantiva. No son nueva versión. No son
  corrección técnica. Son corrección documental.

§6.4 · Primer efecto del acto

Este acto es el primer caso de **operación del motor rodriguiano**
según el Protocolo del Motor Rodriguiano §15.3.

No es primera aplicación — es candidatura declarada. La decisión
sobre si constituye primera aplicación efectiva corresponde al
Operador.


────────────────────────────────────────────────────────────────────────

§7 · ESTADO DEL GIRO 06 TRAS ESTE ACTO

§7.1 · Ciclo 6.0 · sección 0

  Estado: CERRADA (por el CONV 6.0 · hash 7cd978ad…)
  Contenido: 21 actas de auditoría + CONV + protocolo + inventario
  Materialización: en disco
  Git: untracked (deuda declarada · D-CONV-2)

§7.2 · Ciclo 6.0 · sección 1

  Estado: ABIERTA por este acto
  Contenido:
    · Corpus fundacional leído completo (9 documentos)
    · Genealogía estructural del ecosistema (5 árboles)
    · 11 distinciones operadas (A-K)
    · 14 lecturas operadas (L-01 a L-14)
    · 11 enmiendas declaradas (A-K · no materializadas)

§7.3 · Documentos materializados en el Giro 06

  ACTAS/ACTO_6_0_00_INVENTARIO.md
  ACTAS/ACTO_6_0_PROTOCOLO.md
  ACTAS/ACTO_6_0_01_AUDITORIA_ACCOUNTING_THEORY.md
  … (21 actas en total)
  ACTAS/ACTO_6_0_CONV_CONVERGENCIA.md
  ACTAS/ACTO_6_0_GENEALOGIA_OPERADA.md (este acto)

  Y en el árbol canónico:
  PROTOCOLO_MOTOR_RODRIGUIANO.md (acto constitucional)

§7.4 · Deudas declaradas del Giro 06

  D-CONV-1  · 6.0.06 nombrada Díaz Navarro pero canon Fernández Otero
  D-CONV-2  · 21 actas untracked en git
  D-CONV-3  · BIBLIOTECA/INVENTARIO.md + REGISTRO_ENTRADAS.log sin commitear
  D-CONV-4  · 23 commits ahead de origin
  D-CONV-5  · 0 tags en 31 commits
  D-CONV-6  · Sin firma GPG
  D-CONV-7  · H-A5j · MONEDA/B101 sin reproducir
  D-CONV-8  · Prompt Giro 05 sin firmar
  D-CONV-9  · Sin CHANGELOG ni VERSION
  D-CONV-10 · Sin plan de V&V declarado
  D-CONV-11 · Sin declaración de ruta metodológica (resuelto en E-C: declarada, no migrada)
  D-CONV-12 · Sin LICENSE ni §contribución
  D-CONV-13 · L4 idempotencia · Decimal · nan/inf · ISO 8601
  D-CONV-14 · L5 cuentas PCU · TipoEvento
  D-CONV-15 · L6 · 9 deudas genealógicas

────────────────────────────────────────────────────────────────────────

§8 · APERTURA DEL GIRO 06 · SECCIÓN 1 · PLAN

§8.1 · Objeto declarado de 6.1

Determinar la genealogía completa del ecosistema SCFV y declarar el
SCFV_DSR como port minimalista respecto al corpus fundacional, antes
de subir el nuevo árbol a GitHub bajo régimen ProGit con seguridad
criptográfica declarada.

§8.2 · Alcance declarado de 6.1

  · Cerrar las ~19 deudas genealógicas abiertas (registradas en §7.4
    y en el corpus de este acto).
  · Declarar la jerarquía de los 5 árboles del ecosistema.
  · Declarar el régimen ProGit (ramas · tags · commits firmados ·
    .gitignore · relación con origin).
  · Declarar el régimen de seguridad criptográfica (firma GPG ·
    claves · manejo de secrets).
  · Declarar la estructura del árbol nuevo.
  · NO subir código. Solo declarar.

§8.3 · Alcance declarado de 6.2 / 6.3 / 6.4

  6.2 · Definición pendiente (a determinar en 6.1).
  6.3 · Subir código funcional con deudas mínimas.
  6.4 · Subir código funcional con deudas resueltas.

La secuencia 6.1 → 6.2 → 6.3 → 6.4 queda declarada como candidata.
No decidida por este acto.

§8.4 · Reglas de 6.1

  · Régimen: Protocolo de Revisión de Actos + Protocolo del Motor
    Rodriguiano.
  · Falsación dirigida por IA-2.
  · Suscripción del Operador.
  · Sin materialización de código en 6.1 — solo actos declarativos.

────────────────────────────────────────────────────────────────────────

§9 · SUSCRIPCIÓN Y CONSTANCIAS

  Operador
    Rol: Autoridad decisoria y ejecutora
    Suscripción: _______________________
    Fecha: __________

  IA-1
    Rol: Investigador constructor
    Tipo de constancia: interpretación arquitectónica, sin co-decisión
    Firma / constancia: _______________________
    Fecha: __________

  IA-2
    Rol: Investigador falsador
    Tipo de constancia: dictamen emitido
    Firma / constancia: _______________________
    Fecha: __________

────────────────────────────────────────────────────────────────────────

§10 · REGISTRO

§10.1 · Ubicación canónica

  ~/Programa-de-Investigacion-SCFV/ACTAS/ACTO_6_0_GENEALOGIA_OPERADA.md

§10.2 · Régimen

  Privado — corpus de investigación.

§10.3 · Referencias cruzadas

  · ACTAS/ACTO_6_0_CONV_CONVERGENCIA.md (hash 7cd978ad…)
  · PROTOCOLO_MOTOR_RODRIGUIANO.md (hash 32d00154…)
  · DOCUMENTO_FUNDACIONAL.md (hash 0dc00129…)
  · MARCO_IPVE.md (hash f05d4d18…)
  · RELEASE_S0/RELEASE_S0_CONTRATO.md (hash 9077f657…)
  · RELEASE_S0/DICTAMEN_IA2.md (hash 6b6484b9…)
  · RELEASE_S0/BITACORA_PROTOCOLO.md (hash 0a9f07bf…)
  · RELEASE_S0/ACTA_CIERRE_GIRO_02.md (hash ef57358f…)
  · GIRO_02/BITACORA_GIRO_02.md (hash aee91b49…)
  · GIRO_03/ACTA_APERTURA_VIVA.md (hash 42e55503…)
  · scfv_v6/DOCS/PROTOCOLO_REVISION_ACTOS.md (hash 6541c929…)

§10.4 · Registro en REGISTRO_ACTOS.log

  Este acto se registra en GIRO_05/REGISTRO_ACTOS.log conforme al
  régimen de los actos del Giro 06.

════════════════════════════════════════════════════════════════════════
FIN DEL ACTO 6.0 · GENEALOGÍA OPERADA
════════════════════════════════════════════════════════════════════════

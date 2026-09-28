════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON PROGIT 2014
DOCUMENTO: ACTAS/ACTO_6_0_15_AUDITORIA_PROGIT.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autores: Scott Chacon · Ben Straub
Obra: Pro Git (2ª edición, 2014)
Raw: ~/.progit_2014_raw.txt · 18.554 líneas · 904.940 bytes
SHA256 raw: 7fce1e80fd19e2adf1fc75c8c6a0f4d270e17bfca026b4a6d83d3b1cca313663
Naturaleza: control de versiones distribuido · git

Loci invocados:
  L337-388   · sobre el control de versiones
  L446-506   · fundamentos (integridad · content-addressed · snapshots)
  L668-694   · configuración · identidad inmutable
  L2123      · tags anotados
  L2162      · tags ligeros
  L231       · firmando tu trabajo
  L5472-5478 · gpg + git hash-object
  L7019-7117 · los entresijos internos (SHA-1 · objetos)

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3 · materializado en repo Programa SCFV
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: repositorio git ~/Programa-de-Investigacion-SCFV/ (31 commits, rama main, 1 remoto, 1 autor activo)
Nota metodológica: E3 se materializa dentro del repo del Programa. La auditoría ProGit recae sobre el régimen de versionado que aloja el artefacto.

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Integridad por checksum
  Todo objeto en git es verificado por SHA-1 antes de ser
  almacenado — L487-500.

C2 · Content-addressed storage
  Git guarda por hash del contenido, no por nombre de archivo
  — L500.

C3 · Snapshots inmutables
  Commit = copia instantánea; difícil de modificar tras
  confirmación — L446-506.

C4 · Identidad inmutable del autor
  Nombre y email del autor van sellados en el commit — L684.

C5 · Tags como puntos de referencia
  Tag anotado: checksum + etiquetador + fecha + mensaje
  — L2123. Tag ligero: solo checksum — L2162.

C6 · Firma GPG como capa adicional
  Firma criptográfica sobre commits y tags — L231, L5472-5478.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · INTEGRIDAD POR CHECKSUM

  C1-E1 · Content-addressed funcional
    Resultado: resiste
    Cita: L500 "Git guarda todo no por nombre de archivo, sino por el valor
    hash de sus contenidos."
    Ubicación: git log --pretty='%H' devuelve 40 hex por commit

  C1-E2 · Material no versionado fuera del mecanismo
    Resultado: falla
    Cita: L487-488 "Todo en Git es verificado mediante una suma de
    comprobación (checksum en inglés) antes de ser…"
    Ubicación: git status --porcelain → 17 archivos untracked en ACTAS/ +
    GIRO_06/ (todo el output del ciclo 6.0)

C2 · CONTENT-ADDRESSED STORAGE

  C2-E1 · BIBLIOTECA versiona solo metadata
    Resultado: parcial
    Cita: L506 "después de confirmar una copia instantánea en Git es muy
    difícil de [modificar]"
    Ubicación: git ls-files BIBLIOTECA/ = 119 archivos (solo CITAS/FICHA/
    INDICE.md); PDFs origen no versionados

  C2-E2 · .gitignore excluye *.txt / *.pdf
    Resultado: parcial
    Cita: L500 "por el valor hash de sus contenidos"
    Ubicación: .gitignore L1-7 (regla §5 Fundacional: binarios nunca
    al repo)

C3 · SNAPSHOTS INMUTABLES

  C3-E1 · 23 commits ahead de origin
    Resultado: falla
    Cita: L385-388 "los clientes no solo descargan la última copia
    instantánea… Cada clon es realmente una copia completa de…"
    Ubicación: git status -sb: ## main...origin/main [ahead 23]

  C3-E2 · Prefijos temáticos consistentes
    Resultado: resiste
    Cita: L450 "Git maneja sus datos como una secuencia de copias
    instantáneas"
    Ubicación: git log --oneline con prefijos biblioteca:, giro-04:,
    Giro 05:, fundacion:

  C3-E3 · Volumen estructural del repo
    Resultado: no aplica
    Cita: L446-457 (dato sin criterio asociado)
    Ubicación: 15 días · 31 commits · 1 rama · 0 submodules · 1 remoto

C4 · IDENTIDAD INMUTABLE DEL AUTOR

  C4-E1 · Divergencia de identidad en log
    Resultado: falla
    Cita: L684 "introducida de manera inmutable en los commits que envías"
    Ubicación: git log --pretty='%an <%ae>' = {DEDN <lic.dedn@gmail.com>,
    Tu Nombre <tu@email.com>}

  C4-E2 · Identidad local vs global divergente
    Resultado: parcial
    Cita: L668-684 "Tu Identidad… los commits de Git usan esta información"
    Ubicación: git config --get user.name = DEDN · ~/.gitconfig
    user.name = Domingo Eduardo Díaz Navas

C5 · TAGS COMO PUNTOS DE REFERENCIA

  C5-E1 · Ausencia de tags
    Resultado: falla
    Cita: L2123 "Tienen un checksum; contienen el nombre del etiquetador,
    correo electrónico y fecha; tienen un mensaje"
    Ubicación: git tag count=0 en 31 commits y 15 días

C6 · FIRMA GPG COMO CAPA ADICIONAL

  C6-E1 · Ausencia de firma
    Resultado: falla
    Cita: L231 "Firmando tu trabajo" · L5472-5475 gpg -a --export …
    git hash-object -w --stdin
    Ubicación: git log --pretty='%H %G? %GS' = N ×20 · user.signingkey
    vacío · commit.gpgsign vacío · tag.gpgsign vacío

  C6-E2 · Autenticación remota sin push
    Resultado: parcial
    Cita: (fuera de loci ProGit; régimen administrativo)
    Ubicación: ~/.gitconfig credential.helper = cache configurado, sin
    push efectivo

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                                Resiste  Parcial  Falla  No aplica
  ───────────────────────────────────────────────────────────────────────────
  C1 · Integridad por checksum               1        0       1       0
  C2 · Content-addressed storage             0        2       0       0
  C3 · Snapshots inmutables                  1        0       1       1
  C4 · Identidad inmutable del autor         0        1       1       0
  C5 · Tags como puntos de referencia        0        0       1       0
  C6 · Firma GPG                             0        1       1       0
  ───────────────────────────────────────────────────────────────────────────
  Total                                      2        4       5       1

  Emergencias registradas: 12

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  El repo Programa SCFV usa git de forma coherente con C1-C2: hashes
  SHA-1 de 40 caracteres, storage por contenido, prefijos temáticos
  consistentes en los mensajes de commit. La disciplina de nomenclatura
  ("biblioteca:", "giro-04:", "Giro 05:") es trazable.

D · Divergencia
  ProGit describe tags anotados y firma GPG como mecanismos
  estándar de congelamiento y autenticación. E3 materializado en el
  repo Programa no usa ninguno de los dos: 0 tags en 31 commits,
  0 commits firmados, sin signingkey configurada. El régimen de
  cierre del Giro 05 y del ciclo 6.0 opera sin punto de congelamiento
  canónico.

E · Emergencia
  E3 tiene cadena de versionado funcional, pero no tiene firma ni
  tags. Coincide con Patrón E (firma no criptográfica) ya detectado
  por Merkle y NIST. Desde tercer canon consecutivo: la firma es
  ausente en tres capas (decisión H2, commit, tag). Añade un patrón
  nuevo que el borrador nombra Patrón F · materialización sin
  congelamiento: 17 archivos untracked + 23 commits ahead + 0 tags.

E · Enriquecimiento
  ProGit da vocabulario técnico para deudas administrativas §8 del
  traspaso: "ahead of origin", "untracked", "unsigned", "no tags" son
  categorías estándar que permiten medir el régimen de versionado.
  El cierre de giro sin tag anotado no deja punto de referencia
  verificable.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
ProGit 2014 × SCFV_DSR E3.
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
  Constancia: acta 6.0.15 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

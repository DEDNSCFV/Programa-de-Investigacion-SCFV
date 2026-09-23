# Inventario de BIBLIOTECA

Estado al 2026-09-23. Verificable contra `REGISTRO_ENTRADAS.log` (hashes de PDFs origen).

Convención de estado:
- `poblado` — contenido sustantivo (más de 5 líneas)
- `placeholder` — esqueleto (1 línea)
- `vacío` — 0 líneas
- `—` — no aplica

Raws en HOME: 27 archivos (`~/.<nombre>_raw.txt`, permisos 600).
PDFs en Downloads: referenciados, no movidos.

---

## §1 · Entradas en BIBLIOTECA (25)

| # | Entrada | PDF origen (Downloads) | Raw (HOME) | FICHA | INDICE | CITAS | Estatuto |
|---|---|---|---|---|---|---|---|
| 1 | AccountingTheory_2004 | Accounting Theory-M. Com. .pdf | .accounting_theory_raw.txt | poblado | poblado | poblado | contable |
| 2 | Aho_2007 | Alfred-V.-Aho-...Compilers...2007.pdf | .aho_compilers_raw.txt | placeholder | placeholder | placeholder | técnico |
| 3 | Angrisani_2019 | — | .angrisani_raw.txt | poblado | poblado | poblado | contable |
| 4 | Cervantes_2023 | 648e625c...d38c.pdf | .cervantes_raw.txt | poblado | poblado | poblado | técnico |
| 5 | Cosmovision_2004 | LIBRO COSMOVISION.pdf | .cosmovision_raw.txt | poblado | poblado | poblado | contable |
| 6 | Diaz_Navarro_2014 | — | .diaz_navarro_raw.txt | poblado | poblado | poblado | contable |
| 7 | Gadamer_VM | — | .gadamer_raw.txt | poblado | poblado | poblado | metodológico |
| 8 | GarciaCasella_LaLey_SF | AC_U3_1_CLGC.pdf | .garcia_casella_raw.txt | placeholder | placeholder | placeholder | contable |
| 9 | GonzalezRodriguez_UO_2001 | UOV0010.pdf | .gonzalez_rodriguez_2001_raw.txt | placeholder | placeholder | placeholder | técnico |
| 10 | Hevner_Chatterjee_2010 | — | .hevner_raw.txt | poblado | poblado | poblado | metodológico |
| 11 | Huck_SistemasContables_2024 | sistemaContable_aa.pdf | .huck_raw.txt | poblado | poblado | poblado | contable |
| 12 | Lakatos_1976 | — | .lakatos_raw.txt | poblado | poblado | poblado | metodológico |
| 13 | Lakatos_1989 | lakatos-i-la-historia...pp-110-147.pdf | .lakatos_metodologia_raw.txt | poblado | poblado | poblado | metodológico |
| 14 | Merkle_1979 | Certified1979.pdf | .merkle_1979_raw.txt | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 15 | NIST_FIPS_180_4 | NIST.FIPS.180-4.pdf | .nist_fips_180_4_raw.txt | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 16 | Pacioli_1494 | A335068.pdf | .pacioli_summa_raw.txt (OCR destruido) | placeholder | placeholder | placeholder | contable |
| 17 | Popper_1980 | — | .popper_raw.txt | poblado | poblado | poblado | metodológico |
| 18 | ProGit_2014 | 2014_pro-git_es.pdf | .progit_2014_raw.txt | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 19 | Reynoso_Kicillof | introduccion-a-la-arquitectura-de-software.pdf | .reynoso_raw.txt | poblado | poblado | poblado | técnico |
| 20 | Rodriguez_2016 | — | .rodriguez_raw.txt | poblado | poblado | poblado | núcleo |
| 21 | RomeroLopez_2010 | Principios_de_contabilidad_4ta_Edicion.pdf | .principios_raw.txt | poblado | poblado | poblado | contable |
| 22 | Romney_15thEd | — | .romney_raw.txt | poblado | poblado | poblado | contable |
| 23 | Sampieri_2018 | — | .sampieri_raw.txt | poblado | poblado | poblado | metodológico |
| 24 | Sommerville_2005 | libro_689d10b028359.pdf | .sommerville_raw.txt | poblado | poblado | poblado | técnico |
| 25 | Thain_2ndEd | compilerbook.pdf | .thain_compilers_raw.txt | placeholder | placeholder | placeholder | técnico |

Las 8 entradas en placeholder (Aho_2007, GarciaCasella_LaLey_SF, GonzalezRodriguez_UO_2001, Merkle_1979, NIST_FIPS_180_4, Pacioli_1494, ProGit_2014, Thain_2ndEd) permanecen así hasta que un acto del programa las invoque (ver §4).

Gadamer_VM (2026-09-23): CITAS canónico + INDICE con sección «Anclaje en el raw» y 16 anclajes temáticos.

---

## §2 · Raws sin entrada en BIBLIOTECA

| Raw (HOME) | PDF origen | Estatuto propuesto |
|---|---|---|
| .baldor_algebra_raw.txt | ALGEBRA_de_BALDOR.pdf (38 MB, parcial pp.1-50) | aprendizaje-matemático |
| .boole_analysis_logic_raw.txt | mathematicalanal00booluoft.pdf | aprendizaje-matemático |

Ambos pendientes de entrada propia. No se crea entrada hasta invocación (ver §4).

---

## §3 · Deudas activas

| Deuda | Descripción | Estado |
|---|---|---|
| Mattessich fuente primaria | Ausente. Material secundario (UNET 2021, trabajo estudiantil) en Downloads, no procesado. | Abierta — Giro+5 |
| Pacioli OCR | Raw de 126 717 líneas con OCR destruido. No utilizable por texto. | Abierta — requiere transcripción alternativa |
| García Casella año | Sin fecha en metadata del PDF. Declarado `_SF` (sin fecha). | Abierta — verificación opcional |
| D-L Gadamer | 03_rutas.md y 04_ipve declaran «FICHA sin actualizar»; FICHA ya firmada por IA-2 (2026-09-18). Descoordinación declarativa, no material. | Abierta — actualizar o anular declaración obsoleta |

Deudas cerradas: **Raws pendientes** (Bloque 4), **Gadamer_VM/CITAS.md vacío** (2026-09-23).
OBS-MAT-13 reformulado: CITAS.md con formato declarado y citas vacías es **diseño**, no deuda.

---

## §4 · Convenciones

**Régimen de materialización**: nada se materializa sin uso. Un autor invocado por el corpus dispara el llenado de su FICHA (identidad), INDICE (secciones usadas) y CITAS (sólo si hay cita textual). Antes de la invocación, los tres archivos permanecen como placeholder.

Estados operativos derivados:

| Estado | FICHA | INDICE | CITAS |
|---|---|---|---|
| Autor no invocado | placeholder | placeholder | placeholder |
| Autor invocado, sin cita textual | poblado | poblado (secciones usadas) | formato declarado + vacío |
| Autor invocado con cita textual | poblado | poblado | poblado con C-NNN |

La regla aplica también a: material didáctico, corpus de aprendizaje, entradas nuevas por PDF disponible. Tener el PDF y el raw no es motivo para materializar; la invocación del corpus lo es.

**Hashes**: `REGISTRO_ENTRADAS.log` contiene SHA-256 de los PDFs origen. Los raws no están registrados aún (decisión pendiente: crear `REGISTRO_RAWS.log`).

**PDFs**: viven en `~/storage/downloads/`. No se mueven. Se referencian por nombre.

**Raws**: viven en `~/.<nombre>_raw.txt`, ocultos, permisos 600. Respaldo periódico a MEGA.

**FICHA.md**: qué es la obra, autores, año, editorial, estatuto.
**INDICE.md**: secciones, páginas y anclajes verificados en el raw.
**CITAS.md**: citas textuales operativas — efectivamente usadas para fundamentar una operación. No candidatas, no anticipadas.

**Estatutos**:
- `núcleo` — componente del núcleo firme (§9).
- `contable` / `metodológico` / `técnico` — cinturón protector por área.
- `aprendizaje-cripto` — material de estudio, sin estatuto programático.
- `aprendizaje-matemático` — idem para álgebra y lógica.

---

*Actualizado 2026-09-23. Régimen de materialización declarado. Verificable contra REGISTRO_ENTRADAS.log.*

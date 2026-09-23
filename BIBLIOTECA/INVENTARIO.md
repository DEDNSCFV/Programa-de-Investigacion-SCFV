# Inventario de BIBLIOTECA

Estado al 2026-09-23. Verificable contra `REGISTRO_ENTRADAS.log` (hashes externos).

Convención de estado:
- `poblado` — contenido sustantivo (más de 5 líneas)
- `placeholder` — esqueleto (1 línea)
- `vacío` — 0 líneas
- `—` — no aplica

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
| 7 | Gadamer_VM | — | .gadamer_raw.txt | poblado | poblado | **vacío** | metodológico |
| 8 | GarciaCasella_LaLey_SF | AC_U3_1_CLGC.pdf | (pendiente) | placeholder | placeholder | placeholder | contable |
| 9 | GonzalezRodriguez_UO_2001 | UOV0010.pdf | (pendiente) | placeholder | placeholder | placeholder | técnico |
| 10 | Hevner_Chatterjee_2010 | — | .hevner_raw.txt | poblado | poblado | poblado | metodológico |
| 11 | Huck_SistemasContables_2024 | sistemaContable_aa.pdf | .huck_raw.txt | poblado | poblado | poblado | contable |
| 12 | Lakatos_1976 | — | .lakatos_raw.txt | poblado | poblado | poblado | metodológico |
| 13 | Lakatos_1989 | lakatos-i-la-historia...pp-110-147.pdf | .lakatos_metodologia_raw.txt | poblado | poblado | poblado | metodológico |
| 14 | Merkle_1979 | Certified1979.pdf | (pendiente) | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 15 | NIST_FIPS_180_4 | NIST.FIPS.180-4.pdf | (pendiente) | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 16 | Pacioli_1494 | A335068.pdf | .pacioli_summa_raw.txt (parcial OCR) | placeholder | placeholder | placeholder | contable |
| 17 | Popper_1980 | — | .popper_raw.txt | poblado | poblado | poblado | metodológico |
| 18 | ProGit_2014 | 2014_pro-git_es.pdf | (pendiente) | placeholder | placeholder | placeholder | aprendizaje-cripto |
| 19 | Reynoso_Kicillof | introduccion-a-la-arquitectura-de-software.pdf | .reynoso_raw.txt | poblado | poblado | poblado | técnico |
| 20 | Rodriguez_2016 | — | .rodriguez_raw.txt | poblado | poblado | poblado | núcleo |
| 21 | RomeroLopez_2010 | Principios_de_contabilidad_4ta_Edicion.pdf | .principios_raw.txt | poblado | poblado | poblado | contable |
| 22 | Romney_15thEd | — | .romney_raw.txt | poblado | poblado | poblado | contable |
| 23 | Sampieri_2018 | — | .sampieri_raw.txt | poblado | poblado | poblado | metodológico |
| 24 | Sommerville_2005 | libro_689d10b028359.pdf | .sommerville_raw.txt | poblado | poblado | poblado | técnico |
| 25 | Thain_2ndEd | compilerbook.pdf | .thain_compilers_raw.txt | placeholder | placeholder | placeholder | técnico |

---

## §2 · Materiales sin entrada en BIBLIOTECA

Raws en HOME sin directorio correspondiente:

| Raw (HOME) | PDF en Downloads | Estatuto propuesto |
|---|---|---|
| .baldor_algebra_raw.txt | ALGEBRA_de_BALDOR.pdf (38 MB) | aprendizaje-matemático |
| .boole_analysis_logic_raw.txt | mathematicalanal00booluoft.pdf | aprendizaje-matemático |
| .gadamer_raw.txt | (sin PDF) | (ya tiene entrada) |
| .popper_raw.txt | (sin PDF) | (ya tiene entrada) |

PDFs en Downloads sin raw ni entrada:

| PDF en Downloads | Notas |
|---|---|
| UOV0010.pdf | ya tiene entrada — GonzalezRodriguez_UO_2001 |
| A335068.pdf | ya tiene entrada — Pacioli_1494 |
| AC_U3_1_CLGC.pdf | ya tiene entrada — GarciaCasella_LaLey_SF |
| 648e62...d38c.pdf | ya tiene entrada — Cervantes_2023 |
| libro_689d10b028359.pdf | ya tiene entrada — Sommerville_2005 |
| introduccion-a-la-arquitectura-de-software.pdf | ya tiene entrada — Reynoso_Kicillof |

---

## §3 · Deudas activas

| Deuda | Descripción | Bloque afectado |
|---|---|---|
| Mattessich | Fuente primaria ausente. Material secundario (UNET 2021, trabajo estudiantil) disponible en Downloads, no procesado. | Giro+5 |
| Pacioli Tractatus | OCR degradado. Verificación por texto imposible. Se requiere transcripción alternativa. | Bloque 5 |
| García Casella año | Sin fecha en metadata del PDF. Declarado `SF` (sin fecha) hasta verificación adicional. | Bloque 5 |
| Gadamer CITAS vacío | Contradice OBS-MAT-13 (que declaraba 17/17 con 0 citas operativas). Aquí el archivo está literalmente vacío. | Giro+5 |
| Raws pendientes | 6 raws a extraer a HOME: garcia_casella, gonzalez_rodriguez_2001, nist_fips, merkle, progit, pacioli_completo. | Bloque 4 |

---

## §4 · Convenciones

**Hashes**: viven en `REGISTRO_ENTRADAS.log`, no embebidos en los archivos. Verificación externa con `sha256sum`.

**PDFs**: se referencian por nombre desde `~/storage/downloads/`. No se mueven ni copian. Fuente física única.

**Raws**: viven en `~/.<nombre>_raw.txt`, ocultos, permisos 600. Se respaldan a MEGA periódicamente.

**FICHA.md**: qué es la obra, autores, año, editorial, estatuto en el programa.
**INDICE.md**: secciones y páginas, extraídas del raw cuando el acto lo requiera.
**CITAS.md**: citas operativas — aquellas efectivamente usadas en documentos del programa. No candidatas.

**Estatutos**:
- `núcleo` — componente del núcleo firme (§9).
- `cinturón` / `contable` / `metodológico` / `técnico` — cinturón protector por área.
- `aprendizaje-cripto` — material de estudio, sin estatuto programático.
- `aprendizaje-matemático` — idem para álgebra y lógica.

---

*Generado 2026-09-23. Verificable contra REGISTRO_ENTRADAS.log.*

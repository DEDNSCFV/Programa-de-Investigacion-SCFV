# ACTA A-1.3 — Clasificación documental del defecto numérico

**Programa:** Programa de Investigación SCFV  
**Giro:** 03  
**Acto:** A-1.3  
**Fecha:** 2026-09-18  
**Estado:** MATERIALIZADO — DEUDA ABIERTA

## 1. Unidad y alcance

**Unidad:** clasificación documental, bajo el §9 del Protocolo de Revisión de Actos Materializados, del defecto numérico detectado en `scfv_architect.py`.

**Objeto revisado:** plantilla histórica/inactiva de compras.

**Alcance:** existencia, naturaleza técnica, condición histórica/inactiva y consecuencias documentales del defecto. No se realiza modificación del código.

## 2. Resultados por eje

### Eje 1 — Falsación: PASS

La afirmación evaluada —que la fórmula constituye un defecto numérico real— resistió el intento de refutación.

### Eje 2 — Deconstrucción: OBJECIÓN

La fórmula:

`iva = monto * IVA_TASA / 100000000`

materializa una escala incompatible con `IVA_TASA = 0.12`. El defecto es reproducible y no posee origen documental identificado en el corpus, `scfv_v6` ni en la historia Git revisada.

### Eje 3 — Horizonte Rodriguiano: PASS

El tratamiento documental distingue la existencia técnica del defecto de su condición histórica/inactiva y no atribuye impacto productivo no demostrado. Es coherente con el motor epistemológico del Programa.

## 3. IPVE

**I — Invariante:** `IVA_TASA = 0.12` permanece constante en las fuentes verificadas; la fórmula revisada contiene `/100000000`.

**P — Propiedad:** la fórmula produce un cálculo incorrecto del IVA, aunque no impide por sí misma el balance formal de la partida.

**V — Validaciones:** cuantificación matemática, búsqueda de invocaciones, búsqueda de patrón, revisión de procedencia, cronología y Git.

**E — Evidencias:** `scfv_architect.py`, fuentes de `IVA_TASA`, resultados de búsqueda y dictámenes IA-1/IA-2.

## 4. Decisión del Operador

El Operador ratifica la lectura adoptada del §4 para este acto:

- Eje 1: PASS.
- Eje 2: OBJECIÓN.
- Eje 3: PASS.

El Operador **convierte expresamente la objeción del Eje 2 en DEUDA**.

La deuda es técnica/documental y no bloqueante. Esta clasificación no implica defecto operativo de S0 ni exige modificar la versión publicada.

## 5. Estado de la deuda

La deuda permanece **ABIERTA**.

No queda saldada por esta acta. Su cierre requerirá un acto posterior con resolución explícita, evidencia, verificación y decisión del Operador.

## 6. Trazabilidad

Hallazgos relacionados: HL-176, HL-177, HL-178, HL-179 y HL-180.

**IA-1:** constancia de construcción e integración.  
**IA-2:** constancia de falsación y verificación.  
**Operador:** decisión y autorización de materialización.

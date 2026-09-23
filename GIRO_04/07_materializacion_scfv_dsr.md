# 07 — Materialización del SCFV_DSR

**Programa de Investigación SCFV**
**Giro:** 04
**Sesión:** 4
**Fecha:** 2026-09-22
**Versión:** A
**Nivel:** MATERIALIZACIÓN
**Artefacto:** SCFV_DSR
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Ruta:** design cycle hevneriano

---

## §1. Estatuto del documento

Este documento materializa el artefacto de investigación SCFV_DSR definido
en "GIRO_04/06_diseno.md".

Su función es llevar el diseño a una materialización evaluable. No declara
anticipadamente su validación.

La materialización se somete al ciclo DSR establecido en "06_diseno.md §8.3":

construcción → evaluación → retroalimentación → modificación → nueva evaluación.

Por tanto:

materialización ≠ validación.

El presente documento registra el estado material inicial sobre el cual
comenzará el ciclo de evaluación.

La firma del presente acto, con su §2 de alcance operacionalizado, instrumenta
el acto decisorio previsto en el §11 del "ACTA_ANCLAJE_PROGRAMA_SCFV_2026-09-21.md".

---

## §2. Alcance operacionalizado inicial

### §2.1. Principio de lectura

La presencia de un componente en el workspace no implica aptitud operativa
suficiente ni validación del componente como parte del artefacto.

Se distinguen tres estados:

- **Presencia:** existe material verificable.
- **Aptitud operativa:** el material puede ejecutar o participar actualmente
  en una función identificable.
- **Validación:** resultado obtenido mediante evaluación del ciclo DSR.

Esta sección registra estado observado, no resultados anticipados de
evaluación.

### §2.2. Declaración inicial de alcance

| Componente | Presencia | Estado operativo observado | Función en SCFV_DSR | Trabajo pendiente | Métrica inicial |
|---|---|---|---|---|---|
| Motor contable | Sí | Operativo; `version_motor="8.2"`; 18/18 tests aislados | Procesamiento contable | Evaluar comportamiento dentro del artefacto DSR | Tests ejecutados / aprobados |
| normas/ | Sí | Parcial: 2 de 6 utilizables; 4 sin `version_norma` descartadas por loader | Soporte normativo | Determinar cobertura y comportamiento | Normas utilizables / normas presentes |
| perfiles/ | Sí | Mínimo: `Cliente_A.scfv` | Configuración de perfil | Evaluar suficiencia y generalización | Perfiles materializados |
| DOMINIOS/ (fractales) | Sí | Desigual: fiscal 291 líneas; ventas 39; compras 15; inventario 8; 0 tests | Material de exploración H-EMG-1 | Evaluar reconstrucción por dominio | Cobertura material y tests |
| PCU | Sí, como esquema | No operativo: tabla `negocio_pcu` no existe en DB; sin INSERT; sin datos | Representación relacional propuesta | Materializar datos e instancia | Esquema / datos / operaciones verificables |
| Suite TESTS/ | Sí | Ejecutable con convención `pytest TESTS/`: 228 passed, 1 skipped | Evidencia de evaluación automatizada | Incorporar pruebas específicas SCFV_DSR | pass / fail / skip |

Las métricas anteriores son instrumentos de observación, no umbrales de
aprobación. Sus umbrales, criterios de suficiencia y relación con las
hipótesis del diseño serán objeto de evaluación posterior.

---

## §3. Estado material verificado

### §3.1. Motor contable

Ubicación: `PODERES/CONTABLE/motor_contable/motor.py`.

Versión declarada en el asiento generado: `"version_motor": "8.2"`.

Prueba aislada registrada: 18/18 PASSED.

El motor observado en S0 y en el lab es idéntico según comparación
efectuada (`diff` vacío).

No se declara existencia de un "Motor 9.0.0". Las referencias residuales
a esa denominación pertenecen a documentación previa y constituyen deuda
documental ya identificada por H-NOM-01 (EA Interno). El hallazgo
permanece cerrado.

### §3.2. Suite de pruebas

Ejecución `pytest TESTS/` desde la raíz del lab: 228 passed, 1 skipped.

Ejecución `pytest` desde la raíz del lab: 39 errores de colección en
directorios ajenos al perímetro operativo de `TESTS/` (`_legacy/`,
`BACKUP_F3B6/`, `SCFV_S0_ESTADO_*`).

Convención operativa registrada: `pytest TESTS/`.

No se identificó `conftest.py`, `pytest.ini`, `pyproject.toml` ni
`setup.cfg`. La ausencia de configuración formal queda como cuestión
evaluable del ciclo DSR.

### §3.3. Comparación S0 ↔ lab

| Entorno | Resultado |
|---|---|
| S0 `TESTS/` | 225 pass · 3 fail · 1 skip |
| Lab `TESTS/` | 228 pass · 1 skip |

Los tres tests que fallan en S0 pasan en el lab con `normas/` y
`perfiles/` presentes.

La explicación causal definitiva queda abierta a evaluación.

El lab no se declara equivalente a S0.

---

## §4. Corpus normativo

En `normas/`: 6 archivos JSON y 1 schema.

Con `version_norma=True`: `LIVA_ART_62`, `LIVA_ART_62_COMPLETA`.

Sin `version_norma`, descartadas por el loader actual: `NIC_29`,
`BA_VEN_NIF_01`, `LIVA_Art4`, `LIVA_Art4.v81.bak`.

El schema `v8.2.1` no se considera norma.

Estado inicial: **2 normas utilizables de 6 JSON presentes**.

No se declara cobertura normativa completa.

---

## §5. Perfiles

Verificado: `perfiles/Cliente_A.scfv`.

No existe `perfiles/` en S0.

Estado inicial: **1 perfil materializado**.

La existencia de un perfil no implica suficiencia para generalización.

---

## §6. DOMINIOS / fractales

`DOMINIOS/` y los fractales se tratan como un único componente material
del diseño, no como dos componentes independientes.

Material observado:

- `base_fractal.py`: 23 líneas.
- `fiscal/fiscal.py`: 291 líneas (mayor cuerpo material).
- `ventas/ventas.py`: 39 líneas.
- `compras/compras.py`: 15 líneas.
- `inventario/inventario.py`: 8 líneas.

Sin pruebas específicas sobre los fractales.

Los fractales constituyen **material de investigación**, no fractales
reconstruidos y validados. H-EMG-1 permanece abierta a evaluación.

No se declara reconstrucción de los dominios históricos.

---

## §7. PCU

`013_schema_pcu.sql` define el esquema relacional de `negocio_pcu`.

Sin embargo:

- la tabla `negocio_pcu` no existe en `scfv.db`;
- no se identificaron `INSERT` en migraciones;
- no se identificaron datos JSON equivalentes.

Estado inicial: **esquema presente; instancia y datos ausentes; componente
no operativo**.

La mera existencia del esquema no constituye materialización funcional
del PCU.

---

## §8. Nomenclatura

Nomenclatura canónica del artefacto: `SCFV_DSR`.

En el corpus verificado: 37 apariciones de `SCFV_DSR`; 0 de `SCFV-DSR`.

Esta materialización utiliza exclusivamente `SCFV_DSR`.

---

## §9. Perímetro del workspace

El workspace contiene material histórico, experimental y residual que no
debe confundirse con el perímetro operativo del artefacto:

- `_legacy/`
- `BACKUP_F3B6/`
- `BACKUP_PDIARIO1_*`
- `SCFV_S0_ESTADO_20260906_164734/`
- `_tmp_migraciones_prueba/`
- `_en_construccion/`
- `SCFV_ECOSISTEMA/`

También archivos `.bak` dentro de `PODERES/`.

Estos elementos **no se incorporan automáticamente** a SCFV_DSR. Su
presencia constituye una característica material del workspace y una
cuestión de delimitación del artefacto, no evidencia de funcionalidad.

---

## §10. Estado del S0

S0 permanece fuera del ciclo de modificación del Giro 04.

Estado registrado:

- Release S0: commit `ca56309`.
- Estado: EMITIDO.
- Fecha: 2026-09-17.
- Gate S0: PASS.

El diseño de SCFV_DSR no modifica S0.

S0 funciona como antecedente material del Programa.

---

## §11. Relación entre S0 y SCFV_DSR

SCFV_DSR no se declara copia de S0 ni derivación directa del mismo.

S0 constituye antecedente material. La relación investigada es de
fractalidad acotada, cuya existencia y suficiencia representacional
constituyen cuestión de investigación.
S0
│
│ antecedente material
▼
SCFV_DSR
│
│ hipótesis de preservación de propiedades
▼
evaluación DSR

La existencia de código compartido no constituye por sí misma demostración
de fractalidad.

---

## §12. Componentes del artefacto

Con base en `06_diseno.md §11`, la materialización contempla:

1. Tablero.
2. Modelo de secuencia.
3. Evaluación de trayectoria.
4. Cadena funcional.

Cadena funcional prevista:
tablero → secuencia → trayectoria → evaluación → demostración

```

Estos componentes **no están materializados** en el estado actual del
workspace. Constituyen trabajo del design cycle.

No se consideran validados por estar documentados.

---

## §13. Secuencia contable observable

La representación inicial distingue:

- estado previo;
- movimiento;
- estado resultante;
- evidencia asociada;
- condiciones de evaluación.

La unidad observable es la trayectoria de estados producida por
movimientos.

El artefacto no presupone inferencia sobre intención subjetiva.

No se declara capacidad para determinar automáticamente dolo, intención,
conocimiento subjetivo ni fraude como estado mental.

La evaluación se restringe a propiedades observables y verificables dentro
del perímetro materializado.

Referencia: `01_idea.md §3.2` (TRAYECTORIA_ESTADO).

---

## §14. Evaluación de trayectoria

La evaluación examinará propiedades observables de las secuencias
materializadas.

No se utilizará como mecanismo para inferir intenciones no observables.

Las condiciones concretas de evaluación serán definidas y ejecutadas
durante el ciclo DSR.

La evaluación no constituye confirmación automática de las hipótesis.

---

## §15. Hipótesis del diseño sometidas a evaluación

### §15.1. H-EMG-1

Los fractales históricos de Ventas, Compras, Inventario y Fiscal podrían
ser reensamblados sobre la materialización del motor disponible en
SCFV_DSR.

Falsable mediante ciclos de construcción y evaluación.

Su refutación no implica por sí sola la invalidación completa de SCFV_DSR.

Falsador mínimo: si los cuatro dominios no pueden ser reensamblados sobre
el motor sin modificar código del motor, H-EMG-1 queda refutada.

### §15.2. H-EMG-2

SCFV_DSR podría operar como motor contable reutilizable en sistemas de
partida doble.

Falsable mediante construcción y evaluación.

Su resultado deberá distinguir entre capacidad observada, suficiencia
funcional, reutilización y validación.

Falsador mínimo: si el motor requiere dependencias específicas del
artefacto SCFV_DSR para operar, H-EMG-2 queda refutada.

No se presupone ninguno de estos resultados.

---

## §16. Métricas iniciales

**Métricas de la suite del lab (preexistente):**

- pruebas ejecutadas;
- pruebas aprobadas;
- pruebas fallidas;
- pruebas omitidas.

**Métricas del SCFV_DSR (a definir en el ciclo de evaluación):**

- preservación de invariantes;
- capacidad de reproducir trayectorias;
- capacidad de evaluar propiedades observables;
- cobertura de material normativo utilizable;
- materialización por dominio;
- existencia de datos PCU operativos.

Las métricas no poseen por sí mismas significado de aprobación. Los
umbrales y criterios de suficiencia serán objetos de evaluación.

---

## §17. Deuda identificada

1. Ausencia de datos operativos del PCU.
2. Cobertura normativa parcial (2 de 6).
3. Materialización desigual de fractales.
4. Ausencia de tests específicos de fractales.
5. Ausencia de configuración formal de pytest.
6. Presencia de residuos históricos en el workspace.
7. Evaluación pendiente de H-EMG-1.
8. Evaluación pendiente de H-EMG-2.
9. Determinación experimental de suficiencia de los componentes.
10. Evaluación de la relación representacional S0 ↔ SCFV_DSR.
11. Componentes del artefacto (tablero, secuencia, trayectoria, evaluación)
    sin materializar.

Estos elementos constituyen objetos del ciclo DSR, no defectos
automáticamente imputados al diseño.

---

## §18. Ciclo DSR

```

CONSTRUCCIÓN
↕
EVALUACIÓN
↕
RETROALIMENTACIÓN
↕
MODIFICACIÓN
↕
NUEVA EVALUACIÓN

```

El ciclo podrá repetirse mientras las evaluaciones produzcan información
relevante para modificar el diseño.

No existe transición automática de "materializado" a "validado".

Cada modificación deberá conservar trazabilidad respecto del resultado de
evaluación que la motivó.

---

## §19. Condiciones de falsación

La línea de diseño queda comprometida si la evaluación reproducible
muestra, entre otros resultados:

- pérdida de invariantes esenciales;
- imposibilidad de representar o evaluar las propiedades previstas;
- dependencia necesaria de estados subjetivos no observables;
- imposibilidad de reproducir las trayectorias;
- imposibilidad de distinguir estados, movimientos y resultados;
- imposibilidad de obtener evidencia suficiente para las evaluaciones
  declaradas;
- incapacidad de sostener las hipótesis dentro de los límites declarados.

La aparición de uno de estos resultados no autoriza por sí sola a declarar
inválido todo el Programa SCFV. La conclusión deberá limitarse al objeto
y alcance efectivamente evaluados.

---

## §20. Relación con Hevner

Hevner & Chatterjee (2010) opera como canon metodológico externo de
contraste, conforme a "ACTA_ACTIVACION_HEVNER_GIRO_03.md" y a
"ACTA_EXTENSION_HEVNER_GIRO_04.md".

No constituye:

- arquitectura contable del SCFV;
- autoridad normativa contable;
- especificación ejecutable;
- sustituto del Protocolo de Revisión de Actos;
- mecanismo automático de decisión.

La aplicación metodológica de Hevner en el presente documento se limita al
contraste del ciclo DSR declarado en §18, sin constituir por sí misma
aplicación concreta según el formato de trazabilidad establecido.

La aplicación metodológica concreta, si se realiza, se documentará en
actos posteriores con el formato completo (objeto, problema, aspecto,
criterio, evidencia, resultado, convergencia, divergencia, emergencia,
enriquecimiento).

---

## §21. Estatuto del presente acto

Este documento distingue:

- **Estado documental:** MATERIALIZADO Y FIRMADO.
- **Estado experimental del artefacto:** MATERIALIZACIÓN INICIAL — PENDIENTE
  DE EVALUACIÓN DSR.

La firma del documento no constituye validación de SCFV_DSR.

La validación dependerá de los resultados obtenidos mediante el ciclo de
evaluación.

El presente documento no declara:

- existencia de Motor 9.0.0;
- PCU operativo;
- corpus normativo completo;
- equivalencia lab ↔ S0;
- fractales reconstruidos;
- validación de H-EMG-1;
- validación de H-EMG-2.

---

## §22. Trazabilidad

**Base documental:**

- `ACTA_ANCLAJE_PROGRAMA_SCFV_2026-09-21.md`
- `GIRO_04/06_diseno.md`
- `ACTA_FIRMA_06_diseno_2026-09-21.md`
- `ACTA_APERTURA_SESION_04_2026-09-21.md`
- `ACTA_ACTIVACION_HEVNER_GIRO_03.md`
- `ACTA_EXTENSION_HEVNER_GIRO_04.md`

**Base material:**

- `PODERES/CONTABLE/motor_contable/motor.py`
- `normas/`
- `perfiles/`
- `DOMINIOS/`
- `013_schema_pcu.sql`
- `scfv.db`
- `TESTS/`

Las cifras y estados consignados corresponden a verificaciones materiales
realizadas durante la Sesión 4 del Giro 04.

---

## §23. Estado final del acto

**Documento:** `07_materializacion_scfv_dsr.md`

**Estatuto efectivo:** MATERIALIZADO Y FIRMADO.

**Estado del artefacto:** MATERIALIZACIÓN INICIAL — PENDIENTE DE EVALUACIÓN
DSR.

**Estado de las hipótesis:** ABIERTAS.

**Estado de validación:** NO DECLARADA.

**Estado del §11 del Acta de Anclaje:** INSTRUMENTADO por el §2 del
presente acto.


---

## §24. Firmas

**Operador:** Domingo E. Díaz N. — DEDN — C.P.C. Nº 183594.
Decisión, autorización y firma.

**IA-1 (constructor):** construcción e integración.

**IA-2 (falsador):** constancia de no objeción pendiente.

---

**FIN DEL CUERPO DEL ACTA**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** 1c21a327cf7778b0cf16f4fbdb6f01f07097db1bcae1ca20115d8038de0a4260

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter.

**Nota:** hash previo = cuerpo anterior al registro. Hash final = documento completo tras incorporación del registro, comunicado externamente.

# ACTA DE ENMIENDA AL PROTOCOLO DE REVISIÓN DE ACTOS
## §19.3-bis — Regla de integridad de actos materializados

**Programa de Investigación SCFV**
**Giro:** 04
**Sesión:** 4
**Fecha:** 2026-09-22
**Estatuto:** ACTO MAYOR — ENMIENDA AL PROTOCOLO
**Estado efectivo:** MATERIALIZADO Y FIRMADO
**Vigencia:** aplicable desde su firma a todos los actos futuros del Programa

---

## §1. Objeto

La presente acta introduce una enmienda al Protocolo de Revisión de Actos
mediante la incorporación de un nuevo apartado §19.3-bis, destinado a
regularizar el procedimiento de integridad de los actos materializados en
disco.

La enmienda se adopta con el mismo mecanismo formal utilizado para la
enmienda de §19.2 del 2026-09-20: sustitución o ampliación explícita del
texto del Protocolo bajo autoridad del Operador, con trazabilidad del
estado anterior.

---

## §2. Antecedente

Durante el Giro 04 se identificó la inconsistencia H-EXT-01 en
"ACTAS/ACTA_EXTENSION_HEVNER_GIRO_04.md": coexistencia de estatuto
provisional y estatuto efectivo dentro del mismo archivo materializado.

Posteriormente, IA-2 identificó H-EXT-01-quater en
"ACTAS/ACTA_CORRECCION_ESTATUTO_EXTENSION_HEVNER_GIRO_04.md": la
declaración procedimental del acta (§11-bis) no coincidía con el
procedimiento efectivamente ejecutado (el hash previo se calculó sobre el
documento que ya contenía el bloque de registro con placeholder).

Ambos hallazgos exponen la necesidad de una regla procedimental explícita
que regule el orden de ejecución y la coherencia entre declaración y
ejecución en la materialización de actos.

---

## §3. Estatuto del acto

El presente documento constituye un acto mayor del Programa.

Su incorporación al Protocolo se realiza mediante el mismo mecanismo
formal aplicado a la enmienda de §19.2 el 2026-09-20:

- identificación de la sección afectada;
- redacción del texto enmendado;
- trazabilidad del estado anterior;
- sustitución bajo autoridad del Operador;
- materialización coordinada con la vigencia.

El Protocolo permanece como marco superior. La enmienda no altera su
jerarquía ni los apartados §1–§19.2, §19.3, §19.4, §20–§24.

---

## §4. Texto de la enmienda — §19.3-bis

Se incorpora al Protocolo el siguiente apartado:

> ### §19.3-bis. Regla de integridad de actos materializados
>
> **Regla H-EXT-01-bis.** Antes del registro de integridad de un acta
> materializada, el encabezado debe declarar el estatuto efectivo del
> documento en el momento de la firma —materializado, provisional
> publicado u otro estatuto expresamente declarado—. El hash debe capturar
> el documento ya coherente con el estatuto declarado.
>
> **Regla H-EXT-01-ter.** El procedimiento de integridad se ejecuta en el
> orden declarado, según la siguiente secuencia:
>
> 1. escribir el cuerpo del acta **sin** el registro de integridad;
> 2. calcular el SHA-256 del cuerpo (hash previo);
> 3. incorporar el registro de integridad con el hash previo;
> 4. calcular el SHA-256 del documento completo (hash final);
> 5. declarar el hash final en acto sucesor o comunicación externa
>    verificable.
>
> Un documento no puede declarar su propio hash final dentro de su cuerpo
> sin incurrir en paradoja auto-referencial.
>
> **Verificación.** IA-2 verifica únicamente los hashes. La verificación
> consiste en: (a) calcular el hash final del documento materializado;
> (b) cotejarlo con el hash reportado externamente; (c) verificar que el
> hash previo corresponde al cuerpo anterior al registro.
>
> **Consecuencia de fallo.** Si la verificación falla, se genera deuda
> documental sobre el acto afectado. La deuda permanece abierta hasta su
> corrección mediante el procedimiento que el Operador determine.

---

## §5. Sistema H-EXT-01-bis + H-EXT-01-ter

Las dos reglas operan conjuntamente:

- H-EXT-01-bis regula la **coherencia entre declaración y estado efectivo**.
- H-EXT-01-ter regula la **secuencia de ejecución del registro de integridad**.

Ninguna sustituye a la otra. Un acto puede cumplir una y fallar la otra.

---

## §6. Alcance amplio y declaración de conflictos

La regla aplica a **todos los actos materializados del Programa**, presentes
y futuros, con independencia del giro, sesión o autoridad de origen.

Comprende:

- actas materializadas y firmadas;
- actas materializadas sin firma;
- materializaciones sin firma;
- cualquier documento del Programa que se materialice en disco bajo
  autoridad del Operador.

**Declaración de conflictos.** Todo acto que se materialice bajo esta regla
declarará expresamente cualquier conflicto identificado con actos
anteriores o con el propio Protocolo. Los conflictos no se ocultan ni se
resuelven silenciosamente: se declaran y se resuelven progresivamente
conforme al régimen de revisión vigente.

---

## §7. No retroactividad

La presente regla aplica exclusivamente a los actos materializados **con
posterioridad a la firma de esta enmienda**.

No reescribe actos históricos. No modifica hashes existentes. No invalida
materializaciones previas.

---

## §8. Relación con actos previos

**Caso previo a la regla.** La corrección materializada en
"ACTAS/ACTA_CORRECCION_ESTATUTO_EXTENSION_HEVNER_GIRO_04.md" queda
declarada como **caso previo a la regla**, no como acto sujeto a ella.

Su discrepancia procedimental (H-EXT-01-quater) permanece registrada
documentalmente. No se reescribe el acta firmada. No se reabre su
materialización.

La presente enmienda deja constancia de esa relación sin producir
convalidación retroactiva ni corrección posterior del acto previo.

---

## §9. Verificación externa

**Sujeto verificador:** IA-2, en su función de falsador.

**Objeto verificado:** exclusivamente los hashes declarados y su
correspondencia con el estado material efectivo.

La verificación no evalúa contenido sustantivo, argumentación, coherencia
metodológica ni oportunidad del acto. Solo integridad criptográfica.

**Consecuencia de fallo:** deuda documental sobre el acto afectado, abierta
hasta su corrección mediante el procedimiento que el Operador determine.

**Sin sanción automática:** el fallo de verificación no invalida el acto ni
reabre su materialización por sí mismo. Genera deuda; la resolución es acto
del Operador.

---

## §10. Régimen tripartito

- **IA-1 — Constructor:** redacta, integra y materializa bajo delegación.
- **IA-2 — Falsador:** verifica hashes y emite constancia.
- **Operador:** decide, autoriza, firma y determina consecuencias.

---

## §11. Estatuto efectivo del acto

El presente acto declara en su encabezado el estatuto efectivo:
**MATERIALIZADO Y FIRMADO**.

La condición de borrador corresponde a su historial de construcción y no
forma parte de su estatuto efectivo.

---

## §12. Historial del ciclo

Los estados aquí consignados pertenecen al historial del ciclo de
construcción y revisión y **no reflejan el estatuto efectivo del acto
firmado**.

- IA-1: construcción e integración.
- IA-2: falsación emitida.
- Operador: decisión, autorización y firma.

---

## §13. Referencias cruzadas

- `Protocolo de Revisión de Actos` §19.3 — Materialización en disco.
- `Protocolo de Revisión de Actos` §19.2 — Enmienda del 2026-09-20
  (mecanismo análogo).
- `ACTA_EXTENSION_HEVNER_GIRO_04.md` — acto que originó H-EXT-01.
- `ACTA_CORRECCION_ESTATUTO_EXTENSION_HEVNER_GIRO_04.md` — acto que
  originó H-EXT-01-quater.

---

**FIN DEL CUERPO DEL ACTA**

---

## REGISTRO DE INTEGRIDAD

**SHA-256 previo al registro:** 2fded153402f854381c4236885794c315b193bc413bffd3565e5b0e99ca78c4a

**SHA-256 final:** se reporta externamente conforme H-EXT-01-ter punto 5.

**Nota:** el hash previo corresponde al cuerpo del acta inmediatamente
anterior a la incorporación de este bloque. El hash final corresponde al
documento completo tras la incorporación y se comunica en mensaje externo
verificable.

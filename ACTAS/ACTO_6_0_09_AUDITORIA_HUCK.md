════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON HUCK 2024
DOCUMENTO: ACTAS/ACTO_6_0_09_AUDITORIA_HUCK.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Coordinadora: Norma Huck
Obra: Sistemas contables: una visión integral
Editorial: Ediciones UNL · 2024
Raw: ~/.huck_raw.txt · 8.504 líneas
Naturaleza: sistemas contables comparados · visión integral

Loci invocados:
  L120      · introducción y desarrollo de un sistema contable
  L560-568  · contabilidad como sistema de información
  L569-571  · cada ente tiene su propio sistema contable
  L584-588  · presente y futuro de la contabilidad
  L700-714  · implementación o rediseño de sistema contable

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Sistema contable como sistema de información
  La contabilidad forma parte del sistema de información de una
  organización — L120, L560-568.

C2 · Cada ente tiene su propio sistema contable
  Cada ente tiene su propio sistema contable, similar a otros
  pero nunca igual — L569-571.

C3 · Contabilidad para el presente y el futuro
  Brinda información del presente y permite formular planes de
  acciones futuras — L584-588.

C4 · Implementación / rediseño
  Al implementar o rediseñar un sistema contable — L700-714.

C5 · Visión integral
  Sistema contable como sistema integral del ente — L714.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · SISTEMA CONTABLE COMO SISTEMA DE INFORMACIÓN

  C1-E1 · E3 es subsistema contable, no sistema de información
          completo
    Resultado: parcial
    Cita: L560 "La contabilidad forma parte del sistema de
          información de una organización"
    Ubicación: global

  C1-E2 · E3 tiene estructura de SIC (Angrisani 6.0.03 ya detectó)
    Resultado: resiste
    Cita: L568 "aplicación práctica de la contabilidad"
    Ubicación: scfv_dsr/

C2 · CADA ENTE TIENE SU PROPIO SISTEMA CONTABLE

  C2-E1 · E3 asume un solo sistema contable universal (kernel fijo)
    Resultado: falla crítica
    Cita: L569-571 "cada ente tiene su propio sistema contable...
          similar al sistema contable de otras organizaciones,
          pero nunca igual"
    Ubicación: kernel/*.json

  C2-E2 · Fractales podrían parametrizar entes distintos
    Resultado: parcial
    Cita: L571
    Ubicación: fractales/*.scfv

C3 · PRESENTE Y FUTURO

  C3-E1 · E3 no maneja futuro · solo registra pasado
    Resultado: falla
    Cita: L588 "Del futuro, la contabilidad debe permitir
          formular planes de acciones"
    Ubicación: global

  C3-E2 · Reportes futuros (huérfanos) eran esa pieza
    Resultado: falla
    Cita: L588
    Ubicación: reportes_motor.py huérfano

C4 · IMPLEMENTACIÓN / REDISEÑO

  C4-E1 · E3 no tiene guía de implementación por ente
    Resultado: falla
    Cita: L700 "A la hora de implementar o rediseñar un
          sistema contable"
    Ubicación: global

  C4-E2 · Kernel parametrizable
    Resultado: parcial
    Cita: L714 "de información del ente"
    Ubicación: kernel/*.json

C5 · VISIÓN INTEGRAL

  C5-E1 · E3 cubre un slice de sistema contable integral
    Resultado: parcial
    Cita: L714
    Ubicación: global

  C5-E2 · No declara qué slices cubre
    Resultado: falla
    Cita: L714
    Ubicación: README.md

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Sistema de información   1        1       0       0
  C2 · Especificidad de ente    0        1       1       0
  C3 · Presente y futuro        0        0       2       0
  C4 · Implementación           0        1       1       0
  C5 · Visión integral          0        1       1       0
  ──────────────────────────────────────────────────────────────
  Total                         1        4       5       0

  Emergencias registradas: 10

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 como subsistema contable es coherente con Huck.

D · Divergencia
  Huck dice que cada ente tiene su propio sistema contable. E3
  tiene uno solo — el kernel es fijo. No hay declaración de
  "configuración por ente".

E · Emergencia
  E3 es un sistema contable universal, no parametrizable por ente.
  Huck diría que es una contradicción con la práctica. Pero también
  señala que los entes pueden ser "similares". El E3 asume
  "similares".

E · Enriquecimiento
  Huck aporta vocabulario: E3 no es "el" sistema contable — es
  "un" sistema contable (el del Programa SCFV).

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Huck 2024 × SCFV_DSR E3.
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
  Constancia: acta 6.0.09 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

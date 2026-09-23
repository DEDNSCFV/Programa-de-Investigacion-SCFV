PROGRAMA: Investigación SCFV
GIRO: 04
SESIÓN: 4
ACTO: [Observación — sin número formal asignado]
DOCUMENTO: GIRO_04/OBSERVACION_USEQ_01_GIRO_04_2026-09-23.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §19.3-bis
CARÁCTER: ejecución del §21 del pre-registro vE
NOTA DE NUMERACIÓN: sin número de acto. La cadena §10 no lo numera.
  La eventual asignación numérica queda pendiente de decisión del
  Operador en acto correctivo posterior.
FECHA: 2026-09-23

---

§1 · OBJETO

Declarar la ejecución de la observación evaluativa de U-SEQ-01 bajo
las condiciones pre-registradas en vE, conforme al §21.

§2 · CONDICIONES

- Pre-registro: vE (Fase C, materializado)
- k_inicial = k_evento = 1
- Fuente: ~/scfv_v6/scfv.db
- Alcance: event_store.id ∈ [1, 1]
- Sin modificación del pre-registro vE

§3 · EJECUCIÓN

Ejecutada por el Operador en Termux, 2026-09-23T11:06:59Z.
Soporte: Actos 21 y 22.

§4 · EVIDENCIA

Archivo: ~/SCFV_DSR/evaluacion/verificacion/
         observacion_useq_01_20260923T110658Z.json
SHA-256: 935ae9d331c0a63b83c2291c6ea33601efc3046d626fbbcb6b06e8d2d3709e20

Contenido (resumen):
- eventos_observados: [1]
- saldos_por_evento: {1: {110101: +1000.0, 410101: -1000.0}}
- consolidado_por_cuenta: {110101: +1000.0, 410101: -1000.0}
- suma_algebraica_global: 0.0
- partida_doble_ok: true
- hash_previo_evento_1: 0000…0000 (génesis)
- hash_actual_evento_1: 60cd7015f4d8a1086e8b673fb78fb47d78f759689250d3d35451e971f5624296
- version_contexto.V_MOTOR: 8.1

§5 · HALLAZGO

V_MOTOR=8.1 queda empíricamente verificado contra payload real.
Confirma la reconstrucción de O-164 (Acto 17 §3.2).
No modifica el corpus ni el pre-registro vE.

§6 · ALCANCE

Este acto no:
- cierra C-1 por sí mismo (falta falsación IA-2);
- cierra el Giro 04;
- modifica el pre-registro vE;
- extiende la observación más allá de id=1.

§7 · INTEGRIDAD

Régimen §19.3-bis.
Hash del JSON de evidencia: 935ae9d331c0a63b83c2291c6ea33601efc3046d626fbbcb6b06e8d2d3709e20
Registro: REGISTRO_OBSERVACION.log.


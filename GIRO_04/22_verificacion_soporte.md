PROGRAMA: Investigación SCFV
GIRO: 04
SESIÓN: 4
ACTO: 22
DOCUMENTO: GIRO_04/22_verificacion_soporte.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §19.3-bis
FECHA: 2026-09-23

---

§1 · OBJETO

Declarar la verificación del soporte mínimo construido en el Acto 21,
mediante tests ejecutados sobre ~/scfv_v6/scfv.db (10 eventos
ASIENTO_REGISTRADO).

§2 · TEST EJECUTADO

- verificacion/test_soporte_minimo.py
  SHA-256: ca44e9284bc25956a2437781a25ab4eaa8a40e344688c45d6e24b55d5f5c3293
- Resultado: 7/7 PASSED

Tests individuales:
1. lee 10 eventos
2. evento id=1 tiene 2 partidas
3. saldos id=1: {'110101': 1000.0, '410101': -1000.0}
4. partida doble en los 10 eventos
5. rechaza naturaleza desconocida
6. rechaza movimiento desconocido
7. descuadre detectado: 100.0

§3 · CONCLUSIÓN

El soporte funciona según las especificaciones del Acto 11 y las
precondiciones del pre-registro vE §6.d. Habilita la observación.

§4 · ALCANCE

Este acto no:
- ejecuta la observación;
- produce evidencia;
- modifica el pre-registro vE.

§5 · INTEGRIDAD

Régimen §19.3-bis. Hash del test incorporado en §2.


PROGRAMA: Investigación SCFV
GIRO: 04
SESIÓN: 4
ACTO: 21
DOCUMENTO: GIRO_04/21_soporte_minimo_construido.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §19.3-bis
CARÁCTER: materialización retrospectiva (ruta A, decisión del Operador)
FECHA: 2026-09-23

---

§1 · OBJETO

Declarar la construcción del soporte mínimo de evaluación de U-SEQ-01,
especificado en el Acto 11 y requerido como precondición técnica del
pre-registro vE §6.d.

§2 · ARTEFACTOS CONSTRUIDOS

Bajo ~/SCFV_DSR/evaluacion/:

- lectura/leer_eventos_asiento.py
  SHA-256: 120bdd69299d0dba36aeb5f7675eaa56c83edef509e8539a89a9cf5e3d27a395
- normalizacion/normalizar_partidas_para_saldos.py
  SHA-256: 23cac9191f516e8b4d807a0499ee3e1ccb20d05957e96d7f1f91ed37f2b12e8f

Funciones núcleo:
- leer_eventos_asiento(db_path) → eventos ASIENTO_REGISTRADO con payload parseado
- normalizar_partidas_para_saldos(evento) → {cuenta: saldo algebraico}

Convención: positivo = deudor, negativo = acreedor.
Asiento cuadrado → suma algebraica = 0.

§3 · TRAZABILIDAD

- Acto 11 (especificación del soporte)
- Pre-registro vE §6.d (precondición)
- Ejecución por el Operador en Termux
- Sin modificación de la DB ni del pre-registro vE

§4 · ALCANCE

Este acto no:
- ejecuta la observación;
- produce evidencia;
- cierra C-1;
- cierra el Giro 04;
- modifica el pre-registro vE.

§5 · INTEGRIDAD

Régimen §19.3-bis. Hashes de los dos archivos .py incorporados en §2.


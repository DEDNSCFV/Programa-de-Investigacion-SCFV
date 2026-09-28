════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE INVENTARIO FÍSICO
DOCUMENTO: ACTAS/ACTO_6_0_00_INVENTARIO.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-25
════════════════════════════════════════════════════════════════════════

§1 · OBJETO

Fijar el universo físico de unidades del artefacto SCFV_DSR E3
sobre el que operarán las 21 auditorías ciegas del ciclo 6.0.

────────────────────────────────────────────────────────────────────────

§2 · MÉTODO

Recorrido find sobre ~/SCFV_DSR/ excluyendo __pycache__, .pytest_cache,
var/, *.pyc. Listado ordenado alfabéticamente. Verificación de
integridad contra HASHES.txt mediante sha256sum -c.

────────────────────────────────────────────────────────────────────────

§3 · RESULTADO DEL RECORRIDO

Total archivos: 71
Integridad: 70 OK · 0 FAILED
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2

────────────────────────────────────────────────────────────────────────

§4 · CATEGORIZACIÓN

Categoría A · Kernel (6 unidades)
  4 JSON: operaciones · cuentas · categorias · puente
  baldor.py
  xnor.py

Categoría B · Contable defensivo (13 unidades)
  motor.py · nucleo_consecuencias.py · event_store.py
  puente_autorizacion.py · puente_consecuencias.py
  maquina_estados_asiento.py · verificador_autorizacion.py
  decision_provider.py · estados.py · modelos.py
  reportes_motor.py · examinador.py · reticulo.py

Categoría C · Traducción (5 unidades)
  evaluador.py · extractor.py · integrador.py · cli.py
  dsl/parser.py

Categoría D · Epistemológico (6 unidades)
  perceptum.py · evidencia.py · generador_propuesta.py
  models.py · dictum.py · intellectus.py

Categoría E · Profesional (2 unidades)
  h2.py · orquestador.py

Categoría F · Infraestructura (1 unidad)
  serializador_canonico.py

Categoría G · Fractales pipeline (10 unidades)
  ARRENDAMIENTOS · COMBINACIONES · HIPERINFLACION · INTANGIBLES
  INVENTARIOS · MONEDA · PPE · PROVISIONES · SUBVENCIONES · VENTAS

Categoría H · Ejemplos DSL (4 unidades)
  ejemplo_asiento · ejemplo_contrato · ejemplo_integrado
  ejemplo_invariante

Categoría I · Grammar (1 unidad)
  dsl/grammar.lark

Categoría J · Tests (6 unidades)
  test_asiento_declarado_def · test_compatibilidad_s0
  test_contract_def · test_grammar_lalr · test_invariant_def
  test_soporte_minimo (heredado)

Categoría K · Docs heredados (5 unidades)
  DOCS/historicos/evaluacion/lectura/leer_eventos_asiento.py
  DOCS/historicos/evaluacion/normalizacion/normalizar_partidas_para_saldos.py
  DOCS/historicos/evaluacion/verificacion/test_soporte_minimo.py
  DOCS/historicos/evaluacion/verificacion/REGISTRO_OBSERVACION.log
  DOCS/historicos/evaluacion/verificacion/observacion_useq_01_*.json

Categoría L · Config raíz (3 unidades)
  HASHES.txt · README.md · pyproject.toml

Categoría M · __init__.py (9 unidades)

────────────────────────────────────────────────────────────────────────

§5 · UNIDADES AUDITABLES

Runtime puro (A-F): 33 unidades
Fractales + ejemplos + grammar + tests (G-J): 21 unidades
Documentación heredada + config + inits (K-M): 17 unidades
Total auditables: 71

────────────────────────────────────────────────────────────────────────

§6 · LISTA COMPLETA

La lista íntegra de los 71 archivos con sus rutas relativas
respecto a ~/SCFV_DSR/ consta en el listado generado por el
comando de §2 y se conserva como evidencia adjunta al registro
de este acto.

────────────────────────────────────────────────────────────────────────

§7 · USO POR LAS AUDITORÍAS

Cada uno de los 21 auditores del ciclo 6.0 referencia este acto
por hash. El universo de unidades auditadas es el aquí declarado.
Un auditor puede declarar "no aplica" para unidades específicas,
pero no puede excluirlas del universo.

────────────────────────────────────────────────────────────────────────

§8 · FIRMA TRIPARTITA ASIMÉTRICA (§20)

OPERADOR · Autoridad ejecutora
  Firma: _______________________
  Fecha: 2026-09-25
  Decisión: fija el universo físico del E3 para el ciclo 6.0.

IA-1 · Constructor · constancia de interpretación arquitectónica
  Firma: _______________________
  Constancia: inventario verificado contra HASHES.txt y recuento
  por categoría conforme al listado de §2.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: _______________________
  Constancia: sin objeciones bloqueantes al inventario declarado.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

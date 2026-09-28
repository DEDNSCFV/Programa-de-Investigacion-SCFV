════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON FERNÁNDEZ OTERO & NAVARRO HUERGA 2014
DOCUMENTO: ACTAS/ACTO_6_0_06_AUDITORIA_DIAZ_NAVARRO.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autores reales: Marcos Fernández Otero · Miguel A. Navarro Huerga
Título: Sistemas de Gestión Integrada para las Empresas (ERP)
Universidad de Alcalá · 2014
Raw: ~/.diaz_navarro_raw.txt · 11.284 líneas
Naturaleza: canon de contraste para S0 · S0 ≠ ERP

Nota de trazabilidad: la carpeta conserva el nombre histórico
Diaz_Navarro_2014 por convención registrada. Los autores reales
fueron identificados el 2026-09-20 (HL-46 cerrado con nota).

Loci invocados:
  L56       · El sistema integrado de gestión de empresa
  L134      · implantación de un ERP
  L185-198  · módulos y agrupación funcional
  L208-224  · catálogo de módulos ERP
  L351-360  · módulos logísticos y financieros
  L381-385  · módulos financieros recubren la cadena logística
  L436-448  · integración de procesos a través del repositorio
  L672      · módulo Finanzas proporciona funcionalidades contables
  L944      · parametrización mediante guía de implantación

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Sistema integrado de gestión (ERP)
  Cuando se adquiere un ERP, la empresa constructora suministra
  el conjunto completo de módulos — L56, L134, L185-198.

C2 · Módulos ERP · agrupación funcional
  Módulos logísticos (comercial, almacenes, aprovisionamiento) ·
  módulos financieros (finanzas, controlling, activos) — L208-224,
  L351-360.

C3 · Integración de procesos a través del repositorio
  La integración se da entre módulos y su repositorio común
  — L436-448, L460-465.

C4 · ERP vs sistema de registro
  Los módulos financieros recubren la cadena logística —
  contabilidad de sociedad + analítica — L381-385, L568-569,
  L672.

C5 · Implantación / parametrización
  Enfoques de implantación y guía de parametrización — L63-65,
  L944.

C6 · Áreas funcionales cubiertas
  Áreas funcionales que cubre un ERP — L60, L198-224.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · SISTEMA INTEGRADO DE GESTIÓN

  C1-E1 · E3 no es un ERP · es motor de registro de consecuencias
    Resultado: no aplica por diseño
    Cita: L56 "El sistema integrado de gestión de empresa"
    Ubicación: global

  C1-E2 · E3 no declara explícitamente "no soy un ERP" en README
    Resultado: falla
    Cita: L134 "La implantación de un ERP en una empresa permite"
    Ubicación: README.md

C2 · MÓDULOS ERP · AGRUPACIÓN FUNCIONAL

  C2-E1 · E3 no tiene módulos funcionales (ventas, compras, etc.)
    Resultado: no aplica
    Cita: L208-224 "catálogo de módulos ERP"
    Ubicación: global

  C2-E2 · Los fractales emulan funcionalidad modular declarativa
    Resultado: parcial
    Cita: L351-360 "Módulos Logísticos / Módulos Financieros"
    Ubicación: fractales/*.scfv

C3 · INTEGRACIÓN A TRAVÉS DEL REPOSITORIO

  C3-E1 · E3 no integra procesos a través de un repositorio
    Resultado: no aplica
    Cita: L436-448 "integración de procesos a través del repositorio"
    Ubicación: global

  C3-E2 · E3 integra procesos vía DSL + pipeline
    Resultado: parcial
    Cita: L448 "módulos y su integración a través del repositorio"
    Ubicación: dsl/ + integrador.py

C4 · ERP VS SISTEMA DE REGISTRO

  C4-E1 · E3 es solo el módulo financiero-contable de un ERP
    Resultado: resiste
    Cita: L672 "El módulo Finanzas proporciona las
          funcionalidades contables"
    Ubicación: contable/

  C4-E2 · E3 no declara que solo cubre parte de un ERP
    Resultado: falla crítica
    Cita: L381-385 "los módulos financieros recubren la
          cadena logística"
    Ubicación: README.md

C5 · IMPLANTACIÓN / PARAMETRIZACIÓN

  C5-E1 · E3 no tiene guía de implantación
    Resultado: falla
    Cita: L944 "La parametrización se lleva a cabo mediante
          una guía de implantación"
    Ubicación: global

  C5-E2 · E3 sí tiene parametrización vía kernel JSON
    Resultado: parcial
    Cita: L944
    Ubicación: kernel/*.json

C6 · ÁREAS FUNCIONALES CUBIERTAS

  C6-E1 · E3 cubre área funcional contable pero no otras
    Resultado: parcial
    Cita: L60 "Áreas funcionales que cubre un ERP"
    Ubicación: global

  C6-E2 · E3 no declara qué áreas cubre y qué no
    Resultado: falla
    Cita: L198-224
    Ubicación: global

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Sistema integrado        0        0       1       1
  C2 · Módulos ERP              0        1       0       1
  C3 · Integración repositorio  0        1       0       1
  C4 · ERP vs registro          1        0       1       0
  C5 · Implantación             0        1       1       0
  C6 · Áreas funcionales        0        1       1       0
  ──────────────────────────────────────────────────────────────
  Total                         1        4       5       2

  Emergencias registradas: 12

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 sí es sistema integrado en su dominio contable, con módulos
  kernel, DSL y runtime. La parametrización vía kernel JSON cumple
  función análoga a la guía de implantación ERP.

D · Divergencia
  Fernández Otero describe ERP como sistema completo de empresa.
  E3 es pieza dentro de uno, no ERP. Falla en logística,
  aprovisionamiento, comercial, activos, controlling.

E · Emergencia
  E3 no declara su alcance frente al ERP. El README dice "artefacto
  Design Science Research" pero no dice "no es un ERP, es un motor
  contable". La FICHA de Fernández Otero lo tenía previsto
  (S0 ≠ ERP), pero esa declaración no llegó al README del artefacto.

E · Enriquecimiento
  Fernández Otero da vocabulario para preguntar: qué módulo de ERP
  sería E3 si estuviera integrado en uno. Respuesta: módulo
  financiero-contable con DSL propio para reglas. Es un ERP-slice.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Fernández Otero & Navarro Huerga 2014 × SCFV_DSR E3.
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
  Constancia: acta 6.0.06 redactada conforme al protocolo 6.0 §5,
  con emergencias ancladas a loci del raw y a ubicaciones del E3.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

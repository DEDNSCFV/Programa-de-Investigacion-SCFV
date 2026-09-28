════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON NIST FIPS 180-4
DOCUMENTO: ACTAS/ACTO_6_0_13_AUDITORIA_NIST.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: National Institute of Standards and Technology (NIST)
Obra: Federal Information Processing Standards Publication 180-4 — Secure Hash Standard (SHS) · 2014
Raw: ~/.nist_fips_180_4_raw.txt · 1.468 líneas · 50.079 bytes
SHA256 raw: 63ced11fcd7db55af1399cea3edb487fe6263cb6b9942a0bcf9d288f7ea78d29
Naturaleza: estándar federal de algoritmos de hash seguro

Loci invocados:
  L56-58    · especificación de algoritmos (SHA-1/224/256/384/512/512t)
  L62-63    · uso con firma digital y MAC
  L64-70    · infeasibilidad computacional / verificación fallida
  L88-91    · implementaciones validadas por NIST
  L104-106  · cláusula de limitación de garantía
  L155-186  · introducción + TOC §5-§7
  L210-260  · parámetros y símbolos (§2.2)
  L260-280  · tabla propiedades (fig.1)
  L28 errata 5/9/2014

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9
Superficie auditada: HASHES.txt · README.md · pyproject.toml · h2.py · event_store.py · evidencia.py · generador_propuesta.py · maquina_estados_asiento.py · orquestador.py · extractor.py · integrador.py · serializador_canonico.py

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Especificación de algoritmo
  El estándar especifica SHA-1/224/256/384/512/512t como
  funciones de hash iterativas unidireccionales — L56-58, L155-175.

C2 · Uso con firma digital o MAC
  El hash se usa con algoritmos de firma digital o MAC para
  detectar alteración mediante falla de verificación — L62-70.

C3 · Conformidad validada
  Solo implementaciones validadas por NIST se consideran
  conformes al estándar — L88-91.

C4 · Limitación de garantía
  La conformidad al estándar no asegura que una implementación
  particular sea segura — L104-106.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · ESPECIFICACIÓN DE ALGORITMO

  C1-E1 · Declaración de algoritmo
    Resultado: parcial
    Cita: L56-58 "This Standard specifies secure hash algorithms - SHA-1,
    SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224 and SHA-512/256 - for
    computing a condensed representation of electronic data (message)."
    Ubicación: README.md · pyproject.toml:8-11

  C1-E2 · Delegación a hashlib
    Resultado: resiste
    Cita: L88-89 "may be implemented in software, firmware, hardware or any
    combination thereof."
    Ubicación: h2.py:5 · evidencia.py:14 · event_store.py:22 ·
    maquina_estados_asiento.py:16 · motor.py:5 · generador_propuesta.py:14 ·
    orquestador.py:9 · integrador.py:15

  C1-E3 · Límites de tamaño de mensaje
    Resultado: parcial
    Cita: L58-60 "less than 264 bits (for SHA-1, SHA-224 and SHA-256)"
    Ubicación: extractor.py:30 · integrador.py:156

  C1-E4 · Serializador canónico
    Resultado: no aplica
    Cita: L26-28 (fuera del alcance §3 FIPS)
    Ubicación: serializador_canonico.py (grep sin coincidencias de hash)

  C1-E5 · Propiedades §A.1
    Resultado: falla
    Cita: L27-28 (TOC, "SECURITY OF THE SECURE HASH ALGORITHMS")
    Ubicación: README.md (ausencia de §seguridad)

C2 · USO CON FIRMA DIGITAL O MAC

  C2-E1 · firma_h2 no es firma
    Resultado: falla
    Cita: L68-70 "result in a verification failure when the secure hash
    algorithm is used with a digital signature algorithm or a keyed-hash
    message authentication algorithm"
    Ubicación: h2.py:23-35, 88, 105, 119

  C2-E2 · Ausencia de firma/MAC
    Resultado: falla
    Cita: L62-63 "used with other cryptographic algorithms, such as digital
    signature algorithms and keyed-hash message authentication codes"
    Ubicación: pyproject.toml:8-11 (solo lark) · grep global sin
    cryptography/pynacl/hmac

  C2-E3 · Verificación por recomputación
    Resultado: resiste
    Cita: L69 "verification failure" (mecanismo de detección)
    Ubicación: event_store.py:167-169 (emisión) · 270-272 (recomputación)

C3 · CONFORMIDAD VALIDADA

  C3-E1 · Validación NIST
    Resultado: parcial
    Cita: L89-91 "Only algorithm implementations that are validated by NIST
    will be considered as complying with this standard."
    Ubicación: README.md (ausencia)

C4 · LIMITACIÓN DE GARANTÍA

  C4-E1 · Cláusula de no-garantía
    Resultado: falla
    Cita: L104-106 "conformance to this Standard does not assure that a
    particular implementation is secure"
    Ubicación: README.md (ausencia)

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                             Resiste  Parcial  Falla  No aplica
  ────────────────────────────────────────────────────────────────────────
  C1 · Especificación de algoritmo       1        2       1       1
  C2 · Uso con firma digital / MAC       1        0       2       0
  C3 · Conformidad validada              0        1       0       0
  C4 · Limitación de garantía            0        0       1       0
  ────────────────────────────────────────────────────────────────────────
  Total                                  2        3       4       1

  Emergencias registradas: 10

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  E3 delega SHA-256 al módulo hashlib de la biblioteca estándar, sin
  reimplementar. Esto es conforme a L88-89 (implementable en software). La
  recomputación en event_store.py implementa el mecanismo de detección
  de falla declarado en L69.

D · Divergencia
  FIPS 180-4 declara que el hash se usa con algoritmos de firma digital
  o MAC. E3 usa hashlib.sha256 pero no importa ni declara ningún
  algoritmo de firma digital ni MAC. firma_h2 es SHA-256 determinista de
  cuatro campos concatenados, sin clave secreta. Es hash, no firma.

E · Emergencia
  E3 tiene algoritmo de hash y mecanismo de verificación por recomputación,
  pero no tiene firma digital ni MAC. Confirma H84 desde canon NIST y lo
  amplifica: la asimetría firma/autenticación queda explícitamente marcada
  por el estándar como "verification failure" si falta la segunda capa.

E · Enriquecimiento
  NIST aporta tres cláusulas que el artefacto no declara: conformidad
  validada (C3), limitación de garantía (C4) y límites de tamaño de
  mensaje (C1-E3). FIPS 180-4 no es solo una especificación algorítmica:
  es un régimen declarativo que E3 no replica en su documentación.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
NIST FIPS 180-4 × SCFV_DSR E3.
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
  Constancia: acta 6.0.13 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

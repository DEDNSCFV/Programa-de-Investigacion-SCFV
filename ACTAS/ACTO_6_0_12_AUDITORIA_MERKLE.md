════════════════════════════════════════════════════════════════════════
PROGRAMA: Investigación SCFV
GIRO: 06
SECCIÓN: 0 · AUDITORÍA
TIPO: ACTO DE AUDITORÍA · CANON MERKLE 1979
DOCUMENTO: ACTAS/ACTO_6_0_12_AUDITORIA_MERKLE.md
ESTATUTO: MATERIALIZADO
RÉGIMEN: §20
FIRMA: tripartita asimétrica
FECHA: 2026-09-26
════════════════════════════════════════════════════════════════════════

§1 · CANON INVOCADO

Autor: Ralph C. Merkle
Obra: A Certified Digital Signature (1979)
Raw: ~/.merkle_1979_raw.txt · 4.725 líneas
Naturaleza: cadena de hash · firma digital certificada

Loci invocados:
  L10-11    · hashsig · implementación
  L34       · tree signatures
  L48       · A practical digital signature system based
  L126      · Digital signatures promise to
  L185-197  · signature system · kilobytes de memoria

────────────────────────────────────────────────────────────────────────

§2 · OBJETO AUDITADO

Artefacto: SCFV_DSR E3
Hash maestro: 5833327c94de5d97a4de14eca52be4cb8f1ba758cf9d8329425684bb03cbf1e2
Inventario: ACTO 6.0.00 · hash 045f3073ea6843400dcff3bfb580b91c60cdd3018467e888fd3dd6d9425c55a9

────────────────────────────────────────────────────────────────────────

§3 · CRITERIOS DEL AUTOR

C1 · Cadena de hash · estructura de árbol
  Merkle propone sistemas de firmas basados en árboles de
  hash — L34, L152-185.

C2 · Firma digital certificada
  La firma digital autentica con clave secreta — L48, L126.

C3 · Función unidireccional (hash)
  La seguridad se basa en funciones unidireccionales — implícito
  en todo el paper.

C4 · Autenticación verificable
  El receptor verifica con pocos kilobytes de memoria — L197.

────────────────────────────────────────────────────────────────────────

§4 · EMERGENCIAS DETECTADAS

C1 · CADENA DE HASH

  C1-E1 · EventStore tiene cadena de hash verificable
    Resultado: resiste
    Cita: L34 "tree signatures"
    Ubicación: event_store.py

  C1-E2 · E3 no tiene estructura de árbol Merkle
    Resultado: no aplica
    Cita: L34
    Ubicación: global

  C1-E3 · La cadena es lineal, no árbol
    Resultado: parcial
    Cita: L152-185 "signature system"
    Ubicación: event_store.py

C2 · FIRMA DIGITAL CERTIFICADA

  C2-E1 · DecisionProfesional tiene firma_h2 · no es firma digital
    Resultado: falla crítica
    Cita: L48 "practical digital signature system"
    Ubicación: h2.py

  C2-E2 · La firma_h2 es SHA-256 de 4 campos · no criptográfica
    Resultado: parcial
    Cita: L126 "Digital signatures promise to"
    Ubicación: h2.py

C3 · FUNCIÓN UNIDIRECCIONAL

  C3-E1 · SHA-256 es función unidireccional correcta
    Resultado: resiste
    Cita: L10-11 "hashsig"
    Ubicación: event_store.py

C4 · AUTENTICACIÓN VERIFICABLE

  C4-E1 · Autenticación mediante verificar_cadena
    Resultado: resiste
    Cita: L197 "signature, and only a few kilobytes of memory"
    Ubicación: event_store.py

────────────────────────────────────────────────────────────────────────

§5 · RESUMEN DE EMERGENCIAS

  Criterio                    Resiste  Parcial  Falla  No aplica
  ──────────────────────────────────────────────────────────────
  C1 · Cadena de hash           1        1       0       1
  C2 · Firma digital            0        1       1       0
  C3 · Función unidireccional   1        0       0       0
  C4 · Autenticación            1        0       0       0
  ──────────────────────────────────────────────────────────────
  Total                         3        2       1       1

  Emergencias registradas: 7

────────────────────────────────────────────────────────────────────────

§6 · CDEE DEL PROPIO AUTOR

C · Convergencia
  La cadena hash del EventStore es sólida. La verificación
  recalcula cada hash. La función unidireccional es correcta.

D · Divergencia
  Merkle describe firmas digitales con clave privada y verificación
  criptográfica. E3 tiene firma_h2 que es SHA-256 determinista de
  campos, sin clave secreta. Es hash, no firma.

E · Emergencia
  E3 tiene cadena de hash, no firma digital. Confirma H84 desde un
  tercer canon. La cadena preserva integridad. La firma no
  autentica. Son dos propiedades distintas.

E · Enriquecimiento
  Merkle da vocabulario: certified digital signature no es hash of
  fields. El E3 confunde ambos términos en h2.py. La firma es
  determinista pero no autenticada.

────────────────────────────────────────────────────────────────────────

§7 · CONSTANCIA DE NO OPINIÓN

Este acto registra emergencias del cruce
Merkle 1979 × SCFV_DSR E3.
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
  Constancia: acta 6.0.12 redactada conforme al protocolo 6.0 §5.

IA-2 · Falsador · constancia de no objeción pendiente
  Firma: IA-2 · Falsador
  Constancia: sin objeciones bloqueantes al acta emitida.

────────────────────────────────────────────────────────────────────────

§9 · REGISTRO

Registro en GIRO_05/REGISTRO_ACTOS.log.

════════════════════════════════════════════════════════════════════════

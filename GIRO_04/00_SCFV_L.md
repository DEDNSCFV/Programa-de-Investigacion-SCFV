# SCFV-L

**GIRO_04 · PROGRAMA_DE_INVESTIGACION_SCFV**

**Documento:** Propuesta de unificación documental y semántica del vocabulario del Programa
**Versión:** Consolidada para decisión del Operador
**Naturaleza:** Investigación documental y semántica interna
**Función:** Unificación progresiva del vocabulario distribuido del Programa
**Relación con `01_idea.md`:** Paralela e independiente
**Materialización:** Pendiente de autorización del Operador

---

## §1. PROPÓSITO

"SCFV-L" constituye la propuesta de una capa documental y semántica mediante la cual el Programa de Investigación SCFV pueda organizar, relacionar y consultar progresivamente su vocabulario distribuido, preservando la procedencia, el contexto y la historia de cada término.

La operación central propuesta es:

> «RELACIONAR»

y no:

> «ABSORBER.»

SCFV-L no sustituye las fuentes originales del Programa ni elimina su diversidad histórica.

---

## §2. PROBLEMA

El vocabulario del Programa se encuentra distribuido en múltiples clases de fuentes:

1. `glossary.md`;
2. Protocolo;
3. Actas;
4. Estado del Arte Interno;
5. documentos metodológicos;
6. documentos arquitectónicos;
7. documentos ontológicos o conceptuales;
8. NPL y DSL;
9. código;
10. tests;
11. decisiones documentadas;
12. críticas internas y externas.

Esta distribución puede producir:

- duplicación terminológica;
- términos con usos diferentes;
- cambios históricos de significado;
- relaciones no explicitadas;
- dificultad para localizar la procedencia de una definición;
- divergencias entre lenguaje conceptual, documental y técnico.

SCFV-L se propone como respuesta documental a esa dispersión, sin presuponer que todas las diferencias puedan o deban eliminarse.

---

## §3. IDEA

La formulación central es:

> «SCFV-L será una capa documental y semántica mediante la cual el Programa pueda relacionar su vocabulario distribuido sin eliminar la procedencia, el contexto ni la historia de cada término.»

La propuesta no declara que todos los términos puedan ser unificados ni que exista actualmente un vocabulario canónico completo.

---

## §4. DESTINATARIOS

SCFV-L está concebido para facilitar el trabajo de:

- Operador;
- investigadores;
- críticos;
- académicos;
- desarrolladores;
- futuros colaboradores;
- lectores del Programa.

La función es documental y cognitiva antes que ejecutiva.

---

## §5. FUENTES Y ESTATUTO DOCUMENTAL

### §5.1. Fuentes primarias

Una fuente se considera primaria respecto de aquello que originalmente produce, define, establece, ejecuta o documenta.

Pueden actuar como fuentes primarias:

- `glossary.md`, respecto de las definiciones que originalmente establece;
- el Protocolo, respecto de sus reglas y categorías;
- las Actas, respecto del contenido producido en el acto documental correspondiente;
- decisiones documentadas, respecto de la decisión originalmente registrada;
- documentos metodológicos, arquitectónicos, ontológicos o conceptuales, cuando constituyen la fuente original de sus formulaciones;
- NPL y DSL, respecto de los términos y construcciones que originalmente establecen como lenguaje;
- tests, respecto de las propiedades o comportamientos que expresamente especifican o verifican;
- código, solo respecto de elementos cuya función semántica o contractual sea documentable para el Programa;
- soporte original de una crítica, respecto de la crítica efectivamente formulada.

El hecho de que un elemento pertenezca a una de estas categorías no convierte automáticamente todo su contenido en vocabulario SCFV-L.

### §5.1.1. Alcance del código como fuente

El código puede constituir fuente primaria para SCFV-L cuando contiene elementos con función semántica o contractual explícita, tales como:

- modelos o tipos de dominio;
- invariantes;
- propiedades de dominio;
- errores de dominio;
- operaciones de dominio;
- interfaces públicas con significado contractual;
- construcciones NPL/DSL cuando expresan conceptos del dominio.

No ingresan automáticamente al vocabulario SCFV-L:

- variables internas;
- nombres locales;
- identificadores accidentales;
- detalles puramente técnicos de implementación;
- comentarios auxiliares sin función conceptual o contractual.

La presencia de un término en código no constituye por sí sola evidencia de que sea un término del vocabulario del Programa.

### §5.1.2. Soporte original y soporte documentado de las críticas

Se distingue:

- **Soporte original:** mensaje, documento o registro en el que la crítica fue efectivamente producida.
- **Soporte documentado:** acta u otro documento posterior que registra, transcribe, analiza o conserva esa crítica dentro del corpus del Programa.

Cuando ambos existen, el soporte original conserva prioridad como fuente de la formulación, mientras que el soporte documentado conserva la trazabilidad de su recepción y tratamiento dentro del Programa.

En el caso de una crítica externa, como la de Héctor Calderón, el mensaje o documento original constituye el soporte primario de la crítica; el acta interna correspondiente constituye soporte documental derivado de su recepción y tratamiento.

### §5.2. Fuentes sintéticas

Son fuentes sintéticas aquellas que reúnen, condensan o reorganizan información proveniente de otras fuentes.

Ejemplo principal:

- Estado del Arte Interno.

También pueden ser sintéticas documentos metodológicos, arquitectónicos, ontológicos, conceptuales u otros cuando su función concreta sea integrar material procedente de fuentes anteriores.

Por tanto, el estatuto documental se determina por la función de producción de la fuente y no únicamente por su nombre o categoría.

Una fuente sintética debe conservar referencias hacia las fuentes que la sustentan cuando estas sean necesarias para recuperar la procedencia.

### §5.3. Fuentes derivadas

Son fuentes derivadas las representaciones producidas a partir de otras fuentes, por ejemplo:

- índices;
- tablas de correspondencia;
- representaciones;
- relaciones;
- normalizaciones;
- mapas semánticos;
- agrupaciones;
- consultas o vistas generadas;
- mappings documentales.

Una fuente derivada no sustituye a la fuente de origen.

### §5.4. Trazabilidad

La cadena documental propuesta es:

> «SCFV-L → fuente sintética/derivada → fuente relevante de origen»

Cuando sea necesario, deberá poder reconstruirse:

> «término → definición → fuente → contexto → relación → evolución»

La trazabilidad constituye una propiedad documental deseada del sistema, no una propiedad actualmente demostrada de una implementación inexistente.

---

## §6. VOCABULARIO TIPADO Y ESTRUCTURAS CONCEPTUALES

SCFV-L puede registrar:

- términos;
- definiciones;
- diferencias semánticas;
- relaciones;
- categorías;
- correspondencias;
- usos contextuales;
- estructuras conceptuales;
- referencias entre vocabularios.

Esto no presupone la existencia de una ontología formal independiente ya establecida.

La formalización ontológica, si posteriormente resulta necesaria, constituye una cuestión de investigación distinta.

---

## §7. UNIDAD DOCUMENTAL PROVISIONAL

Como estructura inicial, una entrada SCFV-L puede contener:

- TERM
- DEFINITION
- NOT_CONFUSE_WITH
- SOURCE
- CONTEXT
- RELATIONS
- DOCUMENTARY_STATUS
- HISTORY
- REFERENCES

Esta estructura es provisional y puede modificarse durante el desarrollo del Programa.

---

## §8. CADENA DE PROCEDENCIA

Para cada término que ingrese al sistema documental se propone conservar:

> «TÉRMINO → DEFINICIÓN → FUENTE → CONTEXTO → RELACIONES → EVOLUCIÓN»

La cadena permite distinguir:

- dónde apareció el término;
- qué significaba en ese contexto;
- cómo fue utilizado posteriormente;
- qué relaciones se establecieron;
- qué modificaciones experimentó.

La evolución histórica no se considera ruido que deba eliminarse.

---

## §9. OPERACIONES DE UNIFICACIÓN

SCFV-L puede desarrollar progresivamente las siguientes operaciones:

1. identificar términos;
2. extraer usos;
3. normalizar formas cuando corresponda;
4. definir términos;
5. diferenciar términos próximos;
6. enlazar fuentes;
7. relacionar conceptos;
8. conservar la historia;
9. registrar correspondencias;
10. permitir consultas cruzadas.

Estas operaciones no implican que toda diferencia terminológica deba resolverse mediante una única denominación.

---

## §10. RELACIÓN CON `glossary.md`

`glossary.md` conserva su carácter de fuente especializada del vocabulario contable.

SCFV-L:

- no lo reemplaza;
- no lo absorbe;
- no elimina su estructura;
- no altera su genealogía.

SCFV-L funciona como capa de relación y consulta sobre las fuentes que conforman el vocabulario del Programa.

---

## §11. ESTADOS DOCUMENTALES

Se proponen provisionalmente tres estados:

**CANON.** Término cuya identidad, definición o uso ha sido establecido documentalmente dentro del Programa con suficiente estabilidad y procedencia para ser tratado como referencia interna.

**EMERGENT.** Término que surge o se encuentra actualmente en proceso de estabilización dentro del Programa.

**NO_DETERMINADO.** Término cuyo estatuto, significado o relación no cuenta todavía con base documental suficiente para establecerlo.

Estos estados son estados documentales, no estados de verdad epistemológica.

El criterio completo para declarar un término CANON no se establece en este documento.

---

## §12. SCFV-L Y CANON

SCFV-L no se declara equivalente al CANON.

La propuesta actual es:

> «SCFV-L constituye el sistema documental propuesto para organizar, relacionar y consultar el vocabulario del Programa.»

El CANON puede constituir posteriormente un estado o subconjunto documental dentro de ese sistema, si el Programa establece mecanismos suficientes para determinarlo.

La cuestión del criterio formal para declarar CANON queda abierta como cuestión de diseño de SCFV-L. Su estatuto dentro del Programa no se declara en este documento.

---

## §13. IDENTIFICADORES HISTÓRICOS

Los identificadores `HL-XXX` conservan su carácter de genealogía documental.

SCFV-L no los reemplaza ni los renumera.

Cuando resulte útil, podrá presentarse:

> «TRAYECTORIA_ESTADO [HL-XXX]»

de modo que el nombre semántico facilite la consulta mientras el identificador histórico conserva la trazabilidad.

El identificador histórico permanece inmutable.

---

## §14. PRINCIPIO DE NO-BORRADO

La unificación documental no debe borrar la historia terminológica.

Para cada modificación relevante deberá poder conservarse, cuando exista:

- qué se modificó;
- dónde;
- cuándo;
- por qué;
- qué relación tiene con formulaciones anteriores;
- qué fuente respalda el cambio.

SCFV-L busca unificar la consulta sin destruir la genealogía.

---

## §15. CAPA SEMÁNTICA PROPUESTA

Como hipótesis de trabajo documental se propone la siguiente relación:

> «CONCEPTO → SCFV-L → NPL/DSL → PYTHON → ARQUITECTURA → TESTS → EVIDENCIA»

Esta cadena representa una posible infraestructura de continuidad semántica.

No constituye todavía una correspondencia demostrada entre todos sus niveles.

Su validación pertenece a fases posteriores del Programa.

---

## §16. POSIBLE EVOLUCIÓN HACIA LENGUAJE DE DOMINIO

SCFV-L podría, eventualmente, servir como base documental para una evolución hacia un lenguaje de dominio más formal.

Esto no significa que SCFV-L sea actualmente:

- una DSL ejecutable;
- un compilador;
- un parser;
- un lenguaje de programación;
- una especificación formal completa.

La posible evolución hacia esos objetos queda abierta a investigación posterior.

---

## §17. CONTRIBUCIONES DISCIPLINARES POTENCIALES

La construcción de SCFV-L puede recibir aportes de diferentes campos:

- terminología;
- documentación;
- organización de la información;
- filología y transmisión textual;
- ontología y gestión del conocimiento;
- epistemología;
- contabilidad;
- informática;
- diseño de lenguajes específicos de dominio.

La contribución de cada campo deberá delimitarse según el problema concreto.

Ninguna disciplina queda declarada como autoridad exclusiva sobre SCFV-L.

---

## §18. ALCANCE DEL GIRO 04

En este Giro se propone:

1. identificar la dispersión terminológica;
2. identificar las clases de fuentes;
3. distinguir su función documental;
4. preservar procedencia;
5. registrar estados documentales;
6. establecer una estructura provisional;
7. conservar la genealogía `HL-XXX`;
8. definir la relación con `glossary.md`;
9. explorar relaciones entre vocabulario conceptual, documental y técnico;
10. preparar una futura unificación progresiva.

El Giro 04 no pretende completar SCFV-L.

---

## §19. LO QUE ESTE DOCUMENTO NO DECLARA

Este documento no declara:

- un diccionario completo del Programa;
- que todo el vocabulario esté unificado;
- que todas las definiciones sean compatibles;
- que exista un CANON completo;
- que SCFV-L sea el CANON;
- que el criterio para CANON esté resuelto;
- una ontología formal independiente ya establecida;
- una DSL ejecutable;
- correspondencia completa NPL ↔ DSL ↔ Python;
- una estructura definitiva de SCFV-L;
- que todo identificador del código pertenezca al vocabulario del Programa;
- que toda crítica documentada tenga el mismo estatuto que su fuente original.

---

## §20. ESTATUTO DEL DOCUMENTO

`00_SCFV_L.md` constituye un:

> «documento paralelo de investigación documental y semántica del Giro 04.»

No constituye:

- una aporía;
- una resolución definitiva del CANON;
- una implementación;
- una especificación ejecutable;
- un diccionario final.

Su función actual es establecer las bases para una unificación progresiva y trazable del vocabulario del Programa.

---

## §21. FALSACIÓN SOLICITADA

SCFV-L deberá ser sometido posteriormente a contraste respecto de:

1. suficiencia de la estructura documental propuesta;
2. coherencia entre fuentes y estatutos documentales;
3. utilidad real de la distinción CANON / EMERGENT / NO_DETERMINADO;
4. preservación efectiva de la procedencia;
5. tratamiento correcto de cambios históricos;
6. delimitación entre vocabulario conceptual y léxico accidental del código;
7. delimitación entre soporte original y soporte documentado;
8. utilidad de la capa SCFV-L frente a la dispersión existente;
9. coherencia con el Protocolo y el corpus del Programa;
10. relación futura con NPL/DSL;
11. riesgo de convertir la capa documental en una ontología prematuramente cerrada.

La propuesta podrá ser modificada, ampliada o abandonada en función de los resultados de su contraste.

---

## §22. RELACIÓN CON `01_idea.md`

`00_SCFV_L.md` y `01_idea.md` son objetos paralelos del Giro 04.

`01_idea.md` desarrolla una línea de investigación sobre:

> «TRAYECTORIA_ESTADO y EVALUACION_TRAYECTORIA.»

`00_SCFV_L.md` desarrolla una línea de investigación sobre:

> «unificación documental y semántica del vocabulario del Programa.»

Pueden relacionarse posteriormente mediante términos, referencias y trazabilidad, pero ninguno constituye fundamento lógico exclusivo del otro.

---

## §23. CONSTANCIA DE VERIFICACIÓN IA-2

| Elemento | Estado |
|---|---|
| HL-617 (clasificación de las 12 categorías de fuentes) | INTEGRADA |
| HL-618 (delimitación del código como fuente) | INTEGRADA |
| HL-619 (soporte original vs soporte documentado) | INTEGRADA |
| Objeciones sustantivas vivas | CERO |
| Observaciones cosméticas | HL-622, HL-623, HL-624 (no bloqueantes) |
| Ciclo §19.2 | CERRADO |
| Estatuto | APTO PARA MATERIALIZACIÓN |

Constancia emitida por IA-2.

---

## §24. DECISIÓN DEL OPERADOR

El documento queda preparado para la decisión del Operador.

Corresponde exclusivamente al Operador decidir:

- materializar `00_SCFV_L.md`;
- modificarlo;
- posponerlo;
- incorporarlo al corpus del Giro 04.

---

**Fin del documento.**

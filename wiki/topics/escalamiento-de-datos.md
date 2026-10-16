---
title: Escalamiento de datos
aliases:
- Replicación
- Sharding
- Particionamiento
- Localidad
- Primario-secundario
- Primario-primario
sources:
- EXT-001
- EXT-020
related:
- bases-de-datos-relacionales
- bases-de-datos-no-relacionales
- atributos-de-calidad
prerequisites:
- persistencia
---

# Escalamiento de datos

## Panorama

Los apuntes distinguen aumentar recursos de una instancia —escalamiento vertical— de distribuir trabajo entre varias —horizontal—. Para datos, desarrollan replicación, particionamiento e indexación según el patrón de acceso. Esta cobertura procede de material externo. [EXT-001, «Escalamiento de Bases Relacionales» y «Caso Twitter»]

## Replicación

En **primario-secundario**, el primario recibe escrituras y propaga cambios a réplicas que atienden lecturas. Los apuntes describen reemplazar al primario ante una falla mediante elección de un secundario. En **primario-primario**, varios nodos aceptan lecturas y escrituras, con mayores exigencias de coordinación y resolución de concurrencia. [EXT-001, «Escalamiento de Bases Relacionales»]

El objetivo de escalar lecturas o escrituras no es intercambiable: hay que identificar qué operaciones saturan al sistema. La sincronización entre nodos también introduce costos que limitan el crecimiento útil del conjunto. [EXT-001, «Escalamiento de Bases Relacionales»]

## Particionamiento y localidad

El sharding distribuye conjuntos disjuntos de datos entre particiones con el mismo esquema; cada partición puede tener réplicas. La aplicación o infraestructura debe localizar el dato y resolver las operaciones que atraviesan particiones. Los apuntes destacan guardar juntos los datos que se consultan juntos: **principio de localidad**. [EXT-001, «Alternativas de Bases Relacionales»]

## Ejemplo de enseñanza

El relato de Twitter de los apuntes muestra por qué una partición adecuada para consultar por ID puede no servir para consultar por autor. El particionamiento temporal favorece búsquedas recientes, pero concentra actividad en la partición nueva y puede encarecer consultas históricas. Es un caso histórico relatado por la fuente, sin atribuirlo al funcionamiento actual de la plataforma. [EXT-001, «Tweets» y «Búsquedas»]

## Relaciones

La selección combina [atributos de calidad](atributos-de-calidad.md), volumen, estructura y patrones de acceso. Las fuentes externas incluyen explicaciones simplificadas de CAP y de motores particulares; estas páginas no las convierten en una especificación de garantías de productos. [EXT-001, «Bases No Relacionales»; EXT-020, «Bucket de Soluciones»]

## Fuentes

- [EXT-001, «Escalamiento de Bases Relacionales», «Alternativas de Bases Relacionales», «Bases No Relacionales», «Tweets» y «Búsquedas»]
- [EXT-020, «Bucket de Soluciones»]

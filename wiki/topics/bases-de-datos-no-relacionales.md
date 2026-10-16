---
title: Bases de datos no relacionales
aliases:
- NoSQL
- Clave-valor
- Documentos
- Bases columnares
- Bases vectoriales
- Embeddings
sources:
- OFF-016
- EXT-001
- EXT-020
- OFF-017
related:
- persistencia
- escalamiento-de-datos
- bases-de-datos-relacionales
prerequisites:
- persistencia
---

# Bases de datos no relacionales

## Panorama

La clase presenta bases no relacionales como alternativas que abordan escalabilidad, distribución, volumen y flexibilidad de esquema. Explicita que pueden implementar o no propiedades ACID: la categoría no fija una única garantía transaccional. [OFF-016, p. 14]

## Familias

| Familia | Organización y uso en el material |
| --- | --- |
| Columnas | Agrupa información por columnas; facilita proyecciones sobre pocas columnas. La clase incluye BigTable, Hypertable y Cassandra entre sus ejemplos. |
| Clave-valor | Pares de clave y valor, con acceso directo por clave y dificultades para búsquedas combinadas por varios atributos. Se ejemplifica con Redis y Dynamo. |
| Documentos | Guarda estructuras variables; los ejemplos utilizan documentos con campos y referencias. La clase menciona MongoDB y CouchDB. |
| Vectoriales | Guarda vectores multidimensionales y metadatos, y consulta por similitud en lugar de coincidencia exacta. |

[OFF-016, pp. 15-22]

## Búsqueda vectorial

Un modelo transforma texto, imagen u otro dato en un embedding. La base almacena esos vectores y, ante una consulta, calcula similitudes o distancias para recuperar elementos cercanos. La clase los relaciona con búsqueda semántica, recomendación e IA generativa, y los presenta como complemento de bases relacionales. [OFF-016, pp. 21-22, 25]

## Límites del material

Las tablas resumen recomendaciones por familia; deben leerse junto con la aclaración de que las garantías varían. El cheatsheet externo etiqueta motores completos como CA, AP o CP y realiza afirmaciones absolutas sobre transaccionalidad; la clase no establece una garantía idéntica para toda una familia NoSQL. No se derivan capacidades concretas de un motor sólo desde esas etiquetas. [EXT-020, «Bucket de Soluciones»; OFF-016, pp. 14, 24-25]

La clase reúne bajo «columnas» almacenamiento por columna, ejemplos de familias de columnas y usos analíticos. El material incorporado no desarrolla sistemáticamente sus diferencias internas; esta página conserva esa clasificación docente sin convertir todas sus recomendaciones en equivalencias entre motores. [OFF-016, pp. 15-16, 24]

## Relaciones y evaluación

La elección depende de los patrones de consulta y las necesidades de [persistencia](persistencia.md) y [escalamiento](escalamiento-de-datos.md). El repaso incluye columnas, clave-valor y documentos; no explicita bases vectoriales. [OFF-017, p. 10]

## Fuentes

- [OFF-016, pp. 14-25]
- [EXT-020, «Bucket de Soluciones»]
- [OFF-017, p. 10]

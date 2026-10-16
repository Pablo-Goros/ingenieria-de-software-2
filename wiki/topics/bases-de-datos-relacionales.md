---
title: Bases de datos relacionales y analíticas
aliases:
- RDBMS
- OLTP
- OLAP
- ORM
- ACID
- Impedancia objeto-relacional
sources:
- OFF-016
- EXT-001
- OFF-017
related:
- persistencia
- bases-de-datos-no-relacionales
- escalamiento-de-datos
prerequisites:
- persistencia
---

# Bases de datos relacionales y analíticas

## Panorama

Una base relacional organiza datos en tablas de filas y columnas, con claves y restricciones, sobre fundamentos de álgebra relacional y conjuntos. La clase señala la normalización como parte del trabajo con este modelo. [OFF-016, p. 10]

## Transacciones y análisis

Los apuntes distinguen **OLTP**, orientado a operar sobre datos transaccionales, de **OLAP**, orientado a análisis y reportes. La clase describe bases multidimensionales con grandes volúmenes históricos, desnormalización y agregaciones precalculadas; el ejemplo de data warehouse extrae datos transaccionales, los transforma y agrega, y los almacena para lectura analítica. [EXT-001, «Bases de Datos»; OFF-016, pp. 11, 23-24]

La explicación de ACID de la clase distingue atomicidad —transacción indivisible—, consistencia —preservación de reglas de validez—, aislamiento —ejecución concurrente con separación— y durabilidad —permanencia tras commit incluso ante fallas—. El ejemplo de atomicidad exige completar ambas partes de una transferencia. [OFF-016, p. 14]

## Objetos, tablas y ORM

Un ORM mapea objetos del software a tablas y automatiza operaciones como CRUD. La clase destaca facilidad de programación con costos de rendimiento y complejidad. Las bases de objetos, en cambio, almacenan estructuras y relaciones del paradigma orientado a objetos sin realizar ese mapeo a tablas. [OFF-016, pp. 12-13]

Los apuntes llaman **impedancia objeto-relacional** a la fricción entre ambos modelos: herencia, identidad, referencias y comportamiento no coinciden directamente con tablas, claves y relaciones. [EXT-001, «Bases de Datos»]

## Alcance de las generalizaciones

Los apuntes presentan OLAP como append-only y siempre alimentado desde OLTP. La diapositiva oficial describe ese flujo como un caso típico de DWH, sin establecerlo como definición universal de toda solución analítica. Se conserva el alcance ejemplificador de la clase. [EXT-001, «Bases de Datos»; OFF-016, p. 11]

## Relaciones y evaluación

La [replicación y el particionamiento](escalamiento-de-datos.md) abordan crecimiento y disponibilidad. El repaso incluye relacionales, multidimensionales y bases de objetos. [OFF-017, p. 10]

## Fuentes

- [OFF-016, pp. 10-14, 23-24]
- [EXT-001, «Bases de Datos»]
- [OFF-017, p. 10]

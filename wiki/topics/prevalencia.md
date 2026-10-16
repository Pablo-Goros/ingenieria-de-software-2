---
title: Prevalencia
aliases:
- Object prevalence
- Snapshots
- Command log
sources:
- OFF-016
- EXT-001
- EXT-020
- OFF-017
related:
- persistencia
- bases-de-datos-relacionales
prerequisites:
- persistencia
---

# Prevalencia

## Panorama

En prevalencia, el estado se mantiene en memoria en su formato nativo. Se registran las transacciones y se realizan snapshots a disco para persistirlo. La clase menciona Prevayler, Madeleine y Bamboo como implementaciones. [OFF-016, p. 7]

## Funcionamiento y compromisos

El esquema docente muestra un dominio de objetos en RAM, un log de comandos y un snapshotter que guarda periódicamente el estado completo. Los snapshots pueden ser serializaciones binarias del estado interno. El beneficio es evitar transformar continuamente los objetos a otra representación, con transparencia y buen rendimiento; el conjunto de datos debe caber en memoria y la interoperabilidad es una limitación. [OFF-016, pp. 7-8]

El resumen de la clase lo asocia con aplicaciones de baja latencia y datos complejos, y desaconseja el esquema cuando el estado excede la memoria o se requieren consultas ad hoc y alta concurrencia. Estas son orientaciones del material sobre la técnica presentada. [OFF-016, p. 23]

## Diferencia entre fuentes

Los apuntes y el cheatsheet externos describen un snapshot de todo el estado ante cada cambio. Las diapositivas distinguen el registro de transacciones de los snapshots periódicos; no se equipara cada mutación con la escritura completa del estado. Se conserva esta distinción de la fuente oficial. [EXT-001, «Prevalencia»; EXT-020, «Bucket de Soluciones»; OFF-016, pp. 7, 23]

La clase también aclara que Redis comparte un principio arquitectónico, pero persiste estructuras clave-valor; no lo identifica sin más con prevalencia pura de objetos. [OFF-016, p. 7]

## Relaciones y evaluación

Es una alternativa de [persistencia](persistencia.md), diferente de mapear objetos a tablas. El repaso incluye explícitamente prevalencia. [OFF-017, p. 10]

## Fuentes

- [OFF-016, pp. 7-8, 23]
- [EXT-001, «Prevalencia»]
- [EXT-020, «Bucket de Soluciones»]
- [OFF-017, p. 10]

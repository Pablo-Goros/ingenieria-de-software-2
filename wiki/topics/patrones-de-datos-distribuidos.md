---
title: Patrones de datos distribuidos
aliases:
- Two-phase commit
- 2PC
- Sagas
- CQRS
- Event sourcing
- Aggregates
sources:
- EXT-001
- OFF-018
related:
- microservicios
- procesamiento-de-eventos
- persistencia
prerequisites:
- microservicios
- persistencia
---

# Patrones de datos distribuidos

## Panorama

Los apuntes externos estudian cómo gestionar datos cuando servicios separados poseen sus propios modelos y bases. La independencia reduce interferencias, pero exige resolver composición de información y coordinación de cambios. [EXT-001, «Patrones a Nivel de Aplicación»]

## Transacciones entre servicios

**Two-phase commit** utiliza un coordinador que consulta si los participantes pueden realizar la transacción y después decide confirmar o abortar. La fuente destaca consistencia inmediata con costos de bloqueo y rendimiento. [EXT-001, «Patrones a Nivel de Aplicación»]

**Sagas** divide una operación global en transacciones locales. Si falla un paso, se ejecutan acciones compensatorias para los pasos anteriores. El orden de las operaciones y los estados intermedios importan; los apuntes lo vinculan con consistencia eventual y disponibilidad. [EXT-001, «Patrones a Nivel de Aplicación»]

## Lecturas, modelos e historial

Un aggregate agrupa objetos de dominio para tratarlos como una unidad. La fuente presenta CQRS separando el modelo de escritura de una base de lectura que puede tener otro esquema y actualizarse a partir de eventos publicados por los servicios dueños de los datos. [EXT-001, «Patrones a Nivel de Aplicación»]

En esa misma sección, los apuntes denominan «event sourcing» a conservar eventos recibidos para construir información local y disponer de historial. La explicación se concentra en suscripción, duplicación de datos y composición de lecturas; no desarrolla por completo las garantías de un log autoritativo ni un protocolo de reconstrucción. Se conserva ese alcance de la fuente sin completar los detalles ausentes. [EXT-001, «Patrones a Nivel de Aplicación»]

## Relaciones

Estos patrones complementan la descomposición en [microservicios](microservicios.md) y pueden utilizar [eventos](procesamiento-de-eventos.md). Su cobertura detallada en esta tanda proviene de apuntes externos; la clase oficial sólo presenta un mapa de familias de patrones. [OFF-018, p. 21]

## Fuentes

- [EXT-001, «Patrones a Nivel de Aplicación»]
- [OFF-018, p. 21]

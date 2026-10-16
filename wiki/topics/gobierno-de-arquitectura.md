---
title: Gobierno de arquitectura
aliases:
- Architectural guardrails
- Platform engineering
- Internal Development Platform
- IDP
sources:
- EXT-001
- OFF-018
related:
- ciclo-arquitectura-negocio
- evolucion-de-la-arquitectura
- infraestructura-de-despliegue
prerequisites:
- arquitectura-de-software
---

# Gobierno de arquitectura

## Panorama

Los apuntes presentan los architectural guardrails como límites generales que permiten autonomía de equipos dentro de un conjunto conocido de decisiones. Buscan equilibrar velocidad y libertad con consistencia, previsibilidad e interoperabilidad. [EXT-001, «Architectural Guardrails»]

## Límites y automatización

Los ejemplos de la fuente incluyen restringir proveedores de infraestructura, motores de almacenamiento, lenguajes o tiempos de respuesta. Los equipos siguen siendo responsables de sus decisiones dentro de ese espacio. No son requisitos impuestos a este repositorio, sino ejemplos académicos de gobierno. [EXT-001, «Architectural Guardrails»]

Platform engineering implementa plataformas internas que automatizan provisión y hacen cumplir estas reglas. Los apuntes describen un punto central donde los equipos consultan métricas y costos, gestionan infraestructura y despliegan aplicaciones sin conocer todos los detalles subyacentes. [EXT-001, «Platform Engineering»]

La clase oficial aborda gobierno en SOA: seguridad, políticas de acceso, versiones, monitoreo, auditoría, tráfico y cumplimiento de contratos. También advierte sobre el costo y peso de una coordinación centralizada. [OFF-018, pp. 11-12]

## Relaciones

El [ciclo arquitectura-negocio](ciclo-arquitectura-negocio.md) explica cómo influyen las capacidades organizacionales en estas decisiones. La [evolución de arquitectura](evolucion-de-la-arquitectura.md) requiere mantener coherencia mientras cambian equipos, servicios y necesidades.

## Fuentes

- [EXT-001, «Architectural Guardrails» y «Platform Engineering»]
- [OFF-018, pp. 11-12]

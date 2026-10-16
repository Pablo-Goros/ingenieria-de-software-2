---
title: Infraestructura de despliegue
aliases:
- Contenedores
- Serverless
- Kubernetes
- Sidecar
- Service mesh
- HPA
sources:
- OFF-018
- EXT-001
- OFF-014
related:
- microservicios
- gobierno-de-arquitectura
- modelo-cuatro-mas-uno
prerequisites:
- microservicios
---

# Infraestructura de despliegue

## Panorama

La clase muestra una evolución de despliegue desde aplicaciones sobre máquinas físicas hacia máquinas virtuales, contenedores y runtimes serverless. Las alternativas cambian qué infraestructura se administra y cómo se empaqueta y ejecuta la aplicación. [OFF-018, p. 24]

## Contenedores y serverless

Los apuntes describen contenedores como una forma de aislar procesos y empaquetar aplicaciones con sus dependencias y configuración para reproducir su ejecución. En serverless, la ejecución se solicita a demanda y la gestión de máquinas queda abstraída para el equipo consumidor; la fuente señala costos de trazabilidad, restricciones de ejecución y dependencia del proveedor. [EXT-001, «Patrones a Nivel de Infraestructura»]

## Orquestación y comunicación

La fuente externa presenta Kubernetes para gestionar servicios sobre contenedores: asignar recursos, programar su ubicación y mantener la cantidad de instancias deseada. Incluye afinidad para ubicar cargas relacionadas y HPA como escalamiento basado en métricas como CPU y memoria. Estas son capacidades descritas por los apuntes, sin constituir una guía de configuración de una versión concreta del producto. [EXT-001, «Patrones a Nivel de Infraestructura»]

Un sidecar agrega un proceso auxiliar junto a la aplicación, por ejemplo un proxy. Los apuntes lo relacionan con service mesh y control del tráfico entre servicios. [EXT-001, «Patrones a Nivel de Infraestructura»]

## Relaciones

Estas decisiones forman parte del despliegue de [microservicios](microservicios.md) y se comunican mediante la vista física del [modelo 4+1](modelo-cuatro-mas-uno.md). Las [plataformas internas](gobierno-de-arquitectura.md) pueden ofrecer infraestructura bajo reglas compartidas. [OFF-014, p. 15; EXT-001, «Platform Engineering»]

## Fuentes

- [OFF-018, p. 24]
- [EXT-001, «Patrones a Nivel de Infraestructura» y «Platform Engineering»]
- [OFF-014, p. 15]

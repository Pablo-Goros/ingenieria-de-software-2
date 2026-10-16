---
title: Arquitectura orientada a servicios
aliases:
- SOA
- Service Oriented Architecture
- Service registry
- Orquestación
- Coreografía
sources:
- OFF-018
- EXT-001
- OFF-017
related:
- integracion-de-sistemas
- microservicios
prerequisites:
- integracion-de-sistemas
---

# Arquitectura orientada a servicios

## Panorama

SOA organiza funcionalidades de negocio como servicios independientes con interfaces definidas y contratos públicos. Pueden descubrirse, invocarse y reutilizarse para colaborar mediante mensajes estandarizados. La clase lo presenta como un estilo arquitectónico. [OFF-018, pp. 7-8]

## Principios

La clase enumera contratos estandarizados, bajo acoplamiento, abstracción, reutilización, autonomía, ausencia de estado entre invocaciones, descubrimiento y composición. El registro de servicios facilita conocer qué ofrece cada servicio y cómo invocarlo. [OFF-018, pp. 8-9]

La ausencia de estado entre invocaciones facilita distribuir llamadas entre nodos, pero forma parte de los principios de diseño presentados; el análisis del sistema debe explicitar dónde se conserva la información persistente. [OFF-018, p. 9]

## Composición y gobierno

Los apuntes distinguen servicios de grano fino y capacidades más amplias construidas combinándolos. Presentan **orquestación** como coordinación dirigida desde un componente central, y **coreografía** como coordinación entre servicios. En el ejemplo oficial, BPM coordina los procesos de punta a punta y el ESB intermedia la comunicación. [EXT-001, «Servicios»; OFF-018, p. 11]

El gobierno de contratos, versiones, accesos y monitoreo es parte del costo de ordenar la integración. La clase advierte que una estructura centralizada puede volverse pesada y presentar límites para evolución rápida, despliegues frecuentes y tolerancia a fallas. [OFF-018, pp. 11-12]

## Relaciones y evaluación

SOA es una respuesta al problema de [integración](integracion-de-sistemas.md). La comparación con [microservicios](microservicios.md) debe considerar el objetivo y las capacidades organizacionales. El repaso incluye el esquema SOA. [OFF-017, p. 11]

## Fuentes

- [OFF-018, pp. 7-12]
- [EXT-001, «Servicios»]
- [OFF-017, p. 11]

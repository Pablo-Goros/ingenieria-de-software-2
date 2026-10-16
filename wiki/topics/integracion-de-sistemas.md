---
title: Integración de sistemas
aliases:
- EAI
- Middleware
- Integration hub
- ESB
- BPM
- BAM
sources:
- OFF-018
- EXT-001
- OFF-017
related:
- arquitectura-orientada-a-servicios
- microservicios
- comunicacion-distribuida
prerequisites:
- arquitectura-de-software
---

# Integración de sistemas

## Panorama

Integrar sistemas exige conectar aplicaciones con modelos, interfaces y responsabilidades diferentes. La clase muestra la evolución desde conexiones punto a punto hacia capas de integración y exposición de servicios. [OFF-018, pp. 2-6]

## De conexiones individuales a intermediación

En punto a punto, cada sistema mantiene interfaces específicas con los demás. El enfoque es simple al inicio, pero al crecer aparecen alto acoplamiento, dificultad de mantenimiento y responsabilidades poco claras. [OFF-018, pp. 2, 10]

Un **hub de integración** centraliza adaptadores, ruteo, transformación de datos y mediación de protocolos. La clase menciona colas, HTTP/SOAP, RMI y JDBC como mecanismos posibles de conexión. El **ESB** actúa como canal entre sistemas y agrega capacidades de exposición y gobierno de servicios. [OFF-018, pp. 3-4, 11]

En el esquema SOA, **BPM** orquesta y coordina servicios para ejecutar procesos de negocio; el gobierno abarca seguridad, políticas de acceso, versiones, monitoreo, auditoría, tráfico y contratos. Los apuntes agregan **BAM** para observar el cumplimiento de los procesos y definir umbrales o notificaciones. [OFF-018, p. 11; EXT-001, «SOA»]

## Apertura de servicios

La clase muestra cómo las APIs pasan de integrar aplicaciones internas a exponer capacidades al exterior y permitir que terceros construyan sobre ellas. El problema incluye decidir qué publicar y cómo controlar el acceso. [OFF-018, pp. 5-6]

## Relaciones y evaluación

[SOA](arquitectura-orientada-a-servicios.md) organiza servicios reutilizables. Los [microservicios](microservicios.md) introducen otra relación entre estructura de software, equipos y despliegues. El repaso incluye punto a punto, SOA y API gateway. [OFF-017, p. 11]

## Fuentes

- [OFF-018, pp. 2-12]
- [EXT-001, «SOA»]
- [OFF-017, p. 11]

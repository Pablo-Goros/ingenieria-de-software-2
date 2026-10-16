---
title: Arquitectura de software
aliases:
- Software architecture
- ASR
- Rol del arquitecto
sources:
- OFF-013
- OFF-019
- EXT-001
- OFF-017
related:
- ciclo-arquitectura-negocio
- atributos-de-calidad
- estilos-arquitectonicos
- documentacion-de-arquitectura
prerequisites: []
---

# Arquitectura de software

## Panorama

La arquitectura describe la organización fundamental del sistema: componentes, relaciones entre ellos y con el entorno, y principios que orientan su diseño y evolución. Incluye decisiones sobre módulos, servicios, interfaces, dependencias e infraestructura; su alcance supera un diagrama de cajas. [OFF-013, p. 3]

## Conceptos centrales

Los requerimientos funcionales expresan qué servicios debe ofrecer el sistema. Los no funcionales y las restricciones condicionan cómo debe realizarlos. Un **requisito arquitectónicamente significativo (ASR)** puede pertenecer a cualquiera de los dos grupos: satisfacerlo obliga a tomar decisiones arquitectónicas importantes. Si cambia, probablemente cambie la arquitectura. [OFF-013, p. 13; OFF-019, pp. 6-7]

Por ejemplo, integrar pagos en tiempo real o admitir extensiones sin volver a desplegar el núcleo puede condicionar la estructura tanto como una exigencia de disponibilidad o concurrencia. Los ejemplos de ASR de la clase ilustran impactos sobre el diseño; no son requisitos universales para cualquier producto. [OFF-019, p. 7]

El arquitecto articula necesidades, restricciones y compromisos. Los apuntes externos destacan liderazgo, conocimiento del negocio, capacidad técnica, comunicación, negociación y visión. Las decisiones deben resolver una necesidad con recursos y plazos concretos, documentando supuestos ante la incertidumbre. [EXT-001, «Introducción a la Arquitectura de Software»]

## Relaciones

El [ciclo arquitectura-negocio](ciclo-arquitectura-negocio.md) explica las influencias sobre las decisiones. Los [atributos de calidad](atributos-de-calidad.md) permiten expresar objetivos; los [estilos](estilos-arquitectonicos.md) orientan la organización y las [vistas](documentacion-de-arquitectura.md) permiten comunicarla.

## Relevancia para la evaluación

El repaso oficial incluye explícitamente el rol del arquitecto y los requerimientos funcionales y no funcionales. [OFF-017, p. 2]

## Fuentes

- [OFF-013, pp. 3, 13]
- [OFF-019, pp. 6-7]
- [EXT-001, «Introducción a la Arquitectura de Software»]
- [OFF-017, p. 2]

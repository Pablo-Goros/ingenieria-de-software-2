---
title: Evolución de la arquitectura
aliases:
- BDUF
- YAGNI
- Arquitectura emergente
- Arquitectura intencional
- Architectural runway
sources:
- OFF-019
related:
- gobierno-de-arquitectura
- evaluacion-de-arquitecturas
prerequisites:
- arquitectura-de-software
---

# Evolución de la arquitectura

## Panorama

El momento y el esfuerzo dedicados a la arquitectura dependen del tamaño, el riesgo y la certeza necesaria. La clase contrasta la anticipación del big design up front con la adaptación y refactorización asociadas a YAGNI. Es un compromiso entre anticipar y responder a lo aprendido. [OFF-019, pp. 3-5]

## Alternativas de trabajo

La clase enumera cuatro posibilidades en Scrum: arquitectura antes de los sprints, sprint inicial dedicado, diseño y refactorización dentro de los sprints, o un equipo separado que analiza ASR y prepara cada release. Cada alternativa ubica la evaluación en momentos diferentes. El diseño dentro de los sprints requiere madurez y experiencia en el dominio. [OFF-019, p. 6]

## Arquitectura intencional, emergente y runway

La arquitectura intencional establece estrategias planificadas y alineadas con los atributos escogidos; el diseño emergente evoluciona incrementalmente para responder a nuevas necesidades. La clase utiliza SAFe como ejemplo de un enfoque que busca equilibrarlos. [OFF-019, p. 8]

El **architectural runway** es la base de componentes, código e infraestructura que permite implementar próximas funcionalidades sin rediseño adicional inmediato. Se utiliza, consume y renueva; anticipa necesidades de corto y mediano plazo sin diseñar todo el futuro del sistema. Incluye elementos intencionales y emergentes. [OFF-019, pp. 9-11]

La clase ilustra el concepto con infraestructura de seguridad, escalabilidad e integración preparada antes de incorporar pagos internacionales. El objetivo es que las funcionalidades futuras encuentren una base suficiente para avanzar. [OFF-019, p. 10]

## Relaciones

La [evaluación](evaluacion-de-arquitecturas.md) acompaña la evolución y los cambios importantes. El [gobierno](gobierno-de-arquitectura.md) establece límites compartidos para mantener coherencia entre decisiones autónomas.

## Fuentes

- [OFF-019, pp. 3-11, 32]

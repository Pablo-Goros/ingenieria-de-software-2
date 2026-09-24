---
title: "Arquitectura de software"
aliases: ["Software architecture"]
sources: [OFF-013, OFF-014]
related: [atributos-de-calidad, documentacion-de-arquitectura, estilos-de-arquitectura, integracion-de-sistemas]
prerequisites: [ingenieria-de-software]
---

# Arquitectura de software

## Overview

La arquitectura es la organización fundamental de un sistema: sus componentes, las relaciones entre ellos y con el entorno, y los principios que orientan su diseño y evolución. Esas decisiones consideran tanto las necesidades funcionales como las cualidades que el sistema debe sostener. [OFF-013, slide 3] [OFF-014, slides 23-24]

## Core concepts

Los requisitos no determinan por sí solos toda la arquitectura. Las expectativas y restricciones de los interesados, la organización que desarrolla el sistema, el entorno tecnológico y la experiencia del arquitecto también influyen en las decisiones. A su vez, una arquitectura puede afectar futuras decisiones técnicas y organizacionales. [OFF-013, slides 2, 4-10]

Los **drivers arquitectónicos** son escenarios funcionales y atributos de calidad críticos que sirven para modelar, comunicar y evaluar la arquitectura. Se consideran junto con restricciones del negocio y de la arquitectura, como plazos, costos, integración con sistemas existentes, integridad conceptual, completitud y robustez. [OFF-013, slides 22, 24]

La arquitectura toma forma mediante decisiones de organización de alto nivel. Los estilos y patrones conocidos ayudan a orientar esas decisiones; la selección debe atender los problemas y prioridades concretos del sistema. [OFF-013, slide 7] [OFF-014, slide 24]

La documentación y el diseño se complementan: las [vistas de arquitectura](documentacion-de-arquitectura.md) describen el sistema desde perspectivas relevantes, y los [estilos de arquitectura](estilos-de-arquitectura.md) guían su organización e interacción.

## Relationships

Los atributos de calidad y sus escenarios críticos condicionan las decisiones arquitectónicas. La descripción por vistas permite comunicar esas decisiones a distintos interesados y revisar cómo encajan entre sí.

## Sources

* [OFF-013, slides 2-10, 22, 24]
* [OFF-014, slides 23-24]

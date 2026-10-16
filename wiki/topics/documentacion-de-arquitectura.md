---
title: Documentación de arquitectura
aliases:
- Views and viewpoints
- Views and Beyond
- Vista
- Punto de vista
sources:
- OFF-014
- OFF-011
- EXT-001
related:
- modelo-cuatro-mas-uno
- modelo-c4
- estilos-arquitectonicos
prerequisites:
- arquitectura-de-software
---

# Documentación de arquitectura

## Panorama

Una descripción arquitectónica reúne artefactos que permiten entender, validar, criticar y mejorar la arquitectura. Debe comunicar elementos, interacciones, información, recursos y capacidades relevantes con suficiente detalle para orientar el desarrollo. [OFF-014, pp. 2-4]

## Vistas y puntos de vista

Una **vista** representa la arquitectura con un objetivo y una audiencia determinados. Un **punto de vista** define cómo construir esa representación: notación, elementos, alcance y destinatarios. Un diagrama de clases del sistema de ventas es una vista; las reglas que indican qué clases mostrar y con qué notación constituyen su punto de vista. [OFF-014, p. 6]

Views and Beyond agrupa vistas de módulos —organización del código—, de componentes y conectores —interacción en ejecución— y de asignación —mapeos a hardware, equipos o procesos—. Además de las vistas, incluye decisiones, justificaciones y escenarios. [OFF-014, p. 7]

## Nivel de detalle y mantenimiento

La documentación debe equilibrar visión general y detalle particular. Pretender incluir todo dificulta la comunicación. Las vistas se relacionan y deben mantenerse coherentes mientras el sistema evoluciona; pueden adaptarse o combinarse según el proyecto. [OFF-014, pp. 4, 17; OFF-011, pp. 13-15]

La fuente original de Kruchten separa el documento de arquitectura de las guías de diseño: el primero organiza la descripción por vistas; las segundas preservan decisiones necesarias para mantener la integridad arquitectónica. [OFF-011, p. 15]

## Relaciones

El [modelo 4+1](modelo-cuatro-mas-uno.md) organiza preocupaciones complementarias; [C4](modelo-c4.md) ofrece niveles de detalle. Los [estilos](estilos-arquitectonicos.md) guían decisiones de diseño, mientras las vistas permiten describirlas. [OFF-014, pp. 23, 58; EXT-001, «Estándar C4»]

## Fuentes

- [OFF-014, pp. 2-8, 17, 23, 58]
- [OFF-011, pp. 13-15]
- [EXT-001, «Estándar C4»]

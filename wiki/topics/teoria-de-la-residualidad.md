---
title: Teoría de la residualidad
aliases:
- Residuality theory
- Residuo
- Residual index
sources:
- EXT-001
related:
- diseno-dirigido-por-atributos
- evaluacion-de-arquitecturas
prerequisites:
- arquitectura-de-software
- atributos-de-calidad
---

# Teoría de la residualidad

## Panorama

Los apuntes externos resumen un video sobre residuality theory. En ese resumen, un residuo es lo que queda del sistema después de un evento que lo estresa. La propuesta desplaza la atención desde predecir exactamente el evento hacia diseñar límites y relaciones que permitan que lo restante siga siendo útil y adaptable. [EXT-001, «Residuality Theory (Video)»]

## Procedimiento descrito

Se parte de una arquitectura ingenua que resuelve las funciones básicas y se la enfrenta a estresores posibles. Para cada uno se analiza qué sobrevive y qué componentes faltan. Los residuos obtenidos se combinan en una arquitectura coherente y se compara su comportamiento frente a nuevos estresores. [EXT-001, «Residuality Theory (Video)»]

El resumen menciona criticality como un equilibrio para mantenerse operativo ante incertidumbre y un residual index para comparar resultados. No incluye una fórmula o protocolo suficiente para calcularlo, por lo que esta página no completa ese cálculo. [EXT-001, «Residuality Theory (Video)»]

## Relaciones y alcance de la fuente

La fuente relaciona el enfoque con identificar componentes que fallan juntos y lo contrasta con ADD. Su afirmación de que ADD nunca contempla fallas conjuntas es una valoración de los apuntes; las diapositivas oficiales incorporadas no desarrollan esa comparación. No se toma esa valoración como una restricción universal de [ADD](diseno-dirigido-por-atributos.md). [EXT-001, «Residuality Theory (Video)»]

Esta página está respaldada por el resumen externo, no por el video original ni por una fuente primaria adicional. El vínculo con la [evaluación](evaluacion-de-arquitecturas.md) consiste en confrontar una arquitectura con escenarios y analizar qué conserva.

## Fuentes

- [EXT-001, «Residuality Theory (Video)»]

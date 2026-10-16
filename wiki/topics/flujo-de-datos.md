---
title: Arquitecturas de flujo de datos
aliases:
- Dataflow
- Batch secuencial
- Pipes and filters
- Hierarchical layers
- Arquitectura en capas
sources:
- OFF-014
- OFF-017
related:
- estilos-arquitectonicos
- persistencia
- procesamiento-de-eventos
prerequisites:
- estilos-arquitectonicos
---

# Arquitecturas de flujo de datos

## Panorama

El dominio dataflow describe cómo fluyen los datos y cómo se procesan o transforman. La clase desarrolla tres estilos: batch secuencial, pipes and filters y capas jerárquicas. [OFF-014, p. 25]

## Comparación

| Estilo | Organización | Beneficio y compromiso |
| --- | --- | --- |
| Batch secuencial | Programas independientes; cada etapa termina antes de comenzar la siguiente y transfiere el conjunto de datos, frecuentemente mediante archivos. | Sencillez para grandes lotes; mayor latencia. |
| Pipes and filters | Filtros independientes transforman datos de manera incremental; los pipes los transportan y conectan etapas. | Flexibilidad y posibilidad de solapar procesamiento; coordinación más compleja. |
| Capas jerárquicas | Cada capa ofrece servicios a la superior y consume los de la inferior. | Abstracción, reutilización e intercambio; posibles costos de rendimiento y propagación de cambios. |

[OFF-014, pp. 26-29]

## Ejemplos y selección

La clase ilustra batch con las fases de compiladores y con liquidaciones nocturnas; pipes and filters con transformaciones encadenadas de imagen o video y procesamiento de streams; las capas con protocolos de red y aplicaciones organizadas en presentación, negocio y datos. [OFF-014, pp. 26-33]

La guía de selección distingue volumen en lotes, flujo continuo y organización por abstracciones. En capas, encontrar el nivel adecuado es una dificultad central; no todo sistema se estructura bien de esa manera. [OFF-014, pp. 28-29, 33]

## Relaciones

El [procesamiento de eventos](procesamiento-de-eventos.md) puede organizar transformaciones continuas. La [persistencia](persistencia.md) interviene cuando las etapas intercambian archivos o realizan ETL.

## Relevancia para la evaluación

Los tres estilos están incluidos en el repaso oficial de dataflow. [OFF-017, p. 4]

## Fuentes

- [OFF-014, pp. 25-33]
- [OFF-017, p. 4]

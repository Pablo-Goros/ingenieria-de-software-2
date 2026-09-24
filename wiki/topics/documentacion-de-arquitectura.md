---
title: "Documentación de arquitectura"
aliases: ["Modelo 4+1", "4+1", "Views and viewpoints", "Views and Beyond"]
sources: [OFF-011, OFF-012, OFF-014, EXT-001]
related: [arquitectura-de-software, estilos-de-arquitectura]
prerequisites: [arquitectura-de-software]
---

# Documentación de arquitectura

## Overview

Una arquitectura se documenta mediante perspectivas que responden a las preocupaciones de distintos interesados. El modelo 4+1 organiza cuatro vistas técnicas y las relaciona mediante escenarios que muestran cómo funciona el sistema en situaciones concretas. [OFF-011, pp. 2-3] [OFF-014, slides 5, 10-16]

## Core concepts

Una **vista** es una representación de la arquitectura para un propósito y grupo de interés. Un **punto de vista** define las preocupaciones que debe atender esa representación y orienta qué elementos y notaciones usar. [OFF-014, slide 6]

| Vista 4+1 | Qué describe |
| --- | --- |
| Lógica | Funciones y estructura del sistema desde sus elementos principales, como clases, objetos y capas. |
| Procesos | Comportamiento en ejecución, concurrencia, sincronización y aspectos de rendimiento. |
| Desarrollo | Organización estática del software en módulos, componentes, paquetes y dependencias. |
| Física | Asignación del software a nodos y recursos de hardware. |
| Escenarios (+1) | Casos de uso que atraviesan las otras vistas y ayudan a comprobar que forman una arquitectura coherente. |

[OFF-011, pp. 2-3, 10] [OFF-014, slides 10-16]

Las vistas se relacionan entre sí, pero no tienen correspondencia uno a uno. El modelo puede adaptarse: Kruchten señala que se pueden omitir vistas que no aportan información para el sistema y combinar descripciones muy similares en sistemas pequeños. [OFF-011, pp. 11, 14]

El enfoque **Views and Beyond** agrupa las vistas en módulos, componentes y conectores, y asignación. Además de esos diagramas, la documentación puede incluir escenarios y otra información necesaria para entender las decisiones. [OFF-014, slide 7]

El apunte externo también nombra C4 como otro modelo de documentación, pero las fuentes oficiales incorporadas no desarrollan sus vistas; por eso aquí no se detallan. [EXT-001]

El artículo sobre RUP muestra una aplicación del modelo 4+1 al diseño de una aplicación web: los casos de uso y las funciones aparecen en la vista lógica; los módulos en desarrollo; la concurrencia y el rendimiento en procesos; el despliegue en la vista física; y los escenarios conectan las demás vistas. [OFF-012, pp. 5-8]

Hay una inconsistencia en el resumen inicial de ese artículo: lista la vista física como una perspectiva del usuario, pero su figura la identifica con la topología del producto. El artículo original de Kruchten y las diapositivas de clase describen esta vista como la asignación del software al hardware; este tema sigue esa definición y deja registrada la discrepancia. [OFF-012, pp. 5-6] [OFF-011, pp. 2-3] [OFF-014, slide 15]

## Sources

* [OFF-011, pp. 2-3, 10-11, 14]
* [OFF-012, pp. 5-9]
* [OFF-014, slides 5-16]
* [EXT-001]

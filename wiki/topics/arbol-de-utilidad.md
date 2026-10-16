---
title: Árbol de utilidad
aliases:
- Utility tree
- Quality attribute utility tree
sources:
- OFF-019
- OFF-015
related:
- atam
- atributos-de-calidad
prerequisites:
- atributos-de-calidad
---

# Árbol de utilidad

## Panorama

El árbol de utilidad organiza los atributos de calidad y sus escenarios para enfocar la evaluación. En ATAM se construye durante la primera fase y orienta el análisis posterior de los enfoques arquitectónicos. [OFF-019, pp. 25-26]

## Estructura y prioridad

Los nodos superiores son atributos de calidad; los intermedios son características que contribuyen a ellos; las hojas son escenarios concretos. Cada hoja se anota con **importancia para los stakeholders** y **dificultad de lograr el objetivo**, usando alta, media o baja. Son dos dimensiones distintas. [OFF-019, p. 26]

No alcanza con escribir el nombre de un atributo como hoja. El árbol de la clase desarrolla, por ejemplo, rendimiento en características de latencia y throughput, con escenarios medibles. El árbol convierte preocupaciones amplias en situaciones analizables. [OFF-019, p. 26]

## Ejemplo de la fuente

El árbol de CAAS organiza disponibilidad mediante preocupaciones como no fallar ante datos inválidos, degradarse de forma controlada o conservar información crítica cuando existe redundancia. Una de sus hojas pide continuar funcionando ante la falla de una partición. La tabla pertenece al ejemplo docente del material ATAM. [OFF-015, p. 21]

## Relaciones

En [ATAM](atam.md), los escenarios iniciales se amplían con el brainstorming de stakeholders y se priorizan por votación. Los resultados alimentan el análisis de riesgos, puntos sensibles y compromisos de los enfoques elegidos. [OFF-019, pp. 27-28]

## Fuentes

- [OFF-019, pp. 25-28]
- [OFF-015, p. 21] (tabla inspeccionada visualmente)

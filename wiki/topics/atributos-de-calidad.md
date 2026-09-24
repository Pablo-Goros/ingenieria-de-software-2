---
title: "Atributos de calidad"
aliases: ["Requisitos no funcionales", "Quality attributes"]
sources: [OFF-001, OFF-013]
related: [calidad-de-software, arquitectura-de-software]
prerequisites: [calidad-de-software]
---

# Atributos de calidad

## Overview

Un atributo de calidad describe una característica que el sistema debe sostener y que, en general, no cambia la funcionalidad requerida directamente. Permite expresar cómo se espera que funcione el sistema, además de qué funciones ofrece. [OFF-001, pp. 7-8] [OFF-013, slide 15]

## Core concepts

El material clasifica los atributos en cuatro grupos: [OFF-013, slides 18-21]

* **De ejecución:** disponibilidad, tolerancia a fallos, interoperabilidad, gestionabilidad, personalización, rendimiento, precisión, confiabilidad, escalabilidad, auditabilidad y seguridad.
* **De diseño:** integridad conceptual, mantenibilidad, portabilidad y reutilización.
* **Del sistema:** soportabilidad y testeabilidad.
* **Del usuario:** accesibilidad y usabilidad.

Algunos términos describen propiedades cercanas, pero distintas. La **disponibilidad** expresa cuánto tiempo el sistema está operativo; la **tolerancia a fallos**, si puede seguir respondiendo cuando falla un componente. El **rendimiento** mide la respuesta dentro de un intervalo, mientras que la **escalabilidad** describe cómo se sostiene el sistema al crecer la carga. La **mantenibilidad** se refiere a la facilidad de realizar cambios, y la **testeabilidad**, a la facilidad de definir y ejecutar pruebas. [OFF-013, slides 18-20]

Los atributos y restricciones pueden competir. Por eso, la arquitectura debe buscar compromisos explícitos entre las cualidades que más importan al sistema y sus costos o efectos secundarios. [OFF-001, pp. 1, 7-8] [OFF-013, slide 28]

## Example

El material propone contrastes como seguridad y usabilidad: agregar autenticación de dos factores aumenta la seguridad, pero vuelve más trabajoso el ingreso. También compara disponibilidad con costo de infraestructura, portabilidad con eficiencia y escalabilidad con complejidad. La opción adecuada depende de las prioridades del sistema. [OFF-013, slide 28]

## Relationships

Los atributos de calidad son entradas importantes para las decisiones de [arquitectura de software](arquitectura-de-software.md). Sus escenarios críticos, junto con las restricciones, ayudan a evaluar alternativas arquitectónicas.

## Sources

* [OFF-001, pp. 1, 7-10]
* [OFF-013, slides 14-21, 27-28]

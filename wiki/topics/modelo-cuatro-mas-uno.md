---
title: Modelo 4+1 de vistas
aliases:
- 4+1
- Modelo de Kruchten
- Logical view
- Process view
- Development view
- Physical view
sources:
- OFF-011
- OFF-014
- OFF-017
related:
- documentacion-de-arquitectura
- modelo-c4
prerequisites:
- documentacion-de-arquitectura
---

# Modelo 4+1 de vistas

## Panorama

El modelo de Kruchten describe una arquitectura mediante cuatro vistas técnicas y escenarios que las articulan. Cada vista responde a preocupaciones de distintos stakeholders; un único diagrama no expresa adecuadamente estructura lógica, organización de código, ejecución y despliegue. [OFF-011, pp. 2-3]

## Las cinco perspectivas

| Vista | Pregunta y contenido | Diagramas utilizados en la clase |
| --- | --- | --- |
| Lógica | Qué funciones soporta y qué abstracciones las organizan: clases, objetos y relaciones de dominio. | Clases, componentes; también secuencias o comunicación según lo representado. |
| Procesos | Cómo se ejecuta: concurrencia, comunicación, sincronización, rendimiento y disponibilidad. | Actividades, secuencias o comunicación. |
| Desarrollo | Cómo se organiza el software para construirlo: módulos, paquetes, bibliotecas y dependencias. | Paquetes y componentes. |
| Física | En qué nodos se ejecuta y cómo se distribuye el software sobre hardware y redes. | Despliegue. |
| Escenarios (+1) | Qué interacciones importantes atraviesan y validan las otras vistas. | Casos de uso, secuencias y narrativas de interacción. |

La tabla reúne el foco de las vistas y las asociaciones de diagramas de la clase. La notación por sí sola no determina la vista: las diapositivas incluyen secuencias tanto en la vista lógica como en procesos. Hay que identificar la preocupación representada. [OFF-014, pp. 10-16]

## Correspondencias y adaptación

Las vistas no son independientes ni tienen un mapeo uno a uno. Una clase puede requerir varias unidades de implementación o ejecutarse mediante distintos procesos; los procesos se asignan a configuraciones físicas. Los escenarios ayudan a descubrir elementos y luego a validar su colaboración. [OFF-011, pp. 10-14]

Kruchten permite omitir vistas inútiles o combinar algunas en sistemas pequeños. El proceso es iterativo: prototipar, medir, analizar y refinar la arquitectura ayuda a reducir riesgos. Su artículo utiliza notaciones de Booch y otras herramientas de la época; la clase presenta asociaciones con UML. Esa actualización de notación no cambia el propósito de cada vista. [OFF-011, pp. 4, 6-8, 14-15; OFF-014, pp. 12-17]

## Relevancia para la evaluación

El repaso incluye las cinco vistas y los diagramas UML asociados. [OFF-017, p. 3]

## Fuentes

- [OFF-011, pp. 2-15] (páginas del PDF, incluida la portada de ResearchGate)
- [OFF-014, pp. 10-17]
- [OFF-017, p. 3]

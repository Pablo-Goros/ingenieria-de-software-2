---
title: Atributos de calidad
aliases:
- Quality attributes
- Disponibilidad
- Confiabilidad
- Performance
- Escalabilidad
- Accesibilidad
sources:
- OFF-013
- OFF-019
- EXT-019
- EXT-001
- OFF-017
related:
- diseno-dirigido-por-atributos
- evaluacion-de-arquitecturas
- arbol-de-utilidad
prerequisites:
- arquitectura-de-software
---

# Atributos de calidad

## Panorama

Los atributos de calidad expresan características del sistema que complementan su funcionalidad: no alcanza con determinar qué hace; también importa cómo responde, se modifica, se opera y se utiliza. Su prioridad depende del sistema y sus restricciones. [OFF-013, pp. 15-17, 22, 24; EXT-001, «Calidad»]

## Clasificación utilizada en el material

| Grupo | Atributos y significado |
| --- | --- |
| Ejecución | Disponibilidad: proporción de tiempo operativo. Tolerancia a fallos: continuar respondiendo ante fallas, aun con degradación. Confiabilidad: mantenerse operacional en el tiempo. |
| Ejecución | Rendimiento: respuesta temporal. Escalabilidad: soportar aumentos de carga o ampliar capacidad. Precisión: detalle suficiente de los resultados numéricos. |
| Ejecución | Interoperabilidad: intercambiar información con otros sistemas. Gestionabilidad: instrumentación útil para administrar y monitorear. Personalización: adaptación por el usuario. |
| Ejecución | Auditabilidad: examinar registros y actividades. Seguridad: prevenir acciones indebidas y pérdida o divulgación de información. |
| Diseño | Integridad conceptual: coherencia del diseño. Mantenibilidad: facilidad de cambio. Portabilidad: uso en otros entornos. Reusabilidad: aprovechamiento en otros contextos. |
| Sistema | Soportabilidad: información para identificar y resolver problemas. Testeabilidad: facilidad para definir y ejecutar criterios de prueba. |
| Usuario | Accesibilidad: uso por un universo amplio de personas. Usabilidad: satisfacción de necesidades y facilidad de uso para el usuario previsto. |

La tabla resume la clasificación compartida por las diapositivas y la hoja externa. Disponibilidad, tolerancia a fallos y confiabilidad están relacionadas, pero describen propiedades diferentes; tampoco deben confundirse accesibilidad y usabilidad. [OFF-013, pp. 17-21; EXT-019, p. 1]

## Uso en el diseño

Identificar un atributo no basta: hay que cuantificarlo y formular escenarios que permitan analizarlo. Los apuntes proponen priorizar los atributos para resolver compromisos, porque favorecer uno puede perjudicar otro o incrementar costo y plazo. [EXT-001, «Calidad» y «Attribute Driven Design»]

La clase de evaluación usa métricas como tiempo de respuesta, usuarios concurrentes, incidentes de seguridad y tiempos entre fallas o de recuperación. Las métricas deben interpretarse según el atributo y el contexto. [OFF-019, pp. 17, 22]

## Relaciones

El [diseño dirigido por atributos](diseno-dirigido-por-atributos.md) transforma prioridades en decisiones. El [árbol de utilidad](arbol-de-utilidad.md) organiza atributos y escenarios para [ATAM](atam.md).

## Relevancia para la evaluación

Los atributos figuran en el repaso oficial y en una diapositiva marcada como parcializable. [OFF-017, p. 2; OFF-019, p. 22]

## Fuentes

- [OFF-013, pp. 15-24]
- [OFF-019, pp. 17, 22]
- [EXT-019, p. 1]
- [EXT-001, «Calidad» y «Attribute Driven Design»]
- [OFF-017, p. 2]

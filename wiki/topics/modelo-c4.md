---
title: Modelo C4
aliases:
- Context
- Containers
- Components
- Code
sources:
- EXT-001
related:
- documentacion-de-arquitectura
- modelo-cuatro-mas-uno
prerequisites:
- documentacion-de-arquitectura
---

# Modelo C4

## Panorama

Los apuntes externos presentan C4 como una forma jerárquica de observar la arquitectura, haciendo zoom desde el contexto hasta el código. Priorizan la comunicación mediante abstracciones comunes y una notación independiente de formas o colores particulares. [EXT-001, «Estándar C4»]

## Niveles

| Nivel | Qué muestra | Audiencia indicada |
| --- | --- | --- |
| Contexto | El sistema como caja negra, sus usuarios y sistemas externos. | Stakeholders técnicos y no técnicos. |
| Contenedores | Aplicaciones y almacenamientos que componen el sistema: servidores web, aplicaciones móviles, bases o servicios. | Desarrollo, operaciones y soporte. |
| Componentes | Estructura interna de un contenedor, agrupando funcionalidad detrás de interfaces. | Arquitectos y desarrolladores. |
| Código | Implementación de un componente, por ejemplo clases. | Desarrolladores. |

Los niveles cambian la escala y el detalle de la descripción. En este uso de la palabra, un contenedor es una aplicación o almacenamiento de la arquitectura; los ejemplos de la fuente incluyen bases y aplicaciones móviles. [EXT-001, «Estándar C4»]

## Relaciones

Los apuntes proponen combinar C4 para la estructura estática con vistas de procesos y escenarios para el comportamiento y la validación. Esto lo relaciona con el [modelo 4+1](modelo-cuatro-mas-uno.md), sin identificar cada nivel de C4 con una de sus vistas. [EXT-001, «Estándar C4»]

## Fuentes

- [EXT-001, «Estándar C4»]. Cobertura respaldada por apuntes externos; el repaso oficial incorporado no menciona C4 explícitamente.

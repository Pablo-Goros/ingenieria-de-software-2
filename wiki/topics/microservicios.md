---
title: Microservicios
aliases:
- Microservices
- Monolito
- DevOps
- Descomposición por subdominios
sources:
- OFF-018
- EXT-001
related:
- arquitectura-orientada-a-servicios
- patrones-de-datos-distribuidos
- patrones-de-comunicacion-entre-servicios
- infraestructura-de-despliegue
prerequisites:
- integracion-de-sistemas
---

# Microservicios

## Panorama

La clase presenta microservicios como una arquitectura que, junto con prácticas DevOps y equipos pequeños y autónomos, permite entregar cambios de manera rápida y confiable. La arquitectura es una parte de ese conjunto organizacional y técnico. [OFF-018, pp. 14-18, 25]

## Motivación y descomposición

El ejemplo monolítico agrupa funcionalidades en un único artefacto. Al crecer equipos y cambios, la clase señala problemas de coordinación, tiempos desde commit hasta despliegue, escalamiento y tolerancia a fallas. Los apuntes externos enfatizan especialmente la autonomía de equipos y la velocidad de entrega como motivación. [OFF-018, pp. 16-18; EXT-001, «Microservicios»]

La descomposición por subdominios separa capacidades del negocio, como pedidos, entregas o contabilidad, en lugar de dividir sólo por capas técnicas. El material la relaciona con Domain-Driven Design. [OFF-018, p. 22]

## Compromisos y condiciones

Definir servicios adecuados, coordinar transacciones sobre varias bases, probar un sistema distribuido y desplegar cambios que atraviesan servicios son dificultades explícitas. Se agregan latencia, trazabilidad y coordinación. [OFF-018, pp. 19-20]

La clase desaconseja microservicios ante dominio simple, equipo pequeño, falta de madurez DevOps o ausencia de necesidad de escalar partes por separado. Su conclusión exige combinar arquitectura, autonomía y prácticas de entrega. [OFF-018, pp. 20, 25]

## Relaciones

Los [patrones de datos](patrones-de-datos-distribuidos.md) tratan consistencia y consultas; los [patrones de comunicación](patrones-de-comunicacion-entre-servicios.md) organizan exposición y manejo de fallas; la [infraestructura](infraestructura-de-despliegue.md) soporta operación y despliegue. [OFF-018, pp. 21-24; EXT-001, «Patrones a Nivel de Aplicación», «Patrones a Nivel de Comunicación» y «Patrones a Nivel de Infraestructura»]

## Fuentes

- [OFF-018, pp. 14-25]
- [EXT-001, «Microservicios» y secciones de patrones]

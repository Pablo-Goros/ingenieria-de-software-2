---
title: Diseño dirigido por atributos
aliases:
- Attribute Driven Design
- ADD
- Drivers de arquitectura
sources:
- OFF-013
- EXT-001
related:
- atributos-de-calidad
- estilos-arquitectonicos
- atam
prerequisites:
- atributos-de-calidad
---

# Diseño dirigido por atributos

## Panorama

Attribute Driven Design utiliza restricciones, requerimientos funcionales y requerimientos de calidad para construir una arquitectura conceptual. Los escenarios críticos actúan como drivers: permiten modelar, comunicar y evaluar las decisiones. [OFF-013, pp. 16, 24]

## Procedimiento presentado en los apuntes

Los apuntes externos desarrollan una adaptación iterativa del proceso. La siguiente secuencia corresponde a esa fuente, sin atribuirla como especificación completa del método original. [EXT-001, «Attribute Driven Design»]

1. Identificar, cuantificar y ordenar los atributos de calidad. El orden orienta los compromisos entre atributos y restricciones.
2. Delimitar el sistema: tipo de aplicación, usuarios y agentes externos. Construir una arquitectura mínima que cubra las funciones.
3. Tomar un atributo prioritario y plantear un escenario posible que lo ponga a prueba.
4. Analizar si la arquitectura candidata sobrevive. Si no, introducir cambios y volver a verificar funciones y escenarios anteriores, respetando su prioridad.
5. Repetir con nuevos escenarios y atributos. Documentar arquitectura candidata, no riesgos, riesgos asumidos, compromisos y supuestos. [EXT-001, «Attribute Driven Design»]

Resolver un riesgo tiene un costo. La fuente admite asumir algunos riesgos cuando su probabilidad y el costo de resolverlos no justifican la inversión, dejando explícita la decisión y su mitigación. Un escenario resuelto constituye evidencia del análisis realizado, no una garantía de ausencia de cualquier falla imaginable. [EXT-001, «Attribute Driven Design»]

## Relaciones

Los [estilos arquitectónicos](estilos-arquitectonicos.md) aportan organizaciones candidatas. [ATAM](atam.md) permite evaluar decisiones y sus efectos; los apuntes distinguen el uso de ADD para diseñar de la evaluación de arquitecturas heredadas o propuestas por terceros. [EXT-001, «Validación de Proyectos Legacy o Third-Party»]

## Fuentes

- [OFF-013, pp. 16, 24]
- [EXT-001, «Attribute Driven Design» y «Validación de Proyectos Legacy o Third-Party»]

---
title: Evaluación de arquitecturas
aliases:
- SAAM
- SLI
- SLO
- SLA
- Prototipos
- Simulaciones
sources:
- OFF-019
- OFF-015
- EXT-001
- OFF-017
related:
- atam
- evolucion-de-la-arquitectura
prerequisites:
- atributos-de-calidad
---

# Evaluación de arquitecturas

## Panorama

Evaluar permite determinar si una arquitectura es apropiada, comparar candidatas, analizar cuánto satisface los atributos de calidad y detectar riesgos técnicos tempranamente. La clase propone métodos repetibles para reducir o mitigar esos riesgos. [OFF-019, pp. 12-13]

## Técnicas

| Grupo | Técnicas | Uso |
| --- | --- | --- |
| Cualitativas | Escenarios | Narrativas de situaciones posibles desde la perspectiva de stakeholders. |
| Cualitativas | Checklists y cuestionarios | Criterios que el evaluador califica o responde. |
| Cuantitativas | Métricas | Medir respuesta, fallas, usuarios concurrentes, incidentes u otras propiedades. |
| Cuantitativas | Simulaciones, experimentos y prototipos | Modelar comportamiento, probar hipótesis o construir versiones preliminares. |
| Cuantitativas | Modelos matemáticos | Analizar probabilísticamente fallas o estimar rendimiento y utilización de recursos. |

[OFF-019, pp. 14-19]

Los modelos matemáticos y simulaciones demandan más esfuerzo; la clase justifica su uso en sistemas de alta criticidad. La técnica y el momento de evaluación deben elegirse según el proyecto y su metodología. [OFF-019, pp. 18-19, 32]

## Indicadores, objetivos y acuerdos

La clase distingue **SLI**, métrica concreta y cuantificable; **SLO**, objetivo fijado para un SLI; y **SLA**, acuerdo formal o contractual entre proveedor y cliente, presentado como objetivos más penalidades. [OFF-019, p. 17]

Los apuntes externos llaman al SLO «data real» del compromiso y al SLI información del momento actual. Esa descripción difiere de la distinción explícita de la clase; para el vocabulario del curso se conserva la formulación oficial anterior. [EXT-001, «Validación de Proyectos Legacy o Third-Party»; OFF-019, p. 17]

## Metodologías y relaciones

La clase presenta SAAM, [ATAM](atam.md) y Lightweight ATAM como metodologías basadas en escenarios, diferenciando su foco y esfuerzo. El material ATAM incorpora autoevaluación, revisión por pares y revisión externa según el proyecto. [OFF-019, p. 20; OFF-015, pp. 2-5]

## Relevancia para la evaluación

El repaso reproduce las técnicas de evaluación y ATAM. [OFF-017, pp. 8-9]

## Fuentes

- [OFF-019, pp. 12-20, 32]
- [OFF-015, pp. 2-5]
- [EXT-001, «Validación de Proyectos Legacy o Third-Party»]
- [OFF-017, pp. 8-9]

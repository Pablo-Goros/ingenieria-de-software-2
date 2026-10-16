---
title: ATAM
aliases:
- Architecture Tradeoff Analysis Method
- Lightweight ATAM
- Puntos sensibles
- Riesgos arquitectónicos
- Trade-offs
sources:
- OFF-019
- OFF-015
- OFF-017
related:
- arbol-de-utilidad
- evaluacion-de-arquitecturas
- diseno-dirigido-por-atributos
prerequisites:
- evaluacion-de-arquitecturas
---

# ATAM

## Panorama

ATAM evalúa decisiones arquitectónicas frente a atributos de calidad mediante escenarios y preguntas. Es principalmente cualitativo: identifica riesgos, puntos sensibles y compromisos; no sustituye las mediciones empíricas de comportamiento. La clase atribuye su desarrollo al SEI. [OFF-019, pp. 20-21]

## Fases del proceso

1. **Fase 0, preparación:** acordar la evaluación y presentar al equipo. Participan evaluadores, redactores, inquisidor, moderador, decisores y stakeholders.
2. **Fase 1, evaluación inicial:** presentar ATAM, drivers del negocio y arquitectura; identificar enfoques, generar el árbol de utilidad y analizar decisiones.
3. **Fase 2, evaluación ampliada:** incorporar stakeholders, generar y priorizar escenarios mediante brainstorming y votación, y volver a analizar los enfoques.
4. **Fase 3, resultados:** comunicar el análisis y producir el reporte final. [OFF-019, pp. 23-29; OFF-015, pp. 34-37]

El reporte reúne negocio y arquitectura, escenarios, árbol de utilidad, enfoques, decisiones y hallazgos. La fuente adicional ATAM explicita también la correspondencia entre decisiones y requerimientos de calidad y los temas de riesgo que reflejan debilidades sistémicas. [OFF-019, p. 29; OFF-015, pp. 35, 39]

## Hallazgos

- **Riesgo:** una decisión puede generar consecuencias indeseables frente a un escenario.
- **No riesgo:** el análisis sustenta que una decisión responde adecuadamente a la situación considerada.
- **Punto sensible:** una decisión tiene un efecto marcado sobre un atributo.
- **Compromiso o trade-off:** la decisión afecta atributos cuya satisfacción debe balancearse. [OFF-019, p. 28; OFF-015, pp. 10, 23, 39]

En el caso docente CAAS, aislar dependencias del sistema operativo aparece como punto sensible para portabilidad; permitir configurar límites de temperatura aumenta flexibilidad pero reduce seguridad operacional. La falta de interfaces para simuladores es un riesgo identificado. Es un ejemplo de enseñanza de la fuente oficial, independiente de las consignas de práctica catalogadas. [OFF-015, p. 23]

## Versión liviana

Lightweight ATAM reduce esfuerzo y formalidad: puede realizarlo el equipo del proyecto y deja una minuta. La clase advierte menor profundidad, diversidad de ideas y objetividad; su tabla estima una sesión de 4 a 6 horas. Son estimaciones del esquema presentado, no una duración universal. [OFF-019, pp. 30-31]

## Relaciones y evaluación

El [árbol de utilidad](arbol-de-utilidad.md) enfoca las prioridades. El repaso incluye ATAM y sus fases. [OFF-017, p. 9]

## Fuentes

- [OFF-019, pp. 20-31]
- [OFF-015, pp. 10, 23, 34-39]
- [OFF-017, p. 9]

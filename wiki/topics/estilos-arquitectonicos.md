---
title: Estilos arquitectónicos
aliases:
- Architectural styles
sources:
- OFF-014
- OFF-017
related:
- flujo-de-datos
- comunicacion-distribuida
- modelo-vista-controlador
- procesamiento-de-eventos
- arquitectura-orientada-a-servicios
prerequisites:
- arquitectura-de-software
---

# Estilos arquitectónicos

## Panorama

Un estilo es un conjunto de decisiones de diseño aplicables a un contexto que restringen otras decisiones para obtener un beneficio. Seguirlo aporta consistencia y previsibilidad. Un sistema puede combinar varios estilos cuando resuelven problemas en contextos diferentes. [OFF-014, p. 24]

## Familias trabajadas

- [Flujo de datos](flujo-de-datos.md): organización del procesamiento y transformación mediante batch secuencial, pipes and filters o capas.
- [Comunicación distribuida](comunicacion-distribuida.md): descubrimiento e interacción entre participantes mediante broker, publicación-suscripción, forwarder-receiver o client-dispatcher-server.
- [Sistemas interactivos y MVC](modelo-vista-controlador.md): separación entre funcionalidad principal y presentación.
- [Procesamiento de eventos](procesamiento-de-eventos.md): productores, canales y consumidores que reaccionan a sucesos. [OFF-014, pp. 25, 34, 48, 52-54]

Elegir un estilo requiere vincular el problema con sus beneficios y compromisos. Por ejemplo, el batch favorece procesamiento por lotes; pipes and filters admite flujo continuo; las capas organizan responsabilidades, con un posible costo de rendimiento. [OFF-014, pp. 26-29, 33]

## Relaciones

Las [vistas](documentacion-de-arquitectura.md) describen perspectivas del sistema; los estilos guían cómo organizarlo. La clase sintetiza esta relación como descripción mediante vistas y diseño mediante estilos. [OFF-014, pp. 23, 58]

## Relevancia para la evaluación

Las cuatro familias aparecen explícitamente en el repaso del parcial. [OFF-017, pp. 3-7]

## Fuentes

- [OFF-014, pp. 23-58]
- [OFF-017, pp. 3-7]

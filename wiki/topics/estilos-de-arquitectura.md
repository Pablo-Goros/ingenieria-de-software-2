---
title: "Estilos de arquitectura"
aliases: ["Estilos arquitectónicos", "Architectural styles"]
sources: [OFF-014]
related: [arquitectura-de-software, atributos-de-calidad, documentacion-de-arquitectura]
prerequisites: [arquitectura-de-software]
---

# Estilos de arquitectura

## Overview

Un estilo arquitectónico es un conjunto de decisiones de alto nivel que restringe y guía la organización de un sistema. Se puede combinar más de un estilo cuando el sistema contiene contextos distintos; la elección depende de los problemas y prioridades que la arquitectura debe resolver. [OFF-014, slide 24]

## Core concepts

### Flujo de datos

En los estilos de flujo de datos, la organización sigue el recorrido de los datos por etapas de procesamiento. [OFF-014, slides 25-28]

* **Batch secuencial:** cada etapa consume la salida de la anterior. Sirve para procesar grandes volúmenes fuera de línea, por ejemplo una liquidación nocturna o una cadena de compilación. Es simple, pero puede tener alta latencia. [OFF-014, slide 26]
* **Pipes & Filters:** filtros independientes transforman un flujo y se conectan mediante pipes. Es útil para streaming y para encadenar transformaciones; resulta más flexible que batch, aunque coordinar los filtros es más complejo. [OFF-014, slides 27, 33]
* **Capas jerárquicas:** cada capa abstrae a la que está debajo. Los protocolos OSI y TCP/IP ilustran el paso de datos por capas; el estilo ayuda a organizar la complejidad y separar responsabilidades, con un posible costo de rendimiento. [OFF-014, slides 28-33]

### Sistemas distribuidos

Estos estilos organizan la comunicación entre componentes distribuidos. El material resume su objetivo común como desacoplar, escalar y distribuir. [OFF-014, slides 34-47]

* **Broker:** un intermediario recibe y enruta mensajes entre productores y consumidores. Reduce el acoplamiento directo y permite entregar mensajes según disponibilidad. [OFF-014, slides 36-37]
* **Publish–Subscribe:** los productores publican eventos y los consumidores se suscriben; no necesitan conocerse entre sí. La separación favorece el desacoplamiento y la escalabilidad. [OFF-014, slides 39-41]
* **Forwarder–Receiver:** los pares envían y reciben mediante componentes que serializan, transportan y deserializan los mensajes, ocultando los detalles de comunicación. [OFF-014, slide 43]
* **Client–Dispatcher–Server:** un dispatcher elige el servidor que atenderá cada petición y puede distribuir la carga entre servidores disponibles. [OFF-014, slides 45-46]

### Sistemas interactivos y orientados a eventos

**MVC** separa la aplicación en modelo, vista y controlador: el modelo contiene los datos y la lógica principal, la vista presenta información y el controlador procesa las entradas del usuario. El material destaca que permite tener varias vistas sincronizadas del mismo modelo, aunque puede aumentar la coordinación y el acoplamiento entre los tres componentes. [OFF-014, slides 49-51]

En un sistema **basado en eventos**, productores, canales y consumidores intercambian eventos. El procesamiento puede ser individual, en flujo continuo, por correlación de eventos complejos o en línea con latencia mínima. [OFF-014, slides 52-55]

El material también enumera otros estilos, como repositorios y blackboards, máquinas virtuales e intérpretes, sistemas basados en reglas, patrones de servidores web y patrones de concurrencia. [OFF-014, slide 57]

## How it works

La selección empieza por el problema que se quiere resolver: volumen de datos por lotes, flujo continuo o necesidad de organizar una aplicación en capas. Después se comparan las consecuencias del estilo elegido con los atributos de calidad y restricciones importantes del sistema. Por ejemplo, batch simplifica el procesamiento por etapas a costa de latencia; Pipes & Filters admite flujos y transformaciones flexibles, pero exige coordinar filtros; las capas aclaran responsabilidades, aunque pueden afectar el rendimiento. [OFF-014, slides 24, 26-33]

## Relationships

Los estilos concretan decisiones de [arquitectura de software](arquitectura-de-software.md). Las [vistas de arquitectura](documentacion-de-arquitectura.md) describen esas decisiones desde perspectivas distintas, y los [atributos de calidad](atributos-de-calidad.md) ayudan a comparar sus efectos.

## Sources

* [OFF-014, slides 24-57]

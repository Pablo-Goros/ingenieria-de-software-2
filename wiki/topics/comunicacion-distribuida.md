---
title: Estilos de comunicación distribuida
aliases:
- Broker
- Publish-subscribe
- Pub-sub
- Forwarder-receiver
- Client-dispatcher-server
sources:
- OFF-014
- OFF-017
- EXT-001
related:
- procesamiento-de-eventos
- patrones-de-comunicacion-entre-servicios
prerequisites:
- estilos-arquitectonicos
---

# Estilos de comunicación distribuida

## Panorama

Estos estilos organizan cómo se descubren y comunican los miembros de un sistema distribuido. La clase reúne broker, publicación-suscripción, forwarder-receiver y client-dispatcher-server. [OFF-014, p. 34]

## Mecanismos

| Estilo | Responsabilidades |
| --- | --- |
| Broker | Un intermediario coordina la comunicación entre clientes y servidores; proxies ocultan detalles de la distribución. |
| Publicación-suscripción | Los productores publican eventos y los consumidores se suscriben a los que les interesan, sin conocerse entre sí. Un tópico permite distribuir notificaciones. |
| Forwarder-receiver | El emisor serializa y envía; el receptor recibe, deserializa y entrega. Los peers delegan esos detalles de transporte. |
| Client-dispatcher-server | El dispatcher ofrece transparencia de ubicación al localizar el servidor que atenderá la solicitud. |

[OFF-014, pp. 35-45]

## Ejemplos y matices entre fuentes

La clase usa tópicos de sensores como ejemplo de publicación-suscripción. Para client-dispatcher-server presenta tanto el esquema de localización y conexión como balanceadores de carga que distribuyen requests. Es necesario indicar qué responsabilidad cumple el dispatcher del diseño analizado. [OFF-014, pp. 41, 44-46]

Los apuntes externos distinguen el dispatcher que habilita una conexión directa del broker que intermedia. Esa distinción es más estrecha que los ejemplos de balanceo de las diapositivas: no se debe suponer que todo dispatcher tiene idéntico recorrido de mensajes. [EXT-001, «Estilos Arquitectónicos»; OFF-014, pp. 44-46]

Los apuntes describen suscriptores sin recepción retroactiva y brokers como puntos únicos de falla. Esas son condiciones del esquema que desarrollan; las diapositivas definen los roles sin fijar garantías de retención o una implementación redundante. Al aplicar el estilo, esas propiedades deben especificarse. [EXT-001, «Estilos Arquitectónicos»; OFF-014, pp. 35, 38-40]

## Relaciones

Publicación-suscripción puede actuar como canal de una [arquitectura de eventos](procesamiento-de-eventos.md). Los [patrones de comunicación entre servicios](patrones-de-comunicacion-entre-servicios.md) agregan decisiones sobre exposición y manejo de fallas.

## Relevancia para la evaluación

El repaso incluye los cuatro estilos. [OFF-017, p. 5]

## Fuentes

- [OFF-014, pp. 34-47]
- [EXT-001, «Estilos Arquitectónicos»]
- [OFF-017, p. 5]

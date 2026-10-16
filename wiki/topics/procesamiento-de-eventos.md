---
title: Procesamiento de eventos
aliases:
- Event based systems
- Single Event Processing
- Event Stream Processing
- Complex Event Processing
- Online Event Processing
sources:
- OFF-014
- OFF-017
related:
- comunicacion-distribuida
- flujo-de-datos
- microservicios
prerequisites:
- estilos-arquitectonicos
---

# Procesamiento de eventos

## Panorama

Una arquitectura basada en eventos divide el sistema en componentes que se comunican a través de sucesos. Conceptualmente intervienen productores, un canal y consumidores. El canal puede ser una conexión directa, un bus o un mecanismo de publicación-suscripción. [OFF-014, p. 52]

## Modalidades de procesamiento

| Modalidad | Operación | Ejemplo docente |
| --- | --- | --- |
| Single Event Processing | Procesa eventos individuales de manera aislada. | Un sensor dispara una alarma cuando supera un umbral. |
| Event Stream Processing | Transforma, agrega o filtra un flujo continuo. | Analizar clics en línea para producir métricas. |
| Complex Event Processing | Correlaciona múltiples eventos en tiempo y espacio para detectar patrones. | Retiros pequeños junto con una ubicación inusual producen una alerta de fraude. |
| Online Event Processing | Reacciona al suceso en tiempo real o con latencia muy baja. | Actualizar el carrito al recibir un clic del usuario. |

[OFF-014, pp. 53-54; OFF-017, p. 7]

## Beneficios y dificultades

Los subsistemas pueden desarrollarse, escalar y desplegarse de forma independiente. Como contraparte, reproducir fallas, determinar su causa raíz y rastrear operaciones de punta a punta puede resultar complejo; también lo es garantizar el tiempo total de procesamiento. [OFF-014, p. 56]

## Relaciones

[Publicación-suscripción](comunicacion-distribuida.md) ofrece una alternativa de canal. Los [microservicios](microservicios.md) pueden utilizar eventos para colaborar, pero el concepto de evento y la descomposición del sistema son decisiones diferentes. La clase menciona microservicios, IoT y plataformas de streaming como contextos de uso. [OFF-014, pp. 52, 55]

## Relevancia para la evaluación

Las cuatro modalidades están explícitamente incluidas en el repaso. [OFF-017, p. 7]

## Fuentes

- [OFF-014, pp. 52-56]
- [OFF-017, p. 7]

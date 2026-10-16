---
title: Patrones de comunicación entre servicios
aliases:
- API gateway
- Backend for frontend
- BFF
- Circuit breaker
- Timeouts
- Retries
sources:
- OFF-018
- EXT-001
related:
- microservicios
- comunicacion-distribuida
- atributos-de-calidad
prerequisites:
- comunicacion-distribuida
---

# Patrones de comunicación entre servicios

## Panorama

La exposición de servicios y la comunicación distribuida requieren decisiones sobre entrada de solicitudes, adaptación a clientes y tratamiento de fallas. La clase presenta API gateway; los apuntes agregan BFF y circuit breaker. [OFF-018, p. 23; EXT-001, «Patrones a Nivel de Comunicación»]

## API gateway y BFF

El **API gateway** concentra el acceso externo y enruta solicitudes a los servicios internos. Puede aplicar autenticación, logging y otras funciones de borde. Los apuntes amplían sus responsabilidades a composición de APIs, traducción de protocolos, autorización, límites de tráfico, caché y métricas. [OFF-018, p. 23; EXT-001, «Patrones a Nivel de Comunicación»]

Un **Backend for Frontend** ofrece una API adaptada a un cliente específico. La fuente destaca filtrado y composición de respuestas, localización y compatibilidad para evitar que el cliente reciba información innecesaria. Lo presenta como una capa que consulta servicios sin asumir la lógica de negocio de éstos. [EXT-001, «Patrones a Nivel de Comunicación»]

## Timeouts, reintentos y circuit breaker

Los apuntes explican que reintentos encadenados pueden amplificar la carga cuando falla un servicio e impedir su recuperación. El **circuit breaker** corta llamadas tras alcanzar un umbral de fallas y permite pruebas periódicas para comprobar recuperación antes de volver al funcionamiento normal. [EXT-001, «Patrones a Nivel de Comunicación»]

La fuente compara este mecanismo con una protección eléctrica y admite implementarlo en la aplicación o en infraestructura de comunicación. No fija un umbral universal: ese valor es parte del diseño concreto. [EXT-001, «Patrones a Nivel de Comunicación»]

## Relaciones

Estos patrones complementan los [estilos distribuidos](comunicacion-distribuida.md) y el diseño de [microservicios](microservicios.md), en especial sus necesidades de disponibilidad, rendimiento y control de acceso.

## Fuentes

- [OFF-018, p. 23]
- [EXT-001, «Patrones a Nivel de Comunicación»]

---
title: Modelo-vista-controlador
aliases:
- MVC
- Model View Controller
- Sistemas interactivos
sources:
- OFF-014
- OFF-017
related:
- estilos-arquitectonicos
- modelo-cuatro-mas-uno
prerequisites:
- estilos-arquitectonicos
---

# Modelo-vista-controlador

## Panorama

Los estilos para sistemas interactivos separan la funcionalidad principal de las vistas de presentación. MVC divide una aplicación en modelo, vista y controlador. La clase también menciona PAC, MVP y VIPER, pero desarrolla MVC. [OFF-014, pp. 48-49]

## Responsabilidades e interacción

- **Modelo:** contiene información y funcionalidad principal.
- **Vista:** presenta información al usuario.
- **Controlador:** recibe y controla las entradas del usuario. [OFF-014, p. 49]

En el diagrama de la clase, la vista envía eventos de entrada al controlador; este modifica el modelo y puede modificar la vista; el modelo actualiza las vistas. La separación permite múltiples representaciones sincronizadas de un mismo modelo. [OFF-014, pp. 50-51]

## Beneficios y costos

Entre las ventajas se señalan vistas múltiples, sincronización y una base para construir frameworks. Como desventajas se mencionan el número potencialmente alto de actualizaciones y el acoplamiento entre los tres componentes del esquema. La separación de responsabilidades no elimina la necesidad de coordinar sus interacciones. [OFF-014, p. 51]

## Relaciones

MVC es un estilo de [sistema interactivo](estilos-arquitectonicos.md). Para documentarlo con el [modelo 4+1](modelo-cuatro-mas-uno.md), interesa distinguir las responsabilidades funcionales de sus procesos y despliegue; las vistas arquitectónicas responden preguntas distintas. [OFF-014, pp. 14-16, 48-50]

## Relevancia para la evaluación

El repaso de sistemas interactivos incluye el diagrama de MVC. [OFF-017, p. 6]

## Fuentes

- [OFF-014, pp. 14-16, 48-51]
- [OFF-017, p. 6]

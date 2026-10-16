---
title: Persistencia
aliases:
- Persistence
- Archivos
- Serialización
- Almacenamiento persistente
sources:
- OFF-016
- OFF-017
related:
- prevalencia
- bases-de-datos-relacionales
- bases-de-datos-no-relacionales
- escalamiento-de-datos
prerequisites:
- atributos-de-calidad
---

# Persistencia

## Panorama

La persistencia permite que los datos sobrevivan al programa que los genera. Es necesaria porque la memoria es volátil y acotada. Elegir un mecanismo exige considerar rendimiento de acceso y búsqueda, transformación de datos y tolerancia a fallos. [OFF-016, pp. 2-3]

## Alternativas

La clase organiza el problema en archivos, prevalencia y bases de datos. Las bases ofrecen independencia del almacenamiento físico, acceso desde varios programas, recuperación, reglas de integridad y mecanismos de rendimiento y escalabilidad. [OFF-016, pp. 4, 9]

Los **archivos** pueden ser planos —de ancho fijo o variable—, estructurados —como XML o JSON— o binarios. En ancho fijo, cada registro y campo tiene una longitud predefinida. Los archivos indexados facilitan búsquedas por clave a cambio de mantener el índice actualizado. [OFF-016, pp. 5-6]

La **serialización** convierte estructuras u objetos en una secuencia de bytes o texto para almacenarlos o enviarlos. No todo archivo binario es una base de datos ni toda serialización define por sí sola mecanismos de consulta o concurrencia. La clase diferencia archivos, serialización y servicios de base de datos. [OFF-016, pp. 4-6, 9]

## Selección según el uso

El resumen docente asocia archivos con intercambio, configuración, logs y persistencia simple; bases relacionales con transacciones; multidimensionales con análisis; y bases no relacionales con distintos modelos y patrones de acceso. Presenta advertencias sobre concurrencia, integridad y consultas complejas al utilizar archivos como almacenamiento principal. [OFF-016, pp. 23-25]

## Relaciones y evaluación

Los mecanismos específicos se desarrollan en [prevalencia](prevalencia.md), [bases relacionales](bases-de-datos-relacionales.md) y [bases no relacionales](bases-de-datos-no-relacionales.md). El repaso incluye las familias de persistencia. [OFF-017, p. 10]

## Fuentes

- [OFF-016, pp. 2-6, 9, 23-25]
- [OFF-017, p. 10]

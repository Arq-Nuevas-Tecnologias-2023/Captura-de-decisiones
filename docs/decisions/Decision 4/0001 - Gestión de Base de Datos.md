---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
parent: Decisiones de arquitectura
nav_order: 1
title: Iteración 1

# status: "{reemplazado por [ADR-0005](0005-ejemplo.md)}"
# date: {2023-06-19}
# deciders: {Grupo 7 - MATI}
# consulted: {Arquitectos Senior, ArquitectosCognitivos}
# informed: {Grupo 7 - MATI}
---
## Contexto y Problema

Se requiere implementar un componente gestor de base de datos que cumpla con el estilo arquitectónico Event Driven (STREAM) y el patrón ABSTRACT FACTORY. La elección de la tecnología de persistencia es fundamental para garantizar la escalabilidad, rendimiento y confiabilidad del sistema.

## Drivers de Decisión

* RF004: Componente gestor de base de datos

## Opción 1: Base de Datos Relacional

El patrón Publish/Subscribe es una opción adecuada para esta familia, ya que permite la difusión eficiente de mensajes a múltiples destinatarios. En este patrón, los componentes que actúan como editores publican mensajes en un canal de comunicación, mientras que los suscriptores se suscriben a los canales relevantes para recibir los mensajes pertinentes. Esto garantiza un acoplamiento mínimo entre los componentes y facilita la escalabilidad y la distribución.


## Pros y Contras de las Opciones

### Opción 1: Base de Datos Relacional

* Bueno, porque cuenta con una amplia adopción y una comunidad activa que brinda soporte y recursos.
* Bueno, porque ofrece soporte para transacciones ACID, garantizando la integridad de los datos.
* Bueno, porque permite realizar consultas SQL complejas para obtener información específica de manera eficiente.
* Bueno, porque se puede aplicar el patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas.
* Malo, porque presenta un rendimiento ligeramente inferior en comparación con algunas tecnologías NoSQL, especialmente en escenarios con alta concurrencia o grandes volúmenes de datos.
* Malo, porque el modelado de datos puede ser más complejo debido a las restricciones de esquema y relaciones.

## Más Información



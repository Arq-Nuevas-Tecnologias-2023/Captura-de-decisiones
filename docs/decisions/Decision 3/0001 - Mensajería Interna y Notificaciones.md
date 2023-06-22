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

Esta decisión se refiere a la implementación de la Mensajería Interna y Notificaciones en el sistema. El problema radica en cómo diseñar y estructurar adecuadamente esta funcionalidad para garantizar la entrega confiable de mensajes internos y notificaciones a los usuarios del sistema. Se ha decidido utilizar el estilo arquitectónico basado en Event-Driven (Eventos) para la implementación de la Mensajería Interna y Notificaciones. Este estilo permite una comunicación asíncrona y desacoplada entre los diferentes componentes involucrados, lo que facilita la escalabilidad y la extensibilidad del sistema.


## Drivers de Decisión

* RF003: Componente de mensajería interna y notificaciones

## Opción 1: Event-Driven con patrón Publish/Subscribe

El patrón Publish/Subscribe es una opción adecuada para esta familia, ya que permite la difusión eficiente de mensajes a múltiples destinatarios. En este patrón, los componentes que actúan como editores publican mensajes en un canal de comunicación, mientras que los suscriptores se suscriben a los canales relevantes para recibir los mensajes pertinentes. Esto garantiza un acoplamiento mínimo entre los componentes y facilita la escalabilidad y la distribución.


## Decisión

La opción elegida es la **Opción 1: Event-Driven con patrón Publish/Subscribe**. Este patrón proporciona un enfoque desacoplado y escalable para la difusión de mensajes, lo cual es beneficioso para el sistema en general.

## Consecuencias

La elección del patrón Publish/Subscribe para la implementación de la Mensajería Interna y Notificaciones tiene las siguientes consecuencias:

* Bueno, porque permite la difusión eficiente de mensajes a múltiples destinatarios.
* Bueno, porque desacopla los componentes, lo que facilita la escalabilidad y la extensibilidad.
* Malo, porque puede generar una mayor complejidad en la gestión de los canales de comunicación y las suscripciones.
* Requiere una implementación adicional para garantizar la entrega confiable de mensajes.

## Confirmación

La implementación y cumplimiento de esta decisión de diseño se confirmará a través de revisiones de arquitectura y pruebas de integración. Se revisará y evaluará el rendimiento, la escalabilidad y la confiabilidad del sistema para garantizar que la implementación del patrón Publish/Subscribe sea efectiva y satisfaga los requisitos funcionales.

## Pros y Contras de las Opciones

### Opción 1: Event-Driven con patrón Publish/Subscribe

* Bueno, porque permite la difusión eficiente de mensajes a múltiples destinatarios.
* Bueno, porque desacopla los componentes, lo que facilita la escalabilidad y la extensibilidad.
* Neutral, porque requiere una implementación adicional para garantizar la entrega confiable de mensajes.
* Malo, porque puede generar una mayor complejidad en la gestión de los canales de comunicación y las suscripciones.

## Más Información

- [Artículo sobre el patrón Publish/Subscribe](https://learn.microsoft.com/en-us/azure/architecture/patterns/publisher-subscriber)


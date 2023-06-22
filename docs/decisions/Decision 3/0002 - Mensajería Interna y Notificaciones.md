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

## Opción 2: Patrón Request/Response

El patrón Request/Response es otra opción viable para la implementación de la Mensajería Interna y Notificaciones. En este patrón, los componentes envían solicitudes de mensajes a un componente centralizado responsable de la entrega de los mensajes. El componente centralizado puede realizar la entrega directa o almacenar y enviar mensajes en cola para garantizar la entrega confiable.

## Confirmación

La implementación y cumplimiento de esta decisión de diseño se confirmará a través de revisiones de arquitectura y pruebas de integración. Se revisará y evaluará el rendimiento, la escalabilidad y la confiabilidad del sistema para garantizar que la implementación del patrón Publish/Subscribe sea efectiva y satisfaga los requisitos funcionales.

## Pros y Contras de las Opciones

### Opción 2: Patrón Request/Response

* Bueno, porque permite un enfoque centralizado para la gestión y entrega de mensajes.
* Neutral, porque facilita el control y la supervisión de la entrega de mensajes.
* Malo, porque puede generar un mayor acoplamiento entre los componentes.
* Malo, porque puede ser menos escalable en comparación con el patrón Publish/Subscribe.

## Más Información

- [Artículo sobre el patrón Publish/Subscribe](https://learn.microsoft.com/en-us/azure/architecture/patterns/publisher-subscriber)


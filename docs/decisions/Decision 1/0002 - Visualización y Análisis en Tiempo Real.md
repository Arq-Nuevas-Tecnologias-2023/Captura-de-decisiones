---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
Estado: Rechazado
title: Visualización y Análisis en Tiempo Real
Decisión: 002
date: 2023-06-19
deciders: {Grupo 7 - MATI}
consulted: {Arquitectos Senior, ArquitectosCognitivos}

# status: "{reemplazado por [ADR-0005](0005-ejemplo.md)}"
# date: {2023-06-19}
# deciders: {Grupo 7 - MATI}
# consulted: {Arquitectos Senior, ArquitectosCognitivos}
# informed: {Grupo 7 - MATI}
---
## Contexto y Problema

Esta decisión se enfoca en la visualización y análisis en tiempo real de los procesos productivos, órdenes de trabajo y sensores IoT tipo Cockpit. El problema es cómo implementar esta funcionalidad de manera eficiente y escalable utilizando una arquitectura Event-Driven.

## Drivers de Decisión

* RF001-1: Componente de visualización de analítica para procesos productivos
* RF001-2: Componente de visualización de analítica para órdenes de trabajo
* RF001-3: Componente de visualización de sensores de los componentes IoT tipo Cockpit

## Opción 2: Event-Driven con patrón Publish/Subscribe y Chain of Responsibility

Utilizar un enfoque basado en Event-Driven con los patrones de diseño Publish/Subscribe y Chain of Responsibility para implementar la visualización y análisis en tiempo real.

### Detalles de la Opción 2

Esta opción implica diseñar una arquitectura basada en eventos, donde los diferentes componentes publican eventos relacionados con los procesos productivos (RF001-1), órdenes de trabajo (RF001-2) y sensores IoT tipo Cockpit (RF001-3). Los componentes de visualización se suscriben a los eventos relevantes y utilizan el patrón Chain of Responsibility para procesar los eventos en una cadena de responsabilidad.

Ventajas de la Opción 2:

* Proporciona una mayor simplicidad al utilizar solo los patrones de Publish/Subscribe y Chain of Responsibility.
* Permite una fácil adición de nuevos componentes de visualización de analítica para los diferentes requisitos funcionales.

Desventajas de la Opción 2:

* Puede limitar la extensibilidad y flexibilidad al no permitir la creación dinámica de componentes de visualización.

## Consecuencias

Las consecuencias de esta decisión son:

* Bueno, porque permite una arquitectura modular y escalable para la visualización y análisis en tiempo real.
* Bueno, porque facilita la integración de nuevos componentes de visualización en el futuro.
* Malo, porque puede aumentar la complejidad debido a la implementación de los patrones adicionales.

## Pros y Contras de las Opciones

### Opción 2: Event-Driven con patrón Publish/Subscribe y Chain of Responsibility

Esta opción proporciona una mayor simplicidad al utilizar solo los patrones de Publish/Subscribe y Chain of Responsibility.

* Bueno, porque proporciona una mayor simplicidad.
* Bueno, porque permite una fácil adición de nuevos componentes de visualización de analítica para los diferentes requisitos funcionales.
* Neutral, porque puede limitar la extensibilidad y flexibilidad al no permitir la creación dinámica de componentes de visualización.

## Más Información

- [Documentación de Publisher-Subscriber](https://learn.microsoft.com/en-us/azure/architecture/patterns/publisher-subscriber)
-[Documentación Chain of Responsibility](https://refactoring.guru/design-patterns/chain-of-responsibility)
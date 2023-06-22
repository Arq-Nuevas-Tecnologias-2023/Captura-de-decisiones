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

Esta decisión se enfoca en la visualización y análisis en tiempo real de los procesos productivos, órdenes de trabajo y sensores IoT tipo Cockpit. El problema es cómo implementar esta funcionalidad de manera eficiente y escalable utilizando una arquitectura Event-Driven.

## Drivers de Decisión

* RF001-1: Componente de visualización de analítica para procesos productivos
* RF001-2: Componente de visualización de analítica para órdenes de trabajo
* RF001-3: Componente de visualización de sensores de los componentes IoT tipo Cockpit

## Opción 1: Event-Driven con patrón Publish/Subscribe y Abstract Factory

Utilizar un enfoque basado en Event-Driven con los patrones de diseño Publish/Subscribe y Abstract Factory para implementar la visualización y análisis en tiempo real de la familia 1.

### Detalles de la Opción 1

Esta opción implica diseñar una arquitectura basada en eventos, donde los diferentes componentes publican eventos relacionados con los procesos productivos (RF001-1), órdenes de trabajo (RF001-2) y sensores IoT tipo Cockpit (RF001-3). Los componentes de visualización se suscriben a los eventos relevantes y utilizan una Abstract Factory para crear instancias de los diferentes tipos de componentes de visualización.

Ventajas de la Opción 1:

* Permite una arquitectura modular y escalable.
* Facilita la integración de nuevos componentes de visualización en el futuro.
* Proporciona flexibilidad y extensibilidad al permitir la creación de componentes de visualización de manera dinámica a través de la Abstract Factory.

Desventajas de la Opción 1:

* Puede aumentar la complejidad debido a la necesidad de implementar los patrones adicionales.
* Requiere un mayor esfuerzo de desarrollo inicial para establecer la infraestructura del Event-Driven y los patrones de diseño.

## Decisión

La opción elegida es la **Opción 1: Event-Driven con patrón Publish/Subscribe y Abstract Factory**. Esta opción se seleccionó debido a su capacidad de proporcionar una arquitectura modular, escalable y flexible, permitiendo la creación dinámica de componentes de visualización a través de la Abstract Factory. Aunque requiere un mayor esfuerzo de desarrollo inicial, creemos que los beneficios a largo plazo superan las desventajas.

## Consecuencias

Las consecuencias de esta decisión son:

* Bueno, porque permite una arquitectura modular y escalable para la visualización y análisis en tiempo real de la familia 1.
* Bueno, porque facilita la integración de nuevos componentes de visualización en el futuro.
* Malo, porque puede aumentar la complejidad debido a la implementación de los patrones adicionales.

## Confirmación

La implementación de esta decisión será confirmada mediante una revisión de diseño por parte del equipo de arquitectura y una revisión de código durante el desarrollo. Además, se realizarán pruebas y validaciones para garantizar que la arquitectura Event-Driven y los patrones de diseño se implementen correctamente.

## Pros y Contras de las Opciones

### Opción 1: Event-Driven con patrón Publish/Subscribe y Abstract Factory

* Bueno, porque permite una arquitectura modular y escalable.
* Bueno, porque facilita la integración de nuevos componentes de visualización en el futuro.
* Neutral, porque puede proporcionar flexibilidad y extensibilidad al permitir la creación dinámica de componentes de visualización.
* Malo, porque puede aumentar la complejidad debido a la implementación de los patrones adicionales.

## Más Información

{NNNN}



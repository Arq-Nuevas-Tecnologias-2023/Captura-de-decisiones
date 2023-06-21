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

## Context and Problem Statement

El contexto de esta opción es proporcionar capacidades de visualización y análisis en tiempo real para procesos productivos, órdenes de trabajo y sensores de componentes IoT tipo Cockpit. El problema radica en cómo implementar esta funcionalidad de manera efectiva y eficiente.

## Decision Drivers

* Componente de visualización de analítica para procesos productivos
* Componente de visualización de analítica para órdenes de trabajo
* Componente de visualización de sensores de los componentes IoT tipo Cockpit

## Considered Options

* Implementar una solución basada en el patrón Publish/Subscribe y utilizar Abstract Factories para la creación de componentes de visualización.
* Aplicar el patrón Observer y el patrón Factory Method para la implementación de la visualización en tiempo real.
* Utilizar el patrón Command y el patrón Singleton para la gestión de las interacciones y la comunicación en tiempo real.
* Emplear el patrón MVC (Modelo-Vista-Controlador) para estructurar la arquitectura de visualización y análisis en tiempo real.

## Decision Outcome

Opción 1: Implementar una solución basada en el patrón Publish/Subscribe y utilizar Abstract Factories para la creación de componentes de visualización. Esto permitirá una arquitectura flexible y escalable para la visualización y análisis en tiempo real.

### Consequences

* Bueno, porque el patrón Publish/Subscribe permite una comunicación eficiente entre los diferentes componentes de visualización y los datos en tiempo real.
* Bueno, porque el uso de Abstract Factories facilita la creación y gestión de los componentes de visualización de forma coherente.
* Malo, porque se requerirá un esfuerzo adicional para diseñar e implementar la infraestructura de Publicar/Suscribir y las Abstract Factories.

## Pros and Cons of the Options

### Implementar una solución basada en el patrón Publish/Subscribe y utilizar Abstract Factories para la creación de componentes de visualización

* Bueno, porque el patrón Publish/Subscribe permite una comunicación desacoplada entre los componentes de visualización y los productores de datos en tiempo real.
* Bueno, porque el uso de Abstract Factories facilita la creación y gestión de los componentes de visualización de forma coherente y extensible.
* Neutral, porque la implementación del patrón Publish/Subscribe puede requerir un mayor tiempo y esfuerzo en comparación con otras soluciones.
* Malo, porque la gestión de los mensajes publicados y la sincronización de la visualización en tiempo real pueden ser complejas.

### Aplicar el patrón Observer y el patrón Factory Method para la implementación de la visualización en tiempo real

Esta opción implica utilizar el patrón Observer para establecer una comunicación directa entre los componentes de visualización y los productores de datos en tiempo real. Además, se utilizará el patrón Factory Method para la creación de los componentes de visualización. Algunos pros y contras de esta opción son:

* Bueno, porque el patrón Observer permite una comunicación directa y simplificada entre los componentes de visualización y los productores de datos en tiempo real.
* Bueno, porque el uso del patrón Factory Method facilita la creación y gestión de los componentes de visualización de forma flexible y extensible.
* Neutral, porque la implementación del patrón Observer puede requerir una gestión más cuidadosa de las suscripciones y notificaciones.
* Malo, porque el enfoque directo de comunicación puede resultar en un acoplamiento más estrecho entre los componentes de visualización y los productores de datos en tiempo real.


### Utilizar el patrón Command y el patrón Singleton para la gestión de las interacciones y la comunicación en tiempo real

Esta opción implica utilizar el patrón Command para gestionar las interacciones y la comunicación entre los componentes de visualización y los productores de datos en tiempo real. Además, se utilizará el patrón Singleton para garantizar la existencia de una única instancia de los componentes de gestión. Algunos pros y contras de esta opción son:

* Bueno, porque el patrón Command proporciona una estructura organizada para gestionar las interacciones y la comunicación en tiempo real.
* Bueno, porque el uso del patrón Singleton garantiza la existencia de una única instancia de los componentes de gestión, lo que puede facilitar la coordinación y evitar problemas de concurrencia.
* Malo, porque el patrón Command puede introducir una capa adicional de complejidad en la gestión de las interacciones y la comunicación.
* Malo, porque el uso del patrón Singleton puede dificultar la prueba y la modularidad de los componentes.


### Emplear el patrón MVC (Modelo-Vista-Controlador) para estructurar la arquitectura de visualización y análisis en tiempo real

Esta opción implica utilizar el patrón MVC para estructurar la arquitectura de visualización y análisis en tiempo real. El Modelo representa los datos en tiempo real, la Vista proporciona la interfaz de usuario para visualizar los datos y el Controlador maneja las interacciones y la lógica de negocio. Algunos pros y contras de esta opción son:

* Bueno, porque el patrón MVC proporciona una separación clara de responsabilidades y promueve la modularidad y reutilización de código.
* Bueno, porque el uso del patrón MVC facilita la evolución y el mantenimiento del sistema, ya que los cambios en una capa no afectan directamente a las demás capas.
* Neutral, porque la implementación del patrón MVC puede requerir un esfuerzo adicional en comparación con enfoques más simples.
* Malo, porque el patrón MVC puede introducir una mayor complejidad en el diseño y la estructura del sistema.

## More Information

    Enlaces a recursos adicionales relevantes, documentación técnica, colaboración con otros ADR, etc.

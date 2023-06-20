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
## Contexto y Problema Planteado

En el desarrollo de nuestro proyecto de arquitectura (Event Driven - STREAM), nos encontramos con la necesidad de implementar patrones de diseño para abordar los siguientes requerimientos funcionales para nuestra primera ITERACIÓN:

- RF001: Centro de notificaciones
- RF001-1: Componente de visualización de analítica para procesos productivos
- RF001-2: Componente de visualización de analítica para ordenes de trabajo
- RF001-3: Componente de visualización sensores de los componentes IOT tipo Cockpit.
- RF002: Módulo de Ordenes de Trabajo
- RF004: Componente gestor de base de datos
- RF005: Sensores IoT
- RF005-1: Sensores familia A (Sensores monolíticos)

## Factores Determinantes de la Decisión

* Monitoreo y análisis en tiempo real de los procesos de producción y las órdenes de trabajo.
* Recolección y procesamiento eficiente de datos de los sensores.
* Notificaciones y alertas oportunas para los operadores.

## Opciones Consideradas

Opción 1: Patrones Publish/Subscribe, Abstract Factory y Chain of Responsibility

- Utilizar el patrón de diseño Publish/Subscribe para la publicación y suscripción de eventos.
- Aplicar el patrón de diseño Abstract Factory para la creación de instancias de diferentes tipos de objetos.
- Implementar el patrón de diseño Chain of Responsibility para gestionar solicitudes de manera secuencial.

Opción 2: Patrones Observer, Strategy y Abstract Factory

- Emplear el patrón de diseño Observer para la publicación y suscripción de eventos.
- Aplicar el patrón de diseño Strategy para proporcionar una manera flexible de crear familias de objetos relacionados.
- Utilizar el patrón de diseño Abstract Factory para la creación de instancias de diferentes tipos de objetos.

## Resultado de la Decisión

Opción elegida: Opción 1 - Implementar los patrones de comportamiento Publicar/Suscribir, Abstract Factories y Chain of Responsibility para la visualización en tiempo real de análisis, el monitoreo de sensores y las notificaciones.

### Consecuencias

* Bueno, porque los patrones Publicar/Suscribir, Abstract Factories y Strategy permiten actualizaciones y visualización en tiempo real de los análisis de los procesos de producción y las órdenes de trabajo.
* Bueno, porque los patrones permiten la recolección, procesamiento y distribución eficiente de datos de los sensores a los componentes relevantes.
* Bueno, porque las notificaciones y alertas pueden ser fácilmente enviadas a los operadores suscritos, manteniéndolos informados sobre eventos críticos.
* Malo, porque implementar los patrones puede requerir infraestructura adicional y esfuerzo de desarrollo.
* Malo, porque la complejidad del sistema puede aumentar debido a la introducción de los patrones.

## Pros y Contras de las Opciones

### Opción 1: Implementar los patrones de comportamiento Publicar/Suscribir, Abstract Factories y Chain of Responsibility

* Bueno, porque permite actualizaciones y visualización en tiempo real.
* Bueno, porque permite la recolección, procesamiento y distribución eficiente de datos de los sensores.
* Bueno, porque las notificaciones y alertas pueden ser fácilmente enviadas a los operadores suscritos.
* Malo, porque puede requerir infraestructura adicional y esfuerzo de desarrollo.
* Malo, porque puede introducir complejidad al sistema.

### Opción 2: Utilizar el patrón Observer, Strategy y Abstract Factory

* Bueno, porque permite una estructura flexible y desacoplada para la gestión de eventos y notificaciones.
* Bueno, porque permite la actualización y propagación de información a los observadores interesados.
* Malo, porque puede requerir un diseño más elaborado para gestionar la suscripción y notificación de eventos.
* Malo, porque puede ser menos eficiente en términos de procesamiento y distribución de datos en comparación con Publicar/Suscribir.

### Decisión Justificada

La opción 1, de implementar los patrones de comportamiento Publicar/Suscribir, Abstract Factories y Chain of Responsibility, es elegida debido a su capacidad para proporcionar actualizaciones en tiempo real, recolectar y procesar eficientemente datos de sensores, y enviar notificaciones y alertas a los operadores suscritos. Aunque la implementación puede requerir esfuerzo adicional y aumentar la complejidad del sistema, sus beneficios superan los inconvenientes identificados.

## Más Información

Las discusiones adicionales y la documentación sobre los detalles de implementación y consideraciones arquitectónicas se capturarán en los documentos de diseño y en los repositorios de código correspondientes.

---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
Estado: Aprobado
title: Administración de Órdenes de Trabajo
Decisión: 001
date: 2023-06-19
deciders: {Grupo 7 - MATI}
consulted: {Arquitectos Senior, ArquitectosCognitivos}
---
## Contexto y Problema

El módulo de Ordenes de Trabajo es un componente crítico del sistema y es responsable de gestionar las órdenes de trabajo de los procesos productivos. Se requiere encontrar una solución que permita manejar eficientemente las órdenes de trabajo, garantizando la escalabilidad y la modularidad del sistema.

## Drivers de Decisión

* RF002: Módulo de Órdenes de Trabajo

## Opción 1: Enfoque basado en eventos y patrón Abstract Factory

   Esta opción propone utilizar un enfoque basado en eventos, donde se utilizará el patrón Abstract Factory para la creación de los objetos relacionados con las órdenes de trabajo. Cada tipo de proceso productivo tendrá su propia implementación de la Abstract Factory, lo que permitirá la personalización y adaptación del flujo de trabajo según las necesidades específicas.

### Detalles de la Opción 1

   - Se utilizará un sistema de eventos para la comunicación entre los componentes relacionados con las órdenes de trabajo.
   - Se implementará una Abstract Factory que permita la creación de objetos relacionados con las órdenes de trabajo.
   - Cada proceso productivo tendrá su propia implementación de la Abstract Factory, lo que permitirá la personalización del flujo de trabajo.
   - Los eventos se utilizarán para comunicar los cambios de estado de las órdenes de trabajo y desencadenar acciones en los componentes relevantes.

## Decisión

Opción elegida: **Opción 1: Enfoque basado en eventos y patrón Abstract Factory**, ya que esta opción ofrece una mayor flexibilidad y personalización del flujo de trabajo de las órdenes de trabajo al utilizar el patrón Abstract Factory. El enfoque basado en eventos facilita la comunicación y la sincronización entre los componentes relacionados con las órdenes de trabajo. La modularidad del sistema se mantiene mediante la separación de las implementaciones de las Abstract Factory para cada proceso productivo.

## Consecuencias

Las consecuencias de esta decisión son:


* Bueno, porque permite una mayor flexibilidad y personalización del flujo de trabajo de las órdenes de trabajo.
* Bueno, porque facilita la comunicación y sincronización entre los componentes mediante eventos.
* Bueno, porque mantiene la modularidad del sistema al separar las implementaciones de las Abstract Factory para cada proceso productivo.
* Malo, porque requiere un diseño y una implementación más cuidadosa debido a la utilización de eventos y Abstract Factory.
* Malo, porque puede tener una mayor complejidad en comparación con enfoques más simples.


## Confirmación

La implementación y cumplimiento de esta decisión se confirmará mediante una revisión del diseño y la implementación del módulo de Ordenes de Trabajo, así como pruebas de integración y revisión de arquitectura.

## Pros y Contras de las Opciones

### Opción 1: Enfoque basado en eventos y patrón Abstract Factory

* Bueno, porque permite una mayor flexibilidad y personalización del flujo de trabajo de las órdenes de trabajo.
* Bueno, porque facilita la comunicación y sincronización entre los componentes mediante eventos.
* Neutral, porque se necesita un diseño y una implementación más cuidadosa debido a la utilización de eventos y Abstract Factory.
* Malo, porque puede tener una mayor complejidad en comparación con enfoques más simples.

## Más Información

-[Abstract Factory Pattern](https://www.javatpoint.com/abstract-factory-pattern){}





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

La organización requiere un módulo de administración de órdenes de trabajo para gestionar eficientemente las tareas relacionadas con los procesos productivos. La falta de un sistema centralizado ha generado ineficiencias y dificultades para realizar un seguimiento adecuado de las órdenes de trabajo. Se busca una solución que permita el registro, asignación, seguimiento y cierre de las órdenes de trabajo de manera eficiente.

## Decision Drivers

* La necesidad de tener un control total sobre el desarrollo y personalización del módulo de administración de órdenes de trabajo.
* La adaptación precisa a los requisitos específicos de la organización.
* La disponibilidad de recursos internos capacitados y familiarizados con los procesos y necesidades de la organización.

## Considered Options

* **Opción 1**: Desarrollar internamente un módulo personalizado para la administración de órdenes de trabajo.
* **Opción 2**: Comprar un software de administración de órdenes de trabajo ya existente en el mercado.

## Decision Outcome

La opción seleccionada es **Opción 1**. Esta opción se elige debido a las siguientes justificaciones:

* El desarrollo interno del módulo de administración de órdenes de trabajo nos brindará un control total sobre el proceso de desarrollo y personalización, permitiéndonos adaptarlo precisamente a nuestros requisitos específicos.
* Al utilizar nuestros recursos internos capacitados y familiarizados con los procesos y necesidades de la organización, podemos asegurar una mejor comprensión de los requisitos y una implementación más eficiente.
* El desarrollo interno también nos brindará la flexibilidad de realizar modificaciones y mejoras continuas según las necesidades cambiantes de la organización, sin depender de un proveedor externo.


### Consequences

Al elegir la opción 1, se esperan las siguientes consecuencias:

* **Ventajas**:
  * Control total sobre el desarrollo y personalización del módulo.
  * Adaptación precisa a los requisitos específicos de la organización.

* **Desventajas**:
  * Mayor tiempo y recursos necesarios para el desarrollo.
  * Mayor esfuerzo requerido para las pruebas y mantenimiento continuo.

## Pros and Cons of the Options

### Opción 1: Desarrollo interno de un módulo de administración de órdenes de trabajo

* **Ventajas**:
  * Control total sobre el desarrollo y personalización del módulo.
  * Adaptación precisa a los requisitos específicos de la organización.

* **Desventajas**:
  * Mayor tiempo y recursos necesarios para el desarrollo.
  * Mayor esfuerzo requerido para las pruebas y mantenimiento continuo.

### Opción 2: Adquisición de un software de administración de órdenes de trabajo

* **Ventajas**:
  * Implementación más rápida y eficiente.
  * Acceso a funcionalidades avanzadas y actualizaciones regulares proporcionadas por el proveedor del software.
  * Soporte técnico disponible.

* **Desventajas**:
  * Posibles costos asociados con la adquisición y personalización del software.
  * Dependencia de un proveedor externo para soporte y actualizaciones.
## More Information

    Enlaces a recursos adicionales relevantes, documentación técnica, colaboración con otros ADR, etc.

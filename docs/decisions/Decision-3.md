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

En el sistema, es necesario contar con un componente de mensajería interna y notificaciones que permita la comunicación entre los diferentes usuarios y proporcione avisos y alertas relevantes. El objetivo es garantizar una comunicación eficiente y oportuna, así como una adecuada gestión de las notificaciones para mantener a los usuarios informados sobre eventos importantes.

## Decision Drivers

* Componente de mensajería interna y notificaciones.

## Considered Options

* **Opción 1**: Implementar el componente de mensajería interna y notificaciones utilizando el patrón Publish/Subscribe en un entorno basado en Event Driven.
* **Opción 2**: Utilizar un enfoque basado en solicitudes y respuestas para la mensajería interna y notificaciones, sin aplicar el patrón Publish/Subscribe.

## Decision Outcome

La opción seleccionada es **Opción 1**. Esta opción se elige debido a las siguientes justificaciones:

* El patrón Publish/Subscribe es apropiado para el estilo de arquitectura Event Driven, ya que permite la distribución eficiente de mensajes y notificaciones a los suscriptores interesados.
* El enfoque Publish/Subscribe facilita la escalabilidad del sistema, ya que los componentes de mensajería y notificaciones pueden publicar eventos de manera independiente y los suscriptores pueden consumir solo los eventos relevantes para ellos.
* El uso de Event Driven garantiza que los eventos y notificaciones sean gestionados de manera asincrónica y en tiempo real, lo que mejora la eficiencia y la capacidad de respuesta del sistema.
* Este enfoque permite una fácil extensibilidad en el futuro, ya que se pueden agregar nuevos suscriptores y publicadores de eventos según sea necesario sin afectar significativamente la arquitectura existente.


### Consequences

Al elegir la opción 1, se esperan las siguientes consecuencias:

* **Ventajas**:
  * Permite una comunicación eficiente y oportuna entre los usuarios del sistema a través del componente de mensajería interna y notificaciones.
  * Proporciona una gestión efectiva de las notificaciones y alertas relevantes para mantener a los usuarios informados sobre   eventos importantes.
  * Facilita la escalabilidad del sistema al permitir la distribución eficiente de mensajes y notificaciones a los suscriptores interesados.
  * Mejora la eficiencia y la capacidad de respuesta del sistema al gestionar los eventos y notificaciones de manera asincrónica y en tiempo real.

* **Desventajas**:
  * Requiere un diseño y desarrollo adecuados para implementar correctamente el patrón Publish/Subscribe en el componente de mensajería interna y notificaciones.
  * Puede ser necesario proporcionar mecanismos de gestión y monitoreo adicionales para garantizar el correcto funcionamiento del sistema basado en Event Driven.

## Pros and Cons of the Options

### Opción 1:  Implementar el componente de mensajería interna y notificaciones utilizando el patrón Publish/Subscribe en un entorno basado en Event Driven.

* **Ventajas**:
  * Alineado con el estilo de arquitectura Event Driven, lo que garantiza un flujo eficiente y asincrónico de mensajes y notificaciones.
  * Permite la distribución eficiente de mensajes y notificaciones a los suscriptores interesados.
  * Mejora la escalabilidad del sistema al permitir la adición de nuevos suscriptores y publicadores de eventos sin afectar la arquitectura existente.
  * Facilita la extensibilidad y el mantenimiento del sistema en el futuro.

* **Desventajas**:
  * Requiere un diseño y desarrollo adecuados para implementar correctamente el patrón Publish/Subscribe.
  * Puede requerir mecanismos de gestión y monitoreo adicionales para garantizar el correcto funcionamiento del sistema basado en Event Driven.
### Opción 2: Utilizar un enfoque basado en solicitudes y respuestas para la mensajería interna y notificaciones, sin aplicar el patrón Publish/Subscribe.

* **Ventajas**:
  * Puede ser más sencillo de implementar en comparación con el patrón Publish/Subscribe.
  * No requiere la infraestructura adicional necesaria para soportar el patrón Publish/Subscribe.

* **Desventajas**:
  * No aprovecha las ventajas del estilo de arquitectura Event Driven, como el flujo eficiente y asincrónico de mensajes y notificaciones.
  * Puede ser menos escalable y flexible en comparación con el enfoque basado en el patrón Publish/Subscribe.
  * Puede dificultar la extensibilidad y el mantenimiento del sistema en el futuro.

## More Information

    Enlaces a recursos adicionales relevantes, documentación técnica, colaboración con otros ADR, etc.

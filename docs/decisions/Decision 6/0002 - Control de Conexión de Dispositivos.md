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


El sistema requiere un módulo de Control de Conexión de Dispositivos para gestionar y supervisar las conexiones de los dispositivos IoT. Se deben considerar los siguientes aspectos:

- El módulo debe ser capaz de recibir información sobre el estado de conexión de los dispositivos.
- Se deben tomar decisiones sobre las acciones a seguir en caso de desconexión o fallos de conexión.
- Se deben implementar mecanismos para garantizar la seguridad de las conexiones.


## Drivers de Decisión

* RF008: Control de conexión de Dispositivos

## Opción 2: Uso de MQTT para control de conexión

- Utilizar el protocolo MQTT (Message Queuing Telemetry Transport) para gestionar las conexiones de los dispositivos IoT.
- Permitir una comunicación asincrónica y eficiente entre el servidor y los dispositivos.
- Proporcionar un mecanismo de suscripción y publicación de mensajes.
- Implementar estrategias de manejo de desconexiones y calidad de servicio (QoS) configurable.


## Decisión

La opción elegida es la **Opción 2: Uso de MQTT para control de conexión**. Debido a las siguientes justificaciones:

- MQTT es un protocolo ligero y eficiente diseñado específicamente para el Internet de las Cosas (IoT).
- Proporciona un modelo de comunicación asincrónica, lo que permite una mayor flexibilidad en el manejo de conexiones y mensajes.
- MQTT admite mecanismos avanzados de calidad de servicio (QoS), lo que permite garantizar la entrega de mensajes incluso en entornos de red inestables.
- El enfoque de publicación/suscripción de MQTT se adapta bien al estilo de arquitectura Event Driven y al patrón Strategy.


## Consecuencias

* Bueno, porque el uso de MQTT garantiza una comunicación eficiente y confiable entre el servidor y los dispositivos.
* Bueno, porque MQTT permite una fácil integración con otros componentes y servicios del sistema.
* Bueno, porque MQTT proporciona mecanismos avanzados de calidad de servicio (QoS) para garantizar la entrega de mensajes en entornos de red inestables.
* Bueno, porque el enfoque de publicación/suscripción de MQTT facilita la implementación de estrategias de control de conexión flexibles.
* Bueno, porque es de código libre y gratuito.
* Neutral, porque la implementación y configuración de un broker MQTT puede requerir recursos adicionales.
* Neutral, porque el uso de MQTT puede requerir una curva de aprendizaje inicial para familiarizarse con el protocolo y las mejores prácticas de uso.


## Confirmación

La implementación y el cumplimiento de este ADR se confirmarán a través de un proceso de revisión por parte del equipo de aequitecturay se se realizarán pruebas de integración para garantizar el correcto funcionamiento del módulo de Control de Conexión de Dispositivos basado en MQTT.



## Más Información

- [Documentación de MQTT](https://mqtt.org/)
- [Comparativa entre WebSocket y MQTT](https://www.ibm.com/support/knowledgecenter/en/SSMQ79_9.1.0/com.ibm.itsm.sysadmin.doc/c_mqtt_websockets.html)

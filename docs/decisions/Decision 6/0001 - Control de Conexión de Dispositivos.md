---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
Estado: Rechazado
title: Control de Conexión de Dispositivos
Decisión: 001
date: 2023-06-19
deciders: {Grupo 7 - MATI}
consulted: {Arquitectos Senior, Arquitectos Cognitivos}
---
## Contexto y Problema


El sistema requiere un módulo de Control de Conexión de Dispositivos para gestionar y supervisar las conexiones de los dispositivos IoT. Se deben considerar los siguientes aspectos:

- El módulo debe ser capaz de recibir información sobre el estado de conexión de los dispositivos.
- Se deben tomar decisiones sobre las acciones a seguir en caso de desconexión o fallos de conexión.
- Se deben implementar mecanismos para garantizar la seguridad de las conexiones.


## Drivers de Decisión

* RF008: Control de conexión de Dispositivos

## Opción 1: Uso de WebSocket para control de conexión

- Utilizar la tecnología de WebSocket para establecer y supervisar las conexiones de los dispositivos IoT.
- Permitir una comunicación bidireccional y en tiempo real entre el servidor y los dispositivos.
- Proporcionar una alta escalabilidad y eficiencia en la transmisión de datos.
- Implementar estrategias de reconexión automática en caso de desconexiones.


## Más Información

- [Comparativa entre WebSocket y MQTT](https://www.ibm.com/support/knowledgecenter/en/SSMQ79_9.1.0/com.ibm.itsm.sysadmin.doc/c_mqtt_websockets.html)

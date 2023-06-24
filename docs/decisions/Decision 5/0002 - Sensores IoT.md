---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
Estado: Aprobadoo
title: Sensores IoT
Decisión: 002
date: 2023-06-19
deciders: {Grupo 7 - MATI}
consulted: {Arquitectos Senior, Arquitectos Cognitivos}
---
## Contexto y Problema

Esta decision se centra en los sensores IoT, se refiere a los componentes encargados de recopilar datos ambientales y de procesos en tiempo real. El problema radica en elegir la mejor opción para implementar estos sensores y garantizar una comunicación eficiente con los demás componentes del sistema.

## Drivers de Decisión

* RF005: Sensores IoT
* RF005-1: Sensores familia A (Sensores monolíticos)

## Opción 2: Sensores Modulares

Esta opción implica el uso de sensores modulares, donde cada sensor está especializado en recopilar un tipo específico de dato.

## Decisión

La opción elegida es la **Opción 2: Opción 2: Sensores Modulares**. Esta opción se seleccionó debido debido a que cumple con los requerimientos funcionales RF005 y RF005-1. Permite una mayor precisión en la detección de datos específicos. Ofrece un menor consumo de energía al utilizar solo los sensores necesarios.

## Consecuencias

Las consecuencias de esta decisión son:

* Bueno, porque permite una arquitectura modular y escalable para la visualización y análisis en tiempo real de la familia 1.
* Bueno, porque facilita la integración de nuevos componentes de visualización en el futuro.
* Malo, porque puede aumentar la complejidad debido a la implementación de los patrones adicionales.

## Confirmación

La implementación de esta decisión se confirmará mediante pruebas de funcionamiento de los sensores modulares en el entorno de aplicación específico. También se realizarán pruebas de integración para garantizar una comunicación eficiente con los demás componentes del sistema.

## Pros y Contras de las Opciones

### Opción 2: Sensores Modulares

* Mayor precisión en la detección debido a la especialización de cada sensor en un tipo de dato específico.
* Menor consumo de energía al utilizar solo los sensores necesarios para cada caso de uso.
* Mayor complejidad en la gestión y configuración de múltiples sensores modulares.
* Posible necesidad de más espacio físico para alojar los diferentes sensores modulares.



## Más Información

-[Sensores Modulares](https://medind10ma.blogspot.com/2017/07/sensores-sensor-un-sensor-es-un.html#:~:text=Son%20aquellos%20en%20donde%20la,entrada%20solo%20controla%20la%20salida.)



---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
parent: Decisiones de arquitectura - Taller 1
Estado: Aprobado
title: Iteración 1
Visualización y Análisis en Tiempo Real: Decisión 1

# status: "{reemplazado por [ADR-0005](0005-ejemplo.md)}"
# date: {2023-06-19}
# deciders: {Grupo 7 - MATI}
# consulted: {Arquitectos Senior, ArquitectosCognitivos}
# informed: {Grupo 7 - MATI}
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

{NNNN}



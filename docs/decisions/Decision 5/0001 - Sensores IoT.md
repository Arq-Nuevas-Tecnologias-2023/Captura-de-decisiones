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

## Opción 1: Sensores Monolíticos

Esta opción consiste en utilizar sensores monolíticos, donde cada sensor está diseñado para recopilar múltiples tipos de datos. Los sensores monolíticos ofrecen una amplia gama de capacidades de detección y son fáciles de implementar en el sistema.


## Pros y Contras de las Opciones

### Opción 1: Sensores Monolíticos

* Bueno, porque proporciona una mayor precisión en la detección al especializar cada sensor en un tipo de dato específico.
* Bueno, porque reduce el consumo de energía al utilizar solo los sensores necesarios para cada caso de uso.
* Malo, porque puede haber una mayor complejidad en la gestión y configuración de múltiples sensores modulares.
* Malo, porque puede requerir más espacio físico para alojar los diferentes sensores modulares.

## Más Información

{NNNN}



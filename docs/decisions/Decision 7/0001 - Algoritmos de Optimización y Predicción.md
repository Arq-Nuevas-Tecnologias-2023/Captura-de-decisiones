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

En el proyecto se requiere implementar algoritmos de optimización y predicción para mejorar la eficiencia y la toma de decisiones en el sistema. Se busca una arquitectura que permita gestionar y ejecutar estos algoritmos de manera eficiente y escalable.

## Drivers de Decisión

* RF006: Algoritmos de optimización de órdenes de trabajo.
* RF007: Componente de predicción de fallos y resolución.
* RF008: Control de conexión de dispositivos.

## Opción 1: Arquitectura basada en Strategy Pattern

Se implementará una arquitectura basada en el patrón de diseño Strategy para los algoritmos de optimización y predicción. Cada algoritmo se encapsulará en una estrategia independiente que puede ser intercambiada dinámicamente en tiempo de ejecución. Esto permite una mayor flexibilidad y extensibilidad en el sistema.

### Detalles de la Opción 1

Ventajas de la Opción 1:

* Permite la fácil adición o modificación de estrategias de optimización y predicción sin afectar a otros componentes.
* Proporciona una clara separación de responsabilidades entre las estrategias y el contexto que las utiliza.
* Facilita la reutilización de estrategias en diferentes contextos dentro del sistema.

Desventajas de la Opción 1:

* Requiere una adecuada definición de interfaces y abstracciones para las estrategias y el contexto.
* Puede generar una mayor complejidad en la gestión y configuración de múltiples estrategias.

## Decisión

La opción elegida es la **Opción 1: Arquitectura basada en Strategy Pattern**. Esta opción ofrece una mayor flexibilidad, extensibilidad y separación de responsabilidades, lo cual es beneficioso para el sistema en general.

## Consecuencias

Las consecuencias de esta decisión son:

* Bueno, porque permite la fácil adición o modificación de estrategias de optimización y predicción sin afectar a otros componentes.
* * Bueno, porque proporciona una clara separación de responsabilidades entre las estrategias y el contexto que las utiliza.
* Malo, porque requiere una adecuada definición de interfaces y abstracciones para las estrategias y el contexto.
Malo, porque puede generar una mayor complejidad en la gestión y configuración de múltiples estrategias.
## Confirmación

La implementación de la arquitectura basada en Strategy Pattern será confirmada mediante revisiones de diseño, pruebas de integración y seguimiento del rendimiento del sistema. Se realizarán pruebas para garantizar que las estrategias se puedan intercambiar correctamente y cumplan con los requisitos de rendimiento y funcionalidad establecidos.


## Más Información

- [Algoritmo de regresión logística] (https://www.kdnuggets.com/2022/07/logistic-regression-work.html#:~:text=is%20Logistic%20Regression%3F-,Logistic%20regression%20is%20a%20Machine%20Learning%20classification%20algorithm%20that%20is,the%20logistic%20of%20the%20result)
- [Algoritmo Gradient Boosting] (https://www.cienciadedatos.net/documentos/py09_gradient_boosting_python)



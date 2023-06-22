---
# Gestión de Base de Datos: Elección de la Tecnología de Persistencia

## Contexto y Declaración del Problema

En la Familia 4, se requiere implementar un componente gestor de base de datos que cumpla con el estilo arquitectónico Event Driven (STREAM) y el patrón ABSTRACT FACTORY. La elección de la tecnología de persistencia es fundamental para garantizar la escalabilidad, rendimiento y confiabilidad del sistema.

## Drivers de Decisión

* RF004: Componente gestor de base de datos
* Estilo arquitectónico: Event Driven (STREAM)
* Patrón de diseño: ABSTRACT FACTORY
* Escalabilidad y rendimiento del sistema

## Opciones Consideradas

### Opción 1: Base de Datos Relacional (MySQL)

La opción 1 consiste en utilizar una base de datos relacional, como MySQL, para gestionar la persistencia de los datos. Esta tecnología es ampliamente utilizada y cuenta con un sólido soporte y documentación. Además, se puede aplicar el patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas a la base de datos.

#### Ventajas de la Opción 1

* Amplia adopción y comunidad activa.
* Soporte para transacciones ACID.
* Capacidad para realizar consultas SQL complejas.
* Aplicación del patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas.

#### Desventajas de la Opción 1

* Menor rendimiento en comparación con algunas tecnologías NoSQL.
* Mayor complejidad en el modelado de datos debido a las restricciones de esquema.

### Opción 2: Base de Datos NoSQL (MongoDB)

La opción 2 propone utilizar una base de datos NoSQL, como MongoDB, que ofrece una estructura flexible y escalabilidad horizontal. Este tipo de tecnología es adecuada para escenarios donde se requiere un alto rendimiento y almacenamiento de datos no estructurados. El patrón ABSTRACT FACTORY también se puede aplicar para abstraer la creación de conexiones y consultas a la base de datos.

#### Ventajas de la Opción 2

* Alta escalabilidad horizontal y capacidad para manejar grandes volúmenes de datos.
* Flexibilidad en el modelado de datos debido a la ausencia de un esquema rígido.
* Mayor rendimiento en operaciones de lectura y escritura en comparación con algunas bases de datos relacionales.
* Aplicación del patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas.

#### Desventajas de la Opción 2

* Menor soporte y comunidad en comparación con las bases de datos relacionales.
* Limitaciones en consultas complejas y transacciones ACID.

## Decisión Tomada

Se elige la **Opción 2: Base de Datos NoSQL (MongoDB)** como tecnología de persistencia para el componente gestor de base de datos en la Familia 4. Esta elección se basa en los siguientes argumentos:

* La opción 2 proporciona una mayor escalabilidad horizontal y un mejor rendimiento en operaciones de lectura y escritura, lo cual es crucial en un entorno Event Driven.
* La flexibilidad en el modelado de datos de MongoDB se adapta mejor a las necesidades de almacenamiento de datos no estructurados que pueden surgir en la Familia 4.
* La aplicación del patrón ABSTRACT FACTORY permitirá abstraer la creación de conexiones y consultas a la base de datos, facilitando la adaptabilidad y mantenibilidad del componente gestor de base de datos.

## Consecuencias

### Buenas

* Mayor escalabilidad y rendimiento en operaciones de lectura y escritura.
* Flexibilidad en el modelado de datos para manejar datos no estructurados.
* Aplicación del patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas.

### Malas

* Menor soporte y comunidad en comparación con las bases de datos relacionales.
* Limitaciones en consultas complejas y transacciones ACID.

## Confirmación

La elección de la base de datos NoSQL (MongoDB) como tecnología de persistencia será confirmada mediante una revisión del diseño e implementación del componente gestor de base de datos. Además, se realizarán pruebas de escalabilidad y rendimiento para garantizar que cumple con los requisitos establecidos.

## Más Información

Se debe realizar una revisión periódica de la elección de la tecnología de persistencia para evaluar si sigue cumpliendo con los requisitos y realizar ajustes si es necesario. Además, se deben considerar las necesidades específicas del sistema en cuanto a escalabilidad, rendimiento y manejo de datos no estructurados. Se pueden consultar recursos adicionales sobre bases de datos NoSQL y el patrón ABSTRACT FACTORY para obtener información más detallada sobre las características y casos de uso de cada opción.

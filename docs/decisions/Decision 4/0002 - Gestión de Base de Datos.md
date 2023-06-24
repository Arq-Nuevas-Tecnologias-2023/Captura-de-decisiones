---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
Estado: Aprobado
title: Gestión de Base de Datos.
Decisión: 002
date: 2023-06-19
deciders: {Grupo 7 - MATI}
consulted: {Arquitectos Senior, Arquitectos Cognitivos}
---
## Contexto y Problema

Se requiere implementar un componente gestor de base de datos que cumpla con el estilo arquitectónico Event Driven y el patrón ABSTRACT FACTORY. La elección de la tecnología de persistencia es fundamental para garantizar la escalabilidad, rendimiento y confiabilidad del sistema.


## Drivers de Decisión

* RF004: Componente gestor de base de datos

## Opción 2: Base de Datos NoSQL

La opción 2 propone utilizar una base de datos NoSQL, como MongoDB, que ofrece una estructura flexible y escalabilidad horizontal. Este tipo de tecnología es adecuada para escenarios donde se requiere un alto rendimiento y almacenamiento de datos no estructurados. El patrón ABSTRACT FACTORY también se puede aplicar para abstraer la creación de conexiones y consultas a la base de datos.

## Confirmación

La elección de la base de datos NoSQL (MongoDB) como tecnología de persistencia será confirmada mediante una revisión del diseño e implementación del componente gestor de base de datos. Además, se realizarán pruebas de escalabilidad y rendimiento para garantizar que cumple con los requisitos establecidos.


## Pros y Contras de las Opciones

### Opción 2: Patrón Request/Response

* Bueno, porque ofrece una alta escalabilidad horizontal y capacidad para manejar grandes volúmenes de datos.
* Bueno, porque brinda flexibilidad en el modelado de datos debido a la ausencia de un esquema rígido.
* Bueno, porque presenta un mayor rendimiento en operaciones de lectura y escritura en comparación con algunas bases de datos relacionales.
* Bueno, porque se puede aplicar el patrón ABSTRACT FACTORY para abstraer la creación de conexiones y consultas.
* Malo, porque tiene un menor soporte y comunidad en comparación con las bases de datos relacionales.
* Malo, porque presenta limitaciones en consultas complejas y transacciones ACID.

## Más Información
-[Documentación MongoDB](https://www.mongodb.com/es/nosql-explained) 
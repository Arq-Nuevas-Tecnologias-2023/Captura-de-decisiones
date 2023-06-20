---
# Configuración para la plantilla de ADR "Nuevas tecnologias"
parent: Decisiones de arquitectura
nav_order: 3
title: Iteración 3

# status: "{Acepted [ADR-0005](0005-ejemplo.md)}"
# date: {2023-06-19}
# deciders: {Grupo 7 - MATI}
# consulted: {Arquitectos Senior, ArquitectosCognitivos}
# informed: {Grupo 7 - MATI}
---
## Contexto y Problema Planteado

El sistema requiere un estilo de arquitectura Event Driven para manejar eventos de manera eficiente y permitir la comunicación y sincronización entre diferentes componentes. Además, es necesario satisfacer los siguientes requerimientos funcionales utilizando patrones de diseño:

- RF001: Centro de notificaciones
- RF001-1: Componente de visualización de analítica para procesos productivos
- RF001-2: Componente de visualización de analítica para órdenes de trabajo
- RF001-3: Componente de visualización de sensores de los componentes IoT tipo Cockpit
- RF002: Módulo de Órdenes de Trabajo
- RF003: Componente de mensajería interna y notificaciones
- RF004: Componente gestor de base de datos
- RF005: Sensores IoT
- RF005-1: Sensores familia A (Sensores monolíticos)
- RF006: Algoritmos de optimización de órdenes de trabajo
- RF007: Componente de predicción de fallos y resolución
- RF008: Control de conexión de dispositivos
    
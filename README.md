# AI Automation Avanzado — Coderhouse

Repositorio de actividades, checkpoints y proyecto integrador desarrollados durante el curso **AI Automation Avanzado de Coderhouse**.

Este curso forma parte de mi proceso de formación en automatización e inteligencia artificial, como continuación de AI Automation y preparación para profundizar posteriormente en AI Engineering.

## Objetivo del repositorio

Documentar el diseño, implementación y evolución de soluciones de automatización con IA, aplicando progresivamente conceptos como:

- Automatización de procesos con n8n.
- LLMs y agentes con herramientas (Tool Calling).
- Arquitecturas multiagente y multi-workflow.
- Memoria conversacional y persistencia de contexto.
- Integraciones mediante APIs y servicios externos.
- Retrieval-Augmented Generation (RAG).
- Interacción por voz.
- Testing, manejo de errores y observabilidad.

El objetivo no es solamente construir automatizaciones funcionales, sino comprender su arquitectura, evaluar decisiones técnicas e identificar sus limitaciones.

## Proyecto integrador — Centro Alma Mística

Como caso de aplicación se utiliza **Centro Alma Mística**, un centro holístico que ofrece cursos, talleres, terapias y productos relacionados.

El proyecto busca desarrollar progresivamente un sistema de atención y gestión asistido por inteligencia artificial, capaz de responder consultas, recuperar información, interactuar con servicios externos y coordinar procesos administrativos.

El desarrollo parte de un escenario de laboratorio con datos ficticios, inspirado en necesidades de un negocio real.

### Evolución del proyecto

| Módulo | Alcance |
|---|---|
| M1 | Agente base, System Prompt, herramientas y observabilidad |
| M2 | Arquitectura multiagente y subworkflows |
| M3 | Memoria y persistencia de contexto |
| M4 | Integraciones con servicios externos |
| M5 | RAG y recuperación de conocimiento documental |
| M6 | Interacción por voz |
| M7–M11 | Evolución según los requisitos de los siguientes módulos y proyecto final |

Cada checkpoint utilizará como punto de partida el trabajo realizado anteriormente, incorporando nuevas capacidades sin reconstruir innecesariamente el sistema.

## Checkpoints

| Entrega | Descripción | Estado |
|---|---|---|
| [Checkpoint 1](./checkpoint-1/) | Configuración del Tools Agent, catálogo Google Sheets y auditoría mediante Gmail | Implementado y probado |
| Checkpoint 2 | Arquitectura multiagente | Pendiente |
| Checkpoints posteriores | Evolución del proyecto integrador | Pendiente |

## Criterios de desarrollo

Durante el proyecto se priorizan:

- Separación entre operaciones determinísticas y decisiones asistidas por LLM.
- Responsabilidades claras para agentes, herramientas y workflows.
- Validación de datos y restricciones de autorización.
- Pruebas funcionales, negativas y de contingencia.
- Trazabilidad y observabilidad de las ejecuciones.
- Simplicidad, seguridad, mantenibilidad y control de costos.

Las decisiones tecnológicas y las limitaciones conocidas se documentan en cada checkpoint.

## Alcance

Este repositorio contiene implementaciones académicas y prototipos de laboratorio. No representa un sistema desplegado en producción ni un servicio comercial activo
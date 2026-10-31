# Centro Alma Mística — AI Automation Avanzado

Proyecto integrador desarrollado en n8n como parte de la carrera AI Automation de Coderhouse.

El objetivo es construir progresivamente un sistema de automatización con IA para un centro holístico que ofrece cursos, talleres, terapias y productos.

El proyecto utiliza un escenario de negocio inspirado en Centro Alma Mística, con datos ficticios para las pruebas académicas.

## Checkpoint 1 — Agente base y motor de razonamiento

Se implementó un asistente de atención comercial que recibe consultas mediante n8n Chat, interpreta las solicitudes y decide cuándo utilizar Google Sheets como herramienta para consultar el catálogo.

### Componentes

- **Chat Trigger:** recibe las consultas de los usuarios.
- **AI Agent (Tools Agent):** interpreta solicitudes y decide cuándo invocar herramientas.
- **OpenRouter + DeepSeek:** modelo de lenguaje utilizado para el razonamiento y tool calling.
- **Google Sheets Tool:** consulta el catálogo de cursos, talleres, terapias y productos.
- **Chat:** entrega la respuesta al usuario.
- **Gmail:** genera un reporte automático de supervisión con información de la ejecución.

El agente tiene un límite de seis iteraciones y un System Prompt que define su rol, objetivos, restricciones y criterios de escalamiento.

## Pruebas realizadas

Se verificaron consultas comerciales, uso autónomo de herramientas, saludos sin invocaciones innecesarias, solicitudes de modificación no autorizadas, información inexistente y consultas sensibles sobre terapias.

También se realizaron pruebas controladas de fallo de Google Sheets y entrega de correo, utilizando una copia del workflow.

El reporte de supervisión distingue tres estados básicos:

- `SUCCESS`: llamada a herramienta sin errores detectados.
- `TOOL_ERROR`: error reconocido en la respuesta de una herramienta.
- `NO_TOOL_USED`: ejecución sin llamadas a herramientas.

## Limitaciones

El agente solamente consulta información y no está autorizado para modificar precios, gestionar pagos o confirmar inscripciones y reservas.

El catálogo utiliza datos ficticios. La clasificación de auditoría es básica y no sustituye una plataforma completa de observabilidad como Datadog.

## Continuidad

Este workflow constituye la primera versión del proyecto integrador. Se ampliará en los próximos módulos con nuevas capacidades, manteniendo el enfoque de responsabilidades claras, validación, seguridad y observabilidad.

## Archivo de entrega

`checkpoint1_andres_munoz.json`

El workflow requiere configurar credenciales y servicios externos en la instancia de n8n correspondiente.
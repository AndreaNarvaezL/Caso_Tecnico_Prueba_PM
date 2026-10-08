# Caso práctico de Project Manager para Tpaga

Propuesta de planificación y recuperación del proyecto **Lanzamiento de Transferencias Interoperables Inmediatas en Tpaga**, elaborada como ejercicio de candidatura a Project Manager, con enfoque complementario en validación jurídica y gestión de riesgos.

Este repositorio reúne los tres entregables solicitados, sus cronogramas y los archivos para estructurar el seguimiento en Jira. **La propuesta no representa una implementación ejecutada ni resultados reales de Tpaga.**

## Comenzar la revisión

El [documento ejecutivo en PDF](Tpaga_Entregables_Finales.pdf) contiene la solución completa y puede revisarse de forma independiente. El [texto editable](Tpaga_Entregables_Editables.md) permite consultar su contenido en el repositorio.

| Entregable | Contenido |
| --- | --- |
| **1. Plan de proyecto y reestimación** | Alcance funcional, EDT en cuatro fases, cronograma inicial, escenario impactado, recuperación propuesta, ruta crítica y balance de capacidad por rol. |
| **2. Riesgos y comunicación** | Registro de los dos incidentes, riesgos derivados, estrategias de respuesta, informe de una página para PO y comité, RACI y frecuencia de comunicación. |
| **3. Priorización del MVP** | Matriz MoSCoW y trade-offs para liberar capacidad sin retirar controles esenciales de seguridad, operación o cumplimiento. |
| **Complemento jurídico** | Referencias nacionales, validación de aplicabilidad por actor, revisión contractual y traducción de requisitos en actividades, evidencias y condiciones de lanzamiento. |

## Contexto del ejercicio

El caso establece una salida a producción en ocho semanas. Durante la semana 4, en Sprint 2, se presentan simultáneamente:

- Un retraso de tres semanas del sandbox del aliado, que bloquea las pruebas E2E de liquidación en tiempo real.
- Una vulnerabilidad de severidad alta en el middleware de tokenización, cuya corrección exige modificar la autorización backend y requiere **80 horas de esfuerzo acumulado**, no previstas en la capacidad del sprint.

La solución mantiene el lanzamiento de transferencias como objetivo de negocio y organiza el trabajo técnico, regulatorio, de pruebas y despliegue alrededor de ese objetivo.

## Propuesta de recuperación

1. Priorizar la corrección de autorización y reservar revisión, retest independiente y regresión.
2. Diferir funcionalidades opcionales con aprobación de la PO y validar la capacidad liberada por rol.
3. Construir una simulación interna mínima, basada en especificaciones confirmadas del aliado, para adelantar verificaciones internas.
4. Preparar casos, datos, procedimientos operativos y despliegue mientras se recupera el ambiente externo.
5. Completar las pruebas reales y las aprobaciones requeridas antes de habilitar producción.

**Los mocks no reemplazan el sandbox externo, la certificación ni la comprobación de liquidación real.**

## Supuestos y condiciones para conservar la semana 8

Los cronogramas usan días hábiles relativos: **D0** es el inicio; **D15** inicia la semana 4; **D30** inicia la semana 7; **D40** termina la semana 8. Se suponen semanas de cinco días y sprints de dos semanas. El caso no proporciona fecha de inicio ni calendario de festivos.

El balance ilustrativo propone diferir **92 horas backend**: 80 para la corrección y 12 para mocks mínimos. Las horas opcionales, las 12 horas de mocks y la capacidad productiva utilizada son **estimaciones propuestas pendientes de validación**, no datos aportados por Tpaga. QA y Ciberseguridad se planifican por separado.

La recuperación supone sandbox disponible en D30 y una ventana de cinco días hábiles para E2E y certificación, validada por los aliados. No presupone una entrega anticipada del sandbox ni permite omitir pruebas obligatorias.

Si la capacidad o la ventana externa no se confirman, se escala el impacto y la decisión requerida. **La fecha objetivo no sustituye las condiciones de seguridad, cumplimiento y aprobación externa.**

## Archivos de planificación

| Archivo | Finalidad |
| --- | --- |
| [Cronogramas](03_Cronogramas.csv) | Comparar línea base, impacto y recuperación con duraciones, predecesoras y condiciones. |
| [Dependencias](04_Dependencias.csv) | Consultar relaciones propuestas y configurarlas posteriormente con claves reales de Jira. |
| [Capacidad](05_Capacidad.csv) | Revisar esfuerzo backend y disponibilidad propuesta de QA y Ciberseguridad. |
| [Riesgos](06_Riesgos.csv) | Consultar incidentes, riesgos futuros, responsables, respuestas y fechas de decisión. |

## Seguimiento en Jira

Se proponen **cuatro épicas y 33 tareas**, con responsables por rol, criterios de aceptación, dependencias y ventanas relativas.

- **Opción recomendada:** [CSV jerárquico](01_Jira_Jerarquia.csv), si el importador admite identificadores y relaciones Parent.
- **Alternativa:** [CSV de tareas simples](02_Jira_Tareas_Simple.csv), si no se dispone de importación jerárquica.
- **Instrucciones:** [Guía de importación](LEEME_Importacion_Jira.md).

**Importar solo una alternativa para evitar duplicados.** Las estimaciones se expresan en segundos. Los identificadores locales no son claves reales de Jira. No se incluyen usuarios ficticios, horas consumidas ni tareas presentadas como completadas.

Los CSV de cronogramas, dependencias, capacidad y riesgos son archivos de consulta y control; no crean automáticamente fechas, enlaces o campos en Jira. No se ha realizado una importación en una instancia real. Cuando el proyecto esté configurado, su enlace de revisión se incorporará a este README.

## Enfoque jurídico y fuentes

El documento cita normas colombianas de referencia sobre pagos, protección de datos, consumidor, contratos y trabajo suplementario, y explica las validaciones de aplicabilidad necesarias. La propuesta no asume que Tpaga sea una entidad vigilada ni que la infraestructura del caso sea Bre-B. DSP-465 se utiliza como referencia condicionada al modelo que se confirme; ISO 20022 se identifica como estándar técnico de mensajería financiera.

Las referencias y enlaces están incluidos en el PDF y en el texto editable. La fuente de los hechos y requisitos es la prueba técnica suministrada; las estimaciones adicionales se distinguen como supuestos del ejercicio.

## Uso del repositorio

Repositorio preparado para revisión de la candidatura por Tpaga. Los archivos enlazados deben ubicarse junto a este README. El PDF contiene la entrega completa; el repositorio y Jira facilitan explorar su planificación y trazabilidad.

# Caso práctico de Project Manager para Tpaga

Propuesta de planificación y recuperación del proyecto «Lanzamiento de Transferencias Interoperables Inmediatas en Tpaga», elaborada como ejercicio de candidatura a Project Manager, con enfoque complementario en validación jurídica y gestión de riesgos.

**Nota:** La propuesta no representa una implementación ejecutada ni resultados reales de Tpaga.

## Entregables

| Documento | Contenido |
| --- | --- |
| [Entregable 1: Plan de proyecto y reestimación](Tpaga_Entregable_1_Plan_Proyecto.pdf) | Objetivo y alcance, flujo funcional y controles, EDT por fases, actividades en paralelo, cronogramas inicial, impactado y recuperado, dependencias, rutas críticas, hitos y validaciones de capacidad. |
| [Entregable 2: Mitigación de riesgos y comunicación](Tpaga_Entregable_2_Riesgos_Comunicacion.pdf) | Incidentes y riesgos, estrategias de respuesta, informe ejecutivo de una página para PO y comité, decisiones y escalamiento, matriz RACI, flujo de comunicación y frecuencia de seguimiento. |
| [Entregable 3: Priorización del MVP](Tpaga_Entregable_3_Priorizacion_MVP.pdf) | Matriz MoSCoW, trade-offs, funcionalidades diferidas, simulación durante el bloqueo y condiciones de reingreso al backlog y control de cambios. |
| [Anexo: Complemento jurídico](Tpaga_Anexo_Juridico.pdf) | Validación de aplicabilidad por actor, datos personales, consumidor, contratos, capacidad y costos, precisión sobre ISO 20022 y condiciones jurídicas de lanzamiento. |



## Contexto y recuperación propuesta

El caso fija una salida a producción en ocho semanas. Durante la semana 4, Sprint 2, se presentan un retraso de tres semanas del sandbox del aliado y una vulnerabilidad alta cuya corrección requiere 80 horas de esfuerzo acumulado no previstas en la capacidad del sprint.

La propuesta prioriza corregir la autorización, validar los diferimientos del MVP, preparar pruebas y operación en paralelo y utilizar simulaciones internas mínimas cuando sean útiles y exista capacidad. El lanzamiento requiere completar las pruebas reales, los controles y las aprobaciones exigibles.

**Nota:** Los mocks no corrigen la vulnerabilidad ni sustituyen el sandbox, E2E o la aprobación externa correspondiente.

## Hitos y cronogramas

| Semana | Límite de inicio | Límite de cierre | Sprint |
| --- | --- | --- | --- |
| 1 | D0 | D5 | 1 |
| 2 | D5 | D10 | 1 |
| 3 | D10 | D15 | 2 |
| 4 | D15 | D20 | 2 |
| 5 | D20 | D25 | 3 |
| 6 | D25 | D30 | 3 |
| 7 | D30 | D35 | 4 |
| 8 | D35 | D40 | 4 |

**Nota:** Los límites se comparten sin duplicar días: D0–D5 representa cinco días hábiles. Se supone trabajo de lunes a viernes; al asignar fechas reales se incorporará el calendario de festivos.

La línea base termina en D40; el escenario impactado, sin recuperación del plazo y manteniendo las duraciones propuestas, termina en D55. La recuperación propone E2E en D30–D33, aprobación externa en D33–D35, decisión Go/No-Go en D35 y despliegue y estabilización en D35–D40.

**Nota:** Se supone sandbox inicialmente previsto en D15 y reestimado en D30. Deben confirmarse la fecha comprometida y el hito desde el cual se cuentan las tres semanas. Las duraciones propuestas requieren validación del equipo y los aliados.

**Nota:** Las 80 horas proceden del caso. La disponibilidad por rol, el esfuerzo liberable por diferimientos y el esfuerzo de mocks y validaciones están por confirmar; no se presume una capacidad liberada de 92 horas.

## Archivos de planificación

| Archivo | Finalidad |
| --- | --- |
| [Cronogramas](03_Cronogramas.csv) | Comparar línea base, impacto y recuperación. |
| [Dependencias](04_Dependencias.csv) | Consultar relaciones propuestas entre actividades. |
| [Capacidad](05_Capacidad.csv) | Registrar las necesidades y validaciones de disponibilidad por rol. |
| [Riesgos](06_Riesgos.csv) | Consultar incidentes, riesgos, responsables, respuestas y fechas de decisión. |

## Seguimiento en Jira

Se proponen cuatro épicas y 33 tareas con criterios de aceptación, responsables por rol y ventanas relativas.

- [CSV jerárquico](01_Jira_Jerarquia.csv)
- [CSV de tareas simples: alternativa](02_Jira_Tareas_Simple.csv)
- [Guía de importación](LEEME_Importacion_Jira.md)


## Enfoque jurídico y fuentes

Las referencias se presentan en los documentos correspondientes y en el anexo jurídico, con validación de aplicabilidad según los actores y el modelo operativo. DSP-465 se utiliza como referencia condicionada a la infraestructura y roles que se confirmen. ISO 20022 se identifica como estándar de mensajería financiera.

## Cómo revisar la propuesta

Comenzar por el entregable 1, continuar con riesgos y comunicación y finalizar con la priorización del MVP. El anexo jurídico explica las validaciones complementarias. Los CSV permiten consultar el detalle de la planificación.

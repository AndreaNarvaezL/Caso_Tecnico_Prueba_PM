# Caso práctico de Project Manager para Tpaga

Propuesta de planificación y recuperación de Transferencias Interoperables Inmediatas, como ejercicio de candidatura con enfoque jurídico y gestión de riesgos.

**Nota:** representa una propuesta; no una implementación ni resultados reales de Tpaga.

## Documentos y entregables

- [Documento ejecutivo completo](Tpaga_Entregables_Finales.pdf)
- [Documento editable](Tpaga_Entregables_Finales.docx)

| Entregable                | Contenido                                                                          |
| ------------------------- | ---------------------------------------------------------------------------------- |
| 1. Plan y reestimación    | Flujo y controles, EDT con paralelismo, tres cronogramas, ruta crítica y capacidad |
| 2. Riesgos y comunicación | Incidentes, matriz de riesgos, informe de una página, RACI y comunicación          |
| 3. Priorización MVP       | MoSCoW y diferimientos para absorber esfuerzo sin retirar controles esenciales     |
| Plus jurídico             | Normas nacionales, aplicabilidad por actor, contratos y evidencias de salida       |

## Lectura del cronograma actualizado

| Semana | Límite de inicio | Límite de cierre | Sprint |
| ------ | ---------------- | ---------------- | ------ |
| 1      | D0               | D5               | 1      |
| 2      | D5               | D10              | 1      |
| 3      | D10              | D15              | 2      |
| 4      | D15              | D20              | 2      |
| 5      | D20              | D25              | 3      |
| 6      | D25              | D30              | 3      |
| 7      | D30              | D35              | 4      |
| 8      | D35              | D40              | 4      |

**Nota:** límites compartidos sin duplicar días: D0-D5 dura cinco días hábiles. No se cuentan sábados ni domingos; al asignar fechas reales incorporar festivos.

**Nota:** el caso sitúa la crisis en semana 4, Sprint 2. Se supone inicio del incidente en D15, sandbox y E2E originales en D15, y sandbox retrasado en D30. Confirmar el compromiso original y desde qué hito se cuentan tres semanas.

La línea base cierra D40. Sin recuperación, y manteniendo las duraciones propuestas, cierra D55 (semana 11). La recuperación conserva D40 solo si se confirman capacidad y agenda externa D30-D35. Preparar operación en paralelo reduce su impacto sobre la ruta crítica.

**Nota:** la simulación interna adelanta verificaciones; no sustituye sandbox, E2E ni certificación del aliado. Las duraciones son estimaciones propuestas, no datos de Tpaga.

**Nota:** este paquete actualiza únicamente CSV e instrucciones. Los documentos completos deben corresponder a la versión final revisada por la candidata.

## Planificación para Jira

4 épicas y 33 tareas con responsables por rol, criterios de aceptación y ventanas relativas.

- [CSV jerárquico](01_Jira_Jerarquia.csv)
- [CSV simple alternativo](02_Jira_Tareas_Simple.csv)
- [Guía de importación](LEEME_Importacion_Jira.md)

**Nota:** importar una alternativa, no ambas. No se ha importado en una instancia real. Los identificadores de cronograma no son claves Jira.

## Archivos de control

- [Cronogramas](03_Cronogramas.csv)
- [Dependencias](04_Dependencias.csv)
- [Capacidad](05_Capacidad.csv)
- [Riesgos](06_Riesgos.csv)

**Nota:** las 80 horas acumuladas de corrección proceden del caso. La disponibilidad por rol, las horas liberables y el esfuerzo de mocks y validaciones están por confirmar; no se presume un balance cerrado.

## Enfoque jurídico

Las fuentes oficiales y sus condiciones de aplicabilidad se incluyen en el PDF y el texto editable. DSP-465 solo se aplica si infraestructura y roles lo justifican; ISO 20022 es un estándar de mensajería financiera.

**Nota:** las condiciones obligatorias de seguridad, cumplimiento y aprobación externa deben completarse antes de habilitar producción, aunque exista presión por el plazo.

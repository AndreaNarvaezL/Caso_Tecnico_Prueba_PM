# Importación de la planificación en Jira

Importar una sola alternativa: 01_Jira_Jerarquia.csv si el importador permite Issue ID y Parent; de lo contrario 02_Jira_Tareas_Simple.csv y crear/asociar épicas después. No importar ambas.

Mapear Summary, Description, Issue Type, Priority y Labels. En jerárquico, mapear Issue ID y Parent según las opciones de la instancia y crear primero las épicas si el importador lo exige. Validar en vista previa la relación de una tarea con su épica antes de completar.

Original Estimate está en segundos: únicamente T106 contiene 288000 (80 horas acumuladas del caso). Si el importador requiere una unidad explícita, usar 80h para esa celda. Las demás estimaciones están vacías porque requieren estimación; no significan cero. No registrar horas consumidas.

Los responsables son roles propuestos en Description; no son usuarios asignados. D15, D30 y demás referencias son límites relativos de días hábiles, no fechas de Jira. Al confirmar inicio y festivos convertirlas a fechas reales.

Los cuatro CSV de control no son importadores de incidencias. 03 compara escenarios; 04 permite configurar enlaces con claves reales; 05 registra capacidad por validar; 06 registra incidentes y riesgos. Las dependencias parciales y de cierre no son bloqueos completos fin-inicio.

Mocks y su validación son condicionales; no bloquean por sí solos E2E. Certificación significa aprobación de integración exigida por el aliado según el modelo confirmado.

Nota: cuatro épicas y 33 tareas propuestas; ninguna se presenta como ejecutada. No se ha realizado importación en una instancia real.

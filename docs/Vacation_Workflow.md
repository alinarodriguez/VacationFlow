# Gestión de Vacaciones – Caso de Estudio

## 1. Business Rules
- Cada empleado tiene un máximo de 15 días de vacaciones al año.
- No se permite aprobar solicitudes que excedan los días disponibles.
- Solicitudes deben enviarse con al menos 5 días de anticipación.
- Aprobaciones/Rechazos notifican automáticamente al empleado.
- Vacaciones aprobadas actualizan los días usados por el empleado.

## 2. SharePoint Lists

### Employees
| Campo | Tipo | Descripción |
|-------|------|-------------|
| EmployeeID | Número | ID único del empleado |
| Name | Texto | Nombre completo |
| Department | Texto | Departamento |
| VacationDaysAllowed | Número | Días permitidos por año |
| VacationDaysUsed | Número | Días usados en el año |

### Vacation Requests
| Campo | Tipo | Descripción |
|-------|------|-------------|
| RequestID | Número | ID único de la solicitud |
| EmployeeID | Lookup | Relación con empleado |
| StartDate | Fecha | Fecha de inicio |
| EndDate | Fecha | Fecha de fin |
| DaysRequested | Número | Días solicitados |
| Status | Choice | Pending / Approved / Rejected |
| Comments | Texto | Comentarios del supervisor |

## 3. Workflow Structure
1. El empleado crea la solicitud.
2. Validación: `DaysRequested` + `VacationDaysUsed` ≤ `VacationDaysAllowed`.
3. Si válido → enviar a supervisor; si no → rechazo automático.
4. Supervisor aprueba o rechaza.
5. Si aprobado → actualizar `VacationDaysUsed`.
6. Notificación al empleado.

## 4. Workflow Diagram
![diagramaFlujo](images/diagramaFlujo.png)

## 5. Scenarios
| Escenario | Acción esperada |
|-----------|----------------|
| Solicitud válida dentro de días | Enviar a supervisor |
| Solicitud excede días permitidos | Rechazo automático y notificación |
| Solicitud aprobada | Actualizar días usados y notificar |
| Solicitud rechazada | Notificar sin actualizar días usados |

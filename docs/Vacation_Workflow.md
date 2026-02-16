# Gestión de Vacaciones – Caso de Estudio

## 1. Business Rules
- Cada empleado tiene un máximo de 15 días de vacaciones al año.
- No se permite aprobar solicitudes que excedan los días disponibles.
- Solicitudes deben enviarse con al menos 5 días de anticipación.
- Aprobaciones/Rechazos notifican automáticamente al empleado.
- Vacaciones aprobadas actualizan los días usados por el empleado.

## 2. Estructura de Datos (Excel Online)
La solución utiliza Excel Online (OneDrive) como capa de almacenamiento de datos estructurada.

### 📊 Employees.xlsx

| Campo | Tipo | Descripción |
|-------|------|-------------|
| EmployeeName | Texto | Nombre completo del empleado |
| StartDate | Fecha | Fecha de contratación |
| AvailableVacationDays | Número | Días de vacaciones disponibles |

---

### 📁 VacationRequests.xlsx

| Campo | Tipo | Descripción |
|-------|------|-------------|
| EmployeeName | Texto | Nombre del empleado |
| StartDate | Fecha | Fecha de inicio de vacaciones |
| EndDate | Fecha | Fecha de fin de vacaciones |
| DaysRequested | Número | Días solicitados (calculados automáticamente) |
| Status | Texto | Pending / Approved / Rejected |
| ApprovalComments | Texto | Comentarios del aprobador |

> Ambas hojas están formateadas como tablas estructuradas de Excel para permitir integración adecuada con Power Automate.

---

## 3. Estructura del Flujo

1. El empleado envía la solicitud de vacaciones mediante Microsoft Forms.
2. Power Automate calcula automáticamente la cantidad de días solicitados en función de la fecha de inicio y fecha de fin.
3. Fase de validación automática:
   - Validación de anticipación:
     Se verifica que la solicitud se realice con al menos 5 días de anticipación respecto a la fecha de inicio.
     - Si no cumple → rechazo automático y notificación al empleado.
   - Validación de días disponibles:
     Se valida que:
     DaysRequested ≤ (VacationDaysAllowed - VacationDaysUsed)
     - Si no cumple → rechazo automático y notificación al empleado.

4. Si todas las validaciones son correctas → la solicitud se envía al supervisor para aprobación.
5. Si el supervisor rechaza la solicitud → se notifica al empleado sin modificar los días utilizados.
6. Si el supervisor aprueba la solicitud:
   - Se actualiza el campo VacationDaysUsed en Employees.xlsx.
   - Se envía notificación final al empleado.

---

## 4. Diagrama del Flujo

![diagramaFlujo](images/diagramaFlujo.jpg)

---

## 5. Escenarios de Prueba

| Escenario | Acción esperada |
|-----------|----------------|
| Solicitud válida dentro del saldo | Enviar a aprobación |
| Solicitud excede días disponibles | Rechazo automático y notificación |
| Solicitud aprobada | Actualizar saldo y notificar |
| Solicitud rechazada | Notificar sin modificar saldo |

---

## 6. Migración futura a SharePoint

La solución actual utiliza Excel Online como capa de datos debido a limitaciones de licencias.
Sin embargo, la arquitectura está diseñada para soportar la migración a listas de SharePoint con cambios mínimos.

Consideraciones para la migración:

- Reemplazar Employees.xlsx con una lista de SharePoint.
- Reemplazar VacationRequests.xlsx con una lista de SharePoint.
- Actualizar los conectores de Power Automate de Excel a SharePoint.
- Mantener la misma lógica de negocio y estructura de aprobación.

Dado que las reglas de negocio se manejan dentro de Power Automate y no están incrustadas en la capa de datos, la transición no afectaría la lógica de validación principal.

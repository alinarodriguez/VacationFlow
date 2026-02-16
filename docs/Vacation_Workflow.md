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

1. El empleado envía la solicitud mediante Microsoft Forms.
2. Power Automate calcula automáticamente los días solicitados.
3. El flujo consulta `Employees.xlsx` para obtener los días disponibles.
4. Validación:  
   `DaysRequested ≤ AvailableVacationDays`
5. Si no cumple la condición → rechazo automático y notificación.
6. Si cumple la condición → enviar solicitud para aprobación.
7. Si es aprobada → actualizar `AvailableVacationDays` en Employees.xlsx.
8. Enviar notificación final al empleado.

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

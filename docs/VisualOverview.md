# VacationFlow – Presentación General

## 🚀 Automatización Integral de Solicitudes de Vacaciones

VacationFlow es una solución desarrollada con Microsoft Power Platform que automatiza el ciclo completo de gestión de vacaciones dentro de una organización.

La aplicación reemplaza procesos manuales basados en correos electrónicos o archivos compartidos, incorporando validaciones de negocio, flujo de aprobación automatizado y actualización consistente de datos.

El resultado es un proceso estructurado, trazable y controlado de principio a fin.

---

## 📌 1. Registro de Solicitud

![Formulario](../Screenshots/01_request-form.png)

Los empleados registran sus fechas desde una interfaz clara e intuitiva.

La aplicación:

- Calcula automáticamente los días solicitados.
- Muestra el saldo disponible en tiempo real.
- Aplica validaciones antes de permitir el envío.
- Previene errores desde el origen del proceso.

El enfoque está en usabilidad y prevención temprana de inconsistencias.

---

## ⚠️ 2. Validaciones de Reglas de Negocio

![Validaciones](../Screenshots/02_validation-message.png)

La solución incorpora validaciones automáticas que garantizan coherencia operativa:

- Bloqueo de solicitudes que excedan el saldo disponible.
- Prevención de superposición con vacaciones aprobadas.
- Restricción de múltiples solicitudes pendientes por empleado.
- Control de anticipación mínima requerida para solicitar vacaciones.

Estas validaciones reducen intervención manual y evitan reprocesos administrativos.

---

## 🔄 3. Flujo Automatizado de Aprobación

![Flujo](../Screenshots/03_flow-overview.png)

Una vez enviada la solicitud, se activa un flujo en Power Automate que:

- Asigna automáticamente la solicitud al responsable correspondiente.
- Establece el estatus inicial como **Pendiente**.
- Ejecuta lógica condicional según el resultado (Aprobado / Rechazado).
- Envía notificaciones automatizadas.
- Registra cada acción para fines de auditoría.

La arquitectura del flujo sigue una estructura clara:

**Trigger → Validación → Condición → Acción → Actualización**

---

## 📧 4. Notificación Automática por Correo

![Correo de Notificación](../Screenshots/04_approval-email.png)

El sistema envía notificaciones estructuradas que incluyen:

- Datos del empleado.
- Fechas solicitadas.
- Días totales.
- Comentarios.
- Enlace directo a revisión.

Esto garantiza comunicación inmediata y seguimiento oportuno.

---

## 📊 5. Panel de Administración

![Panel de Administración](../Screenshots/06_panelAdmin.png)

El panel permite a administradores:

- Visualizar indicadores clave (totales, pendientes, aprobadas, rechazadas).
- Filtrar por empleado, estatus o rango de fechas.
- Revisar solicitudes individuales.
- Acceder al módulo de decisión.

Ofrece visibilidad centralizada del proceso completo.

---

## 👥 6. Pantalla de Aprobación / Rechazo

![Modal de Aprobación](../Screenshots/05_approval-modal.png)

Desde esta vista el gerente puede:

- Aprobar la solicitud.
- Rechazarla con comentario obligatorio.
- Registrar la decisión con fecha y usuario responsable.

Esto asegura control, responsabilidad y trazabilidad.

---

## 📊 7. Actualización Automática de Saldo

![Saldo Antes](../Screenshots/07_SaldoAntes.png)

![Saldo Después](../Screenshots/08_SaldoDespues.png)

Cuando una solicitud es aprobada:

- El saldo disponible se actualiza automáticamente.
- Se mantiene consistencia entre aplicación y fuente de datos.
- Se preserva integridad en los cálculos acumulados.

Demuestra persistencia y sincronización de datos.

---

## 🏢 Escenarios de Aplicación

VacationFlow es especialmente útil para:

- Pequeñas y medianas empresas sin sistema formal de Recursos Humanos.
- Organizaciones que gestionan vacaciones mediante correo o Excel manual.
- Empresas que utilizan Microsoft 365 y desean automatizar procesos internos.
- Negocios que buscan trazabilidad sin invertir en un sistema HR completo.

---

## 🎯 Valor Estratégico

- Reducción significativa de errores manuales  
- Disminución de tiempos en aprobaciones  
- Visibilidad en tiempo real del estado de solicitudes  
- Registro auditable de decisiones  
- Arquitectura escalable preparada para migración futura a SharePoint o Dataverse  

VacationFlow no es solo una aplicación, sino un modelo de automatización aplicable a múltiples procesos internos.

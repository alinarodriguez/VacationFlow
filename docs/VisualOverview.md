# VacationFlow – Presentación General

## 🚀 Automatización de Solicitudes de Vacaciones

VacationFlow es una solución desarrollada con Microsoft Power Platform que automatiza completamente el proceso de solicitud y aprobación de vacaciones dentro de una organización.

El objetivo es reemplazar procesos manuales basados en correos electrónicos o archivos compartidos, proporcionando control, trazabilidad y validaciones automáticas.

---

## 📌 1. Formulario de Solicitud

![Formulario](../screenshots/01_request-form.png)

Los empleados ingresan sus fechas de vacaciones desde una aplicación sencilla e intuitiva.

El sistema calcula automáticamente los días solicitados y valida la información antes de permitir el envío.

---

## ✅ 2. Validaciones Automáticas

![Validaciones](../screenshots/02_validation-message.png)

La aplicación impide:

- Solicitudes que excedan el saldo disponible.
- Superposición con vacaciones previamente aprobadas.
- Más de una solicitud pendiente por empleado.
- Solicitudes con menos de 5 días de anticipación.

Esto reduce errores y evita intervención manual.

---

## 🔄 3. Flujo Automatizado de Aprobación

![Flujo](../screenshots/03_flow-overview.png)

Una vez enviada la solicitud:

- Se asigna automáticamente al gerente correspondiente.
- El estado se establece como **Pendiente**.
- Se envía notificación por correo electrónico.
- Todas las acciones quedan registradas para auditoría.

---

## 👥 4. Proceso de Aprobación

![Correo de Aprobación](../screenshots/04_approval-email.png)

El gerente o administrador puede:

- Aprobar la solicitud.
- Rechazarla con comentario obligatorio.

El sistema registra quién realizó la acción y en qué momento.

---

## 📊 5. Actualización Automática de Saldo

![Actualización de Saldo](../screenshots/05_balance-update.png)

Al aprobarse una solicitud:

- El saldo disponible del empleado se actualiza automáticamente.
- Se mantiene un historial completo de movimientos.
- Se garantiza consistencia de datos.

---

## 💼 ¿Para qué tipo de empresa es ideal?

Esta solución es ideal para:

- Pequeñas y medianas empresas sin sistema de Recursos Humanos.
- Negocios que gestionan vacaciones por correo o Excel.
- Organizaciones que utilizan Microsoft 365 y desean automatizar procesos internos.
- Empresas que buscan orden y trazabilidad sin invertir en un sistema HR completo.

---

## 🎯 Valor que aporta

- Reducción de errores manuales  
- Ahorro de tiempo en aprobaciones  
- Mayor visibilidad del estado de solicitudes  
- Registro auditable de decisiones  
- Arquitectura preparada para migración futura a SharePoint o Dataverse  

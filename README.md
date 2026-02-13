# VacationFlow

## 🚀 Vacation Request Automation – Power Platform

### 📌 Project Overview (English)

VacationFlow is an automated vacation request management system built using Microsoft Power Platform.

The solution allows employees to submit vacation requests, validates the number of requested days against available vacation balance, and routes valid requests through an approval workflow. If approved, the system automatically updates the employee's remaining vacation days.

This project demonstrates intermediate Power Automate capabilities including:

- Business rule validation
- Conditional logic
- Variable handling
- SharePoint integration
- Automated approvals
- Dynamic record updates

**Project Start Date:** February 16, 2026  
**Status:** In Development

---

## 🧩 System Architecture

The solution includes:

1. Microsoft Forms – Vacation request submission  
2. SharePoint List – Employees (stores available vacation days)  
3. SharePoint List – Vacation Requests  
4. Power Automate Flow – Validation + Approval + Update logic  

---

## 🔄 Business Logic

1. Employee submits vacation request (start date / end date).
2. Flow calculates total requested days.
3. System retrieves available vacation balance from SharePoint.
4. Validation:
   - If requested days exceed available balance → automatic rejection.
   - If valid → approval request is sent.
5. If approved:
   - Vacation balance is updated.
   - Request status is updated.
6. If rejected:
   - Status is updated.
   - Notification email is sent.

---

## 🛠 Technologies Used

- Microsoft Power Automate
- Microsoft Forms
- SharePoint Online
- Power Platform

---

## 📂 Repository Structure

-/docs
-/diagrams
-/screenshots

---


Documentation and evidence of the flow design and implementation will be stored in these folders.

---

---

# 🇪🇸 Versión en Español

## 🚀 Automatización de Solicitudes de Vacaciones – Power Platform

### 📌 Descripción General

VacationFlow es un sistema automatizado de gestión de solicitudes de vacaciones desarrollado con Microsoft Power Platform.

Permite a los empleados enviar solicitudes de vacaciones, valida automáticamente los días solicitados contra los días disponibles y envía las solicitudes válidas a un flujo de aprobación. Si la solicitud es aprobada, el sistema descuenta automáticamente los días utilizados del saldo del empleado.

Este proyecto demuestra habilidades intermedias en Power Automate incluyendo:

- Validaciones de reglas de negocio
- Lógica condicional
- Manejo de variables
- Integración con SharePoint
- Automatización de aprobaciones
- Actualización dinámica de registros

**Fecha de inicio del proyecto:** 16 de febrero de 2026  
**Estado:** En desarrollo  

---

## 🧩 Arquitectura del Sistema

La solución incluye:

1. Microsoft Forms – Envío de solicitud de vacaciones  
2. Lista en SharePoint – Empleados (almacena días disponibles)  
3. Lista en SharePoint – Solicitudes de Vacaciones  
4. Flujo en Power Automate – Validación + Aprobación + Actualización de saldo  

---

## 🔄 Lógica de Negocio

1. El empleado envía solicitud (fecha inicio / fecha fin).
2. El flujo calcula automáticamente los días solicitados.
3. El sistema consulta el saldo disponible en SharePoint.
4. Validación:
   - Si los días solicitados exceden los disponibles → rechazo automático.
   - Si son válidos → se envía a aprobación.
5. Si se aprueba:
   - Se descuentan los días del saldo.
   - Se actualiza el estado de la solicitud.
6. Si se rechaza:
   - Se actualiza el estado.
   - Se envía notificación por correo.

---

## 🎯 Objetivos del Proyecto

- Implementar validación automática de días disponibles.
- Automatizar el proceso de aprobación.
- Actualizar dinámicamente el saldo de vacaciones.
- Documentar arquitectura y flujo para portafolio profesional.

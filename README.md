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

Vacation Request Automation is designed using a decoupled arcchitecture that separates inout, business logic, and data storage.

Flow:
1. Microsoft Forms – Vacation request submission  
2. Power Automate Flow – Validation + Approval + Update logic
3. Excel Online (Data Storage)
4. Email Notifications

The system is intentionally designed to be easly migratable to SharePoint Lists if licensing becomes available.

---

## 🔄 Business Logic

The flow validates vacation requests based on predefined business rules:

1. Each employee has a defined number of available vacation days.
2. Requested days are calculated automatically.
3. If requested days exceed available balance → automatic rejection.
4. If valid → approval request is sent.
5. Upon approval → employee balance is updated.
6. Upon rejection → no balance modification occurs.

---

## 🛠 Technologies Used

- Microsoft Power Automate
- Microsoft Forms
- Excel Online (OneDrive)
- Outlook

---

## 📂 Repository Structure

- /docs
- /docs/images
- /screenshots

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

VacationFlow está diseñado con una arquitectura desacoplada que separa la captura de información, la lógica de negocio y la capa de almacenamiento de datos.

Flujo general:

Microsoft Forms
→ Power Automate
→ Excel Online (OneDrive)
→ Notificaciones por correo (Outlook)

Nota: La arquitectura fue diseñada para permitir migración sencilla a SharePoint Lists en caso de contar con licencia empresarial.

---

## 🔄 Lógica de Negocio

El flujo automatizado valida las solicitudes de vacaciones con base en reglas predefinidas:

1. Cada empleado tiene un número definido de días de vacaciones disponibles.
2. Los días solicitados se calculan automáticamente a partir de la fecha de inicio y fin.
3. Si los días solicitados superan el saldo disponible → la solicitud se rechaza automáticamente.
4. Si la solicitud es válida → se envía a aprobación.
5. Si es aprobada → se actualiza el saldo del empleado.
6. Si es rechazada → no se modifica el saldo.

---

## 🎯 Objetivos del Proyecto

- Implementar validación automática de días disponibles.
- Automatizar el proceso de aprobación.
- Actualizar dinámicamente el saldo de vacaciones.
- Documentar arquitectura y flujo para portafolio profesional.

# VacationFlow

## 🚀 Vacation Request Automation – Power Platform

### 📌 Project Overview (English)

VacationFlow is an automated vacation request management system built using Microsoft Power Platform.

The solution allows employees to submit vacation requests, validates the number of requested days against available vacation balance, and routes valid requests through an approval workflow. If approved, the system automatically updates the employee's remaining vacation days.

This project demonstrates intermediate Power Automate capabilities including:

- Business rule validation
- Custom app development
- Conditional logic
- Variable handling
- Approval workflows
- Dynamic record updates
- Identity-based request association

**Project Start Date:** February 16, 2026  
**Status:** In Development

---

## 🧩 System Architecture

VacationFlow follows a decoupled architecture that separates user interface, business logic, and data storage.

Flow:
1. Microsoft Power Apps – Vacation request submission (Canvas App) 
2. Power Automate Flow – Validation + Approval + Update logic
3. Microsoft Excel Online (OneDrive) – Data storage
4. Microsoft Outlook – Email notifications

The application automatically associates each request with the logged-in user using identity context, reducing manual input errors.

The architecture is designed to be easily migratable to SharePoint Lists or Dataverse if required.

---

## 🔄 Business Logic

The flow validates vacation requests based on predefined business rules:

1. Each employee has a defined number of available vacation days.
2. Requested days are calculated automatically.
3. If requested days exceed available balance → automatic rejection.
4. If valid → approval request is sent.
5. Upon approval → employee balance is updated.
6. Upon rejection → no balance modification occurs.

Users cannot manipulate status values directly. Status changes are controlled exclusively by the automated flow.
---

## 🛠 Technologies Used

- Microsoft Power Automate
- Microsoft Power Apps (Canvas App)
- Excel Online (OneDrive)
- Outlook

---

## 📂 Repository Structure

- /docs
- /docs/images
- /screenshots

Documentation and evidence of the flow design and implementation will be stored in these folders.

---

---

# 🇪🇸 Versión en Español

## 🚀 Automatización de Solicitudes de Vacaciones – Power Platform

### 📌 Descripción General

VacationFlow es un sistema automatizado de gestión de solicitudes de vacaciones desarrollado con Microsoft Power Platform.

Permite a los empleados enviar solicitudes de vacaciones, valida automáticamente los días solicitados contra los días disponibles y envía las solicitudes válidas a un flujo de aprobación. Si la solicitud es aprobada, el sistema descuenta automáticamente los días utilizados del saldo del empleado.

Este proyecto demuestra habilidades intermedias en Power Automate incluyendo:

- Desarrollo de aplicaciones con Power Apps
- Implementación de reglas de negocio
- Automatización de aprobaciones
- Control de estados mediante flujo automatizado
- Actualización dinámica de datos
- Asociación automática del usuario autenticado

**Fecha de inicio del proyecto:** 16 de febrero de 2026  
**Estado:** En desarrollo  

---

## 🧩 Arquitectura del Sistema

La solución está diseñada con una arquitectura desacoplada que separa:
- 1Interfaz de usuario (Power Apps)
- Lógica de negocio (Power Automate)
- Almacenamiento de datos (Excel Online)

Flujo general:

→ Power Apps
→ Power Automate
→ Excel Online (OneDrive)
→ Notificaciones por correo (Outlook)

La arquitectura permite una futura migración a SharePoint Lists o Dataverse sin rediseñar la lógica principal.

---

## 🔄 Lógica de Negocio

El flujo automatizado valida las solicitudes de vacaciones con base en reglas predefinidas:

1. Cada empleado tiene un número definido de días de vacaciones disponibles.
2. Los días solicitados se calculan automáticamente según las fechas.
3. Si los días solicitados superan el saldo → rechazo automático.
4. Si es válida → se envía a aprobación.
5. Si es aprobada → se actualiza el saldo.
6. Si es rechazada → no se modifica el saldo.
7. El estado solo puede ser modificado por el flujo automatizado.

---

## 🎯 Objetivos del Proyecto

- Implementar validación automática de días disponibles.
- Automatizar el proceso de aprobación.
- Actualizar dinámicamente el saldo de vacaciones.
- Documentar arquitectura y flujo para portafolio profesional.

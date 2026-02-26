# VacationFlow

## 🚀 Intelligent Vacation Request Automation – Power Platform

---

## 📌 Executive Summary

VacationFlow is a business process automation solution built with Microsoft Power Platform that digitizes and controls the complete vacation request and approval lifecycle within an organization.

The solution replaces manual email-based or spreadsheet-based processes, ensuring:

- Automated business rule validation  
- Prevention of overlapping vacation periods  
- Real-time vacation balance control  
- Structured approval workflow  
- Full audit traceability  
- Migration-ready architecture  

This project was developed as a professional portfolio case demonstrating real-world automation capabilities for freelance and business environments.

**Project Start Date:** February 16, 2026  
**Status:** Active Development  

---

## 🧩 Solution Architecture

VacationFlow follows a decoupled architecture based on separation of concerns:

| Layer | Technology | Responsibility |
|-------|------------|----------------|
| Interface | Power Apps (Canvas App) | User interaction and first-level validation |
| Business Logic | Power Automate | Critical validation, approval workflow, balance updates |
| Data Storage | Excel Online (OneDrive) | Structured data persistence |
| Notifications | Outlook | Automated email communication |

The architecture is designed to allow future migration to:

- SharePoint Lists  
- Dataverse  

without redesigning core business logic.

---

## 🔄 Business Rules & Logic

The system applies dual-layer validation (Application + Automation) to ensure data integrity.

Key rules implemented:

- Automatic calculation of requested days  
- Available balance validation  
- Overlapping request prevention  
- Single pending request restriction per employee  
- Minimum 5-day advance submission requirement  
- Balance deduction only upon approval  
- Status transitions controlled exclusively by automated flow  
- Real approver registration for audit traceability  

---

## 🎯 What This Project Demonstrates

This solution showcases the ability to:

- Translate business processes into automated logic  
- Design hierarchical approval workflows  
- Implement redundant validations to prevent manual manipulation  
- Apply role-based access simulation (RBAC)  
- Build scalable, migration-ready architectures  
- Deliver structured technical documentation  

---

## 📋 Covered Scenarios

- Valid request within available balance  
- Automatic rejection for exceeded balance  
- Blocking of overlapping date ranges  
- Blocking of multiple pending requests  
- Approval by manager or administrator  
- Automatic balance update upon approval  
- Complete audit trail recording  

---

## 🛠 Technologies Used

- Microsoft Power Apps (Canvas)  
- Microsoft Power Automate  
- Excel Online (OneDrive)  
- Outlook  

---

## 📧 Email Service Consideration

Due to Microsoft licensing limitations in the development environment, Gmail was used as the email notification service instead of Outlook.

This decision does not impact the core architecture, as the notification layer is fully replaceable. In a production environment with appropriate licensing, Outlook or Microsoft Exchange would be the standard integration.

The solution was intentionally designed to keep the notification mechanism modular, allowing seamless replacement without affecting business logic.

---

## 📂 Repository Structure

- `/docs` → Detailed technical documentation  
- `/docs/images` → Flow diagrams and ER model  
- `/screenshots` → Application visual evidence  

---

## 🔮 Potential Extensions

- Multi-level approval workflow  
- Outlook calendar integration  
- Power BI dashboard reporting  
- Migration to SharePoint or Dataverse  
- Department-based leave policies  

---

---

# 🇪🇸 Versión en Español

## 🚀 Automatización Inteligente de Solicitudes de Vacaciones – Power Platform

---

## 📌 Resumen Ejecutivo

VacationFlow es una solución de automatización de procesos desarrollada con Microsoft Power Platform que digitaliza y controla el ciclo completo de solicitud y aprobación de vacaciones dentro de una organización.

La solución reemplaza procesos manuales basados en correo electrónico o archivos compartidos, asegurando:

- Validación automática de reglas de negocio  
- Prevención de superposición de periodos  
- Control de saldo en tiempo real  
- Flujo de aprobación estructurado  
- Trazabilidad completa  
- Arquitectura preparada para migración futura  

Este proyecto fue desarrollado como caso profesional de portafolio para demostrar capacidades reales en automatización empresarial orientada a entornos freelance y corporativos.

**Fecha de inicio:** 16 de febrero de 2026  
**Estado:** Desarrollo activo  

---

## 🧩 Arquitectura de la Solución

VacationFlow implementa una arquitectura desacoplada basada en separación de responsabilidades:

| Capa | Tecnología | Responsabilidad |
|------|------------|----------------|
| Interfaz | Power Apps (Canvas App) | Interacción del usuario y validación inicial |
| Lógica de negocio | Power Automate | Validaciones críticas, flujo de aprobación y actualización de saldo |
| Almacenamiento | Excel Online (OneDrive) | Persistencia estructurada de datos |
| Notificaciones | Outlook | Comunicación automática por correo |

La arquitectura permite migración futura a:

- SharePoint Lists  
- Dataverse  

sin necesidad de rediseñar la lógica central.

---

## 🔄 Reglas y Lógica de Negocio

El sistema aplica validaciones en dos niveles (Aplicación + Automatización) para garantizar integridad de datos.

Reglas principales implementadas:

- Cálculo automático de días solicitados  
- Validación de saldo disponible  
- Prevención de solicitudes superpuestas  
- Restricción de una sola solicitud pendiente por empleado  
- Envío obligatorio con al menos 5 días de anticipación  
- Descuento de saldo únicamente tras aprobación  
- Control total de estados gestionado exclusivamente por el flujo automatizado  
- Registro del aprobador real para trazabilidad  

---

## 🎯 ¿Qué demuestra este proyecto?

Esta solución evidencia capacidad para:

- Traducir procesos de negocio en lógica automatizada  
- Diseñar flujos de aprobación jerárquicos  
- Implementar validaciones redundantes para evitar manipulación manual  
- Aplicar control de acceso basado en roles (RBAC)  
- Diseñar arquitecturas escalables y migrables  
- Documentar soluciones técnicas con enfoque profesional  

---

## 📋 Escenarios Cubiertos

- Solicitud válida dentro del saldo disponible  
- Rechazo automático por exceso de días  
- Bloqueo por superposición de fechas  
- Bloqueo por solicitud pendiente existente  
- Aprobación por gerente o administrador  
- Actualización automática de saldo tras aprobación  
- Registro completo para auditoría  

---

## 🛠 Tecnologías Utilizadas

- Microsoft Power Apps (Canvas)  
- Microsoft Power Automate  
- Excel Online (OneDrive)  
- Outlook  

---

## 📧 Consideración sobre el Servicio de Correo

Debido a limitaciones de licenciamiento de Microsoft en el entorno de desarrollo, se utilizó Gmail como servicio de notificaciones en lugar de Outlook.

Esta decisión no afecta la arquitectura principal, ya que la capa de notificaciones es completamente reemplazable. En un entorno productivo con licencias adecuadas, Outlook o Microsoft Exchange serían la integración estándar.

La solución fue diseñada manteniendo el mecanismo de notificación desacoplado, permitiendo su sustitución sin afectar la lógica de negocio.

---

## 📂 Estructura del Repositorio

- `/docs` → Documentación técnica detallada  
- `/docs/images` → Diagramas de flujo y modelo ER  
- `/screenshots` → Evidencia visual de la aplicación  

---

## 🔮 Posibles Extensiones

- Aprobación multinivel  
- Integración con calendario corporativo  
- Dashboard en Power BI  
- Migración a SharePoint o Dataverse  
- Políticas diferenciadas por departamento  

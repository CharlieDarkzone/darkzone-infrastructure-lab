# 00 - Introducción: Infraestructura Active Directory Empresarial

## 🎯 Propósito del Proyecto

Este laboratorio representa la evolución desde un entorno de fundamentos de Active Directory hacia un modelo de Infraestructura orientado a empresa mediana/grande.

El enfoque deja de ser:

> Configurar políticas y usuarios

y pasa a ser:

> Diseñar, gobernar y proteger la infraestructura de identidad corporativa.

---

## 🏢 Escenario Objetivo

El diseño de este laboratorio simula una organización con:

- 800 usuarios
- 120 servidores
- 3 administradores de infraestructura
- 1 proveedor externo de ciberseguridad (SOC / EDR)
- Entorno híbrido Windows + Linux

El objetivo no es instalar servicios, sino diseñar correctamente la arquitectura de privilegios y control.

---

## 🧠 Cambio de Enfoque

En el proyecto anterior (Fundamentos) se trabajó:

- OU
- GPO
- Filtrado por grupos
- Modelo de excepciones
- Gobierno básico

En este proyecto se abordará:

- Modelo de privilegios por niveles (Tiering)
- Delegación estructurada
- Hardening del Domain Controller
- Administración segura
- Auditoría avanzada
- Separación de funciones
- Reducción de superficie de ataque

---

## 🔐 Principios de Diseño

Este laboratorio se basará en:

- Principio de mínimo privilegio
- Separación de roles administrativos
- Prevención de movimiento lateral
- Arquitectura escalable
- Gobernanza y trazabilidad

---

## 📌 Objetivo Profesional

Este proyecto está orientado a construir un perfil de:

> Administrador de Infraestructura / Identity & Access Management

Capaz de diseñar y defender arquitectura ante auditorías internas y externas.

---

## 🚀 Próximo Paso

Diseñar el modelo de privilegios por niveles:

01 - Modelo Tier 0 / Tier 1 / Tier 2
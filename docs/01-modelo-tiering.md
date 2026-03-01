# 01 - Modelo de Privilegios por Niveles (Tiering Model)

## 🎯 Objetivo

Diseñar una arquitectura de privilegios que reduzca el riesgo de movimiento lateral y proteja los activos críticos del dominio.

En entornos empresariales grandes, no todos los administradores deben tener acceso a todo.

Se implementa un modelo de separación por niveles (Tier Model).

---

# 🏗️ ¿Qué es el Tiering Model?

El Tiering Model divide la infraestructura en niveles de confianza:

## 🔴 Tier 0 – Identidad Crítica

Incluye:

- Domain Controllers
- Active Directory
- Cuentas Domain Admin
- Servicios de autenticación
- PKI (si existe)

Si Tier 0 se compromete, toda la empresa está comprometida.

---

## 🟠 Tier 1 – Servidores

Incluye:

- Application Servers
- File Servers
- SQL Servers
- Infraestructura interna

Administradores de servidores NO deben tener privilegios sobre Tier 0.

---

## 🟢 Tier 2 – Workstations

Incluye:

- Equipos de usuario final
- Callcenter
- PCs corporativos

Administradores de estaciones NO deben administrar servidores ni Domain Controllers.

---

# 🚨 Problema que Resuelve

Sin separación por niveles:

- Un administrador inicia sesión en un PC comprometido.
- Sus credenciales privilegiadas quedan en memoria.
- El atacante extrae credenciales.
- Movimiento lateral hacia servidores o Domain Controller.

El Tiering Model rompe esa cadena.

---

# 🔐 Principio Clave

Un administrador solo puede administrar su propio nivel o inferiores, nunca superiores.

Ejemplo:

- Admin Tier 2 → Solo Workstations
- Admin Tier 1 → Servidores
- Admin Tier 0 → Domain Controllers

Nunca mezclar.

---

# 📌 Próximo Paso

Diseñar la estructura de grupos y OU alineada con el modelo Tiering.

---

## 🌍 English Summary

The Tiering Model is a privilege separation architecture designed to reduce lateral movement risk in enterprise Active Directory environments.

Tier 0 protects identity infrastructure such as Domain Controllers and privileged accounts.

Tier 1 manages servers, while Tier 2 manages workstations.

Administrators must never cross tiers upward, preventing credential exposure and reducing attack surface.

This model is essential in medium and large enterprise environments.
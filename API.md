# 🔌 Especificación Técnica y API — Wanos_GMGenie

[![GitHub](https://img.shields.io/badge/GitHub-DarckRovert%2FWanos_GMGenie-black?logo=github)](https://github.com/DarckRovert/Wanos_GMGenie)
[![Ecosistema](https://img.shields.io/badge/Ecosistema-WoW%20Per%C3%BA%203.3.5a-gold.svg)](https://projectjaina.com/)

## 📌 Resumen Arquitectónico
Herramienta integral de soporte y administración para GMs con gestión de tickets, teletransporte, inspección silenciosa de jugadores y despacho protegido de comandos.

- **Rol en el Ecosistema:** Módulo Oficial #6 — Herramientas Staff / GM
- **Archivo Principal TOC:** `GMGenie.toc`
- **Compatibilidad del Motor:** World of Warcraft 3.3.5a (Build 12340)

---

## ⌨️ Comandos de Consola (Slash Commands)
- `/tickets`: Acceso principal o comando del addon.
- `/spy`: Acceso principal o comando del addon.
- `/builder`: Acceso principal o comando del addon.
- `/spawns`: Acceso principal o comando del addon.

---

## 📡 Protocolo de Red y Eventos
- `GMGenie_Sync`: Prefijo registrado para sincronización de datos.
- `GMGenie_TicketSync`: Prefijo registrado para sincronización de datos.

### Eventos del Motor 3.3.5a Gestionados
- `PLAYER_LOGIN` / `ADDON_LOADED`: Inicialización atómica de tablas de configuración y hooks.
- `PLAYER_ENTERING_WORLD`: Sincronización de estado tras transiciones de pantalla o mapa.
- `PLAYER_LOGOUT`: Guardado seguro en disco de las variables locales.

---

## 💾 Persistencia de Datos (SavedVariables)
- `GMGenie_SavedVars`: Almacenamiento estructurado de configuración y estado persistente.

---

## 🛠️ Buenas Prácticas de Integración
1. Toda invocación a funciones públicas debe verificar previamente la existencia del espacio de nombres en `_G`.
2. Las tablas de configuración deben consultarse en modo lectura sin sobreescribir valores por omisión no validados.
3. El intercambio de datos con otros addons debe efectuarse a través del bus oficial `Wanos_Companion` o hooks de eventos estándar.

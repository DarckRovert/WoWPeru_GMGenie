# Registro de Cambios — Wanos_GMGenie

Todos los cambios notables de este proyecto están documentados en este archivo siguiendo el estándar [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/).

---

## [1.0.0-AzerothCore-wp] — 2026-10-05
### Correcciones Críticas de Seguridad y Red (Project Jaina)
- **Eliminación de Fuga de Comandos GM en Chat Público:** Reemplazado el envío de comandos administrativos vía `SendChatMessage` por inyección directa a la consola de comandos de FrameXML (`ChatFrameEditBox:SetText` / `ChatEdit_SendText`), evitando que comandos sensibles o erróneos se transmitan como texto plano en canales públicos.
- **Corrección de Firma `CHAT_MSG_ADDON` en Tickets:** Ajustada la lista de argumentos en el manejador de eventos de `GMGenie_Tickets` para compatibilidad exacta con la firma de WotLK 3.3.5a, eliminando el crash por concatenación de `nil` que afectaba a todos los clientes de Game Master conectados.
- **Reparación de `markAsUnread`:** Corregida la referencia a tabla no inicializada en `markAsUnread`.
- **Blindaje de Emisiones de Hermandad:** Añadida guardia `IsInGuild()` previa a cualquier broadcast de tickets para evitar errores de red en personajes GM sin hermandad.
- **Higiene Documental:** Adición de `CHANGELOG.md`, `ECOSYSTEM_REGISTRY.md` y `.gitattributes`.

---

## [1.0.0-AzerothCore] — Upstream (Chocochaos / Adaptación AzerothCore)
### Suite Administrativa Base
- Panel de gestión y visualización de tickets de jugadores.
- Módulos de spawns de NPCs/GameObjects y utilidades de teletransporte rápido.
- HUD administrativo con monitor de estado y Spy de canales.
- Librería Chronos integrada para gestión de temporizadores asíncronos.

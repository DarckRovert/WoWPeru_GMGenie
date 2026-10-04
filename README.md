# GMGenie — Game Master Genie para WoW Perú

> **WoW Perú Ecosystem** · WotLK 3.3.5a compatible · `Interface: 30300`  
> Fork de [Game Master Genie](https://www.curse.com/addons/wow/game-master-genie) por Chocochaos — Adaptado para AzerothCore/WoW Perú por DarckRovert

Suite completa de herramientas para **Game Masters** de WoW Perú sobre AzerothCore. Combina múltiples paneles (tickets, spawns, HUD, disciplina, teleports) en una interfaz unificada diseñada para la gestión eficiente del servidor.

---

## Características

### Gestión de Tickets
- Visualización y respuesta a tickets de jugadores en tiempo real.
- Sistema de categorización y prioridades.

### Sistema de Spawns
- Panel de spawn de NPCs y objetos con coordenadas.
- Base de datos de spawns frecuentes.

### HUD de GM
- Overlay de información del GM visible solo con `.gm on`.
- Estado del servidor, jugadores online, alertas.

### Macros GM
- **Disciplina** — Macros de sanciones (warn, mute, ban).
- **Teleports** — Teletransporte rápido a zonas clave.
- **Mail** — Envío masivo de correos de anuncio.
- **Whispers** — Plantillas de respuesta rápida.

### Spy
- Monitoreo de canales de chat para detección de comportamiento.

---

## Instalación

Solo para cuentas GM en servidores WoW Perú.

1. Copia `GMGenie` a `Interface/AddOns/`.
2. Requiere `.gm on` para acceder a los paneles.
3. Los sub-addons de `Chronos/` se cargan automáticamente.

## Variables Guardadas

- `GMGenie_SavedVars` — Configuración global, layouts de paneles, macros personalizados.

## Estructura

```
GMGenie/
├── GMGenie.lua         # Core del addon
├── GMGenie.xml         # Frames principales
├── Hud.lua/.xml        # HUD overlay
├── Tickets.lua/.xml    # Sistema de tickets
├── Spawns.lua/.xml     # Panel de spawns
├── Spy.lua/.xml        # Monitor de chat
├── Macros.*.lua        # Módulos de macros
├── Options/            # Paneles de configuración
├── Chronos/            # Librería de timers
└── Textures/           # Recursos gráficos
```

## Créditos

- **Autor original:** Chocochaos (GPL v3)
- **Adaptación WoW Perú:** DarckRovert (Elnazzareno)
- **Versión:** 1.0.0-AzerothCore
- **Licencia:** GNU General Public License v3.0

---

*Parte del [ecosistema WoW Perú](https://github.com/DarckRovert)*
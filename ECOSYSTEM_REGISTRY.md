# 🌐 Registro de Ecosistema — WoWPeru_GMGenie

Ficha técnica oficial de registro en la infraestructura multi-addon de **WoW Perú - Reino Andino**.

---

## 1. Identidad del Addon

| Campo | Valor |
|---|---|
| **Nombre Técnico** | `WoWPeru_GMGenie` |
| **Título en Cliente** | `GM Genie [WoW Perú]` |
| **Versión** | `1.0.0-AzerothCore` |
| **Tipo de Sistema** | Suite Administrativa para Staff y Game Masters (Client-Side con Privilegios GM) |
| **Repositorio GitHub** | [DarckRovert/WoWPeru_GMGenie](https://github.com/DarckRovert/WoWPeru_GMGenie) |
| **Directorio de Instalación** | `Interface\AddOns\GMGenie\` |

---

## 2. Red y Mensajería de Addon

| Propiedad | Valor |
|---|---|
| **Prefijo Oficial** | `GMGenie` |
| **Canales de Red** | `GUILD`, `WHISPER` |
| **OpCodes Manejados** | Sincronización P2P de tickets entre miembros del staff (`TICKETS:SYNC`, `TICKETS:CLAIM`, etc.) |
| **Presupuesto Máximo** | < 180 bytes por paquete |
| **Seguridad de Red** | Requiere membresía activa en hermandad del staff y rol GM en el servidor |

---

## 3. Persistencia de Datos

| Variable Global | Tipo | Ámbito | Propósito |
|---|---|---|---|
| `GMGenie_SavedVars` | Tabla Lua (`SavedVariables`) | Por Cuenta | Guarda preferencias de paneles, plantillas de tickets y coordenadas de spawns. |

---

## 4. Matriz de Integración del Ecosistema

| Sistema Coexistente | Modo de Interacción | Flujo de Datos |
|---|---|---|
| **AzerothCore Worldserver** | Inyección de Comandos | Envía comandos administrativos (`.ticket`, `.appear`, `.summon`, `.mute`, etc.) mediante la consola de FrameXML. |
| **`IntiObjGPS`** | Coexistencia GM | Permite combinar la localización precisa de objetos con las herramientas de spawn de GMGenie. |

---

## 5. Garantías de Rendimiento

- **Tiempo de Cuadro:** < 0.03 ms por frame (paneles ocultos por defecto hasta invocar `.gm on`).
- **Memoria en Tiempo de Ejecución:** ~ 1.2 MB de memoria Lua.
- **Compatibilidad de Hardware:** 100% verificado para estaciones de trabajo del staff.

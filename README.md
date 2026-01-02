# NuvikShop Keys

<p align="center">
  <img width="271" height="48" alt="Captura de pantalla 2026-01-02 112426" src="https://github.com/user-attachments/assets/1f992e29-c1d3-4636-98df-3c0d3510b0a1" alt="NuvikShop Keys Banner">
</p>


<p align="center">
  <b>Sistema Profesional de Keys para tu Tienda de Minecraft</b><br>
  Versión 1.0.0 | Por Nuvik
</p>

---

## 📋 Descripción

**NuvikShop Keys** es un plugin que te permite generar y gestionar keys de productos para tu servidor de Minecraft. Perfecto para integrar con tiendas como **SellAuth**, **Tebex** o cualquier sistema de comercio electrónico.

## ✨ Características

- ✅ **Multi-Database** - Soporta SQLite, MySQL, H2 y Supabase (PostgreSQL)
- ✅ **Keys Personalizables** - Formato configurable (NUVIK-XXXXX-XXXXX)
- ✅ **Comandos Predefinidos** - Configura rangos, kits, coins y más
- ✅ **Integración SellAuth** - Webhook para automatizar la entrega
- ✅ **Sistema de Seguridad** - Cooldowns, anti-spam y bloqueo temporal
- ✅ **GUI Interactivo** - Gestiona keys visualmente
- ✅ **Efectos Visuales** - Sonidos y partículas al canjear
- ✅ **Mensajes Personalizables** - Todo configurable en messages.yml

## ⌨️ Comandos

| Comando | Descripción | Permiso |
|---------|-------------|---------|
| `/redeem <key>` | Canjear una key | `nuvikshop.redeem` |
| `/keygen <tipo> [cantidad]` | Generar keys | `nuvikshop.admin` |
| `/keylist [página]` | Ver todas las keys | `nuvikshop.admin` |
| `/keyinfo <key>` | Ver información de key | `nuvikshop.admin` |
| `/keydelete <key>` | Eliminar una key | `nuvikshop.admin` |
| `/nuvik reload` | Recargar configuración | `nuvikshop.admin` |
| `/nuvik status` | Ver estado del plugin | `nuvikshop.admin` |

## 🔑 Permisos

```
nuvikshop.redeem  - Permite canjear keys (default: true)
nuvikshop.admin   - Acceso a comandos de administración (default: op)
nuvikshop.*       - Acceso completo al plugin (default: op)
```

## 🗄️ Bases de Datos

| Tipo | Descripción |
|------|-------------|
| **SQLite** | Base de datos local en archivo |
| **MySQL** | Base de datos remota |
| **H2** | Base de datos embebida rápida |
| **Supabase** | PostgreSQL en la nube |

## ⚙️ Configuración Rápida

```yaml
database:
  type: "SUPABASE"
  
  supabase:
    host: "tu-proyecto.supabase.co"
    port: 5432
    database: "postgres"
    username: "postgres.tu-proyecto"
    password: "tu-password"
    schema: "public"

keys:
  format: "NUVIK-%random%-%random%"
  random-length: 5

predefined-commands:
  vip:
    command: "lp user %player% parent set vip"
    description: "Rango VIP"
```

## 🚀 Instalación

1. Descarga `NuvikShopKeys.jar`
2. Colócalo en `plugins/`
3. Reinicia el servidor
4. Configura `config.yml`
5. `/nuvik reload`

## 📝 Requisitos

- **Minecraft:** 1.20.x+
- **Java:** 17+
- **Servidor:** Spigot, Paper, Purpur

---

<p align="center">
  Desarrollado con ❤️ por <b>Nuvik</b>
</p>

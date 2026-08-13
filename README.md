# Módulo de Envío Masivo por WhatsApp y Correo (CodeIgniter 4)

Módulo integral desarrollado en **CodeIgniter 4** para la administración de contactos, segmentación por grupos y automatización de envíos masivos e individuales de notificaciones mediante **WhatsApp** y **correo electrónico**, incluyendo registro detallado de *logs* de envío y normalización de números telefónicos.

---

## 🚀 Características Principales

* **Gestión de Contactos:**
  * Almacenamiento de datos clave: Nombres, Apellidos, DNI, Celular, Correo y Grupo/Segmento.
  * Seguimiento de estados independientes para WhatsApp y Correo (`estado_whatsapp`, `estado_correo`).
* **Normalización Automática:**
  * Limpieza y formateo de números celulares según el formato estándar requerido para el envío de mensajería (ej. APIs como Factiliza).
* **Auditoría y Logs de Envío:**
  * Registro histórico de cada intento de envío (`EnvioLogModel`) para monitoreo de entregas, errores y estado actual del proceso.
* **Integración Modular:**
  * Diseñado de forma limpia dentro de la arquitectura de modelos y controladores de CodeIgniter 4.

---

## 🛠️ Tecnologías Utilizadas

* **Framework:** CodeIgniter 4 (PHP 8.x)
* **Base de Datos:** MySQL / MariaDB
* **Integraciones:** APIs de mensajería (Factiliza / WhatsApp Service) y SMTP de correo

---

## 📋 Estructura de la Base de Datos

### Tabla: `contactos`

| Campo | Tipo | Descripción |
| :--- | :--- | :--- |
| `id` | `INT` (PK, Auto Increment) | Identificador único |
| `nombres` | `VARCHAR` | Nombre(s) del contacto |
| `apellidos` | `VARCHAR` | Apellido(s) del contacto |
| `dni` | `VARCHAR` | Documento de Identidad |
| `celular` | `VARCHAR` | Número telefónico normalizado |
| `correo` | `VARCHAR` | Dirección de correo electrónico |
| `grupo` | `VARCHAR` | Categoría o segmento |
| `estado_whatsapp` | `VARCHAR` / `TINYINT` | Estado del último envío por WhatsApp |
| `estado_correo` | `VARCHAR` / `TINYINT` | Estado del último envío por Correo |
| `created_at` | `DATETIME` | Fecha de creación |
| `updated_at` | `DATETIME` | Fecha de actualización |

---

## ⚙️ Configuración e Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)

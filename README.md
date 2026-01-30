# QRAcademy 🎓📱

<div align="center">
  <img src="https://img.shields.io/badge/Status-Development-orange?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/Platform-Mobile%20(iOS%20%26%20Android)-blue?style=for-the-badge&logo=react" alt="Platform" />
  <img src="https://img.shields.io/badge/Backend-Supabase-green?style=for-the-badge&logo=supabase" alt="Backend" />
</div>

<br />

**QRAcademy** es una solución **SaaS (Software as a Service)** de vanguardia diseñada para transformar el control de asistencia en academias y centros educativos. Mediante tecnología de códigos QR, eliminamos la fricción administrativa, automatizamos el seguimiento de puntualidad y proporcionamos datos accionables en tiempo real tanto para tutores como para administradores.

---

## 🚀 Propuesta de Valor

En el entorno educativo tradicional, el control de asistencia es lento y propenso a errores. **QRAcademy** resuelve esto:
- **Agilidad Extrema:** Elimina las colas de ingreso mediante un escaneo instantáneo.
- **Precisión Total:** Reduce el error humano y evita registros falsificados.
- **Transparencia:** Dashboard en tiempo real para una gestión administrativa eficiente y basada en datos.

---

## ✨ Características Principales

### 📱 Experiencia del Tutor
- **Escáner de Alta Velocidad:** Integración nativa con la cámara para una respuesta inmediata.
- **Validación Inteligente:** Alertas visuales inmediatas sobre el estado del alumno (ej. pagos pendientes, alertas médicas).
- **Registro Automático:** Sincronización instantánea con la base de datos centralizada.

### 📊 Gestión Administrativa
- **Autenticación Multi-tenant:** Cada centro educativo gestiona su propio ecosistema de forma aislada y segura.
- **Panel de Métricas:** Visualización de asistencia diaria, porcentajes de puntualidad y tendencias por aula.
- **Gestión de Alumnos:** Administración centralizada de base de datos y generación de QRs únicos.

---

## 🛠️ Stack Tecnológico

| Componente | Tecnología |
| :--- | :--- |
| **Frontend** | [React Native](https://reactnative.dev/) + [Expo](https://expo.dev/) (SDK 54) |
| **Arquitectura** | [Expo Router](https://docs.expo.dev/router/introduction/) (File-based routing) |
| **Estilos** | [NativeWind](https://www.nativewind.dev/) (Tailwind CSS) |
| **Backend** | [Supabase](https://supabase.com/) (PostgreSQL & Auth) |
| **Iconografía** | Lucide React Native |

---

## 🏗️ Modelado de Datos (Sugerido)

El sistema utiliza una estructura relacional optimizada en Supabase para soportar multi-tenancy:

| Tabla | Descripción |
| :--- | :--- |
| `academias` | Entidades B2B (ID, Nombre, Configuración, Plan). |
| `estudiantes` | Datos personales, QR Code único y FK a `academias`. |
| `asistencias` | Logs de `estudiante_id`, `fecha`, `hora`, `estado` (Puntual/Tardanza). |
| `tutores` | Perfiles de usuario con acceso a escaneo, vinculados a una academia. |

---

## ⚡ Hoja de Ruta (Backlog)

Vemos un futuro donde la comunicación es clave:
- [ ] **Fase 2: Integración WhatsApp:** Notificaciones automáticas a padres sobre ingresos y tardanzas.
- [ ] **Fase 3: Reportes PDF:** Generación mensual de reportes de asistencia para facturación y auditoría.
- [ ] **Fase 4: Offline Mode:** Capacidad de escanear sin conexión y sincronizar posteriormente.

---

## ⚙️ Instalación y Configuración

Sigue estos pasos para poner el proyecto en marcha en tu entorno local:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/QRAcademy.git
   cd QRAcademy
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno:**
   Crea un archivo `.env` en la raíz con tus credenciales de Supabase:
   ```env
   EXPO_PUBLIC_SUPABASE_URL=tu_url_aqui
   EXPO_PUBLIC_SUPABASE_ANON_KEY=tu_key_aqui
   ```

4. **Iniciar el entorno de desarrollo:**
   ```bash
   npx expo start
   ```

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---

<div align="center">
  Desarrollado con ❤️ para modernizar la educación.
</div>

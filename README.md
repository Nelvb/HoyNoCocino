# 🍽️ Hoy No Cocino

**Plataforma full-stack de reservas de restaurantes** que conecta comensales con restaurantes, permitiendo gestionar reservas, menús y disponibilidad de forma ágil y profesional.

🌐 **En producción:** [hoynococino.es](https://hoynococino.es)

---

## 📋 Descripción

Hoy No Cocino es una aplicación web completa que digitaliza el sistema de reservas para restaurantes. Ofrece una experiencia moderna tanto para clientes que buscan dónde comer como para propietarios que necesitan gestionar su negocio de forma eficiente.

### ✨ Características principales

**Para Clientes:**
- 🔐 Registro e inicio de sesión seguro
- 🔍 Exploración de restaurantes con filtros y búsqueda
- 📅 Sistema de reservas (crear, editar, cancelar)
- ⭐ Gestión de favoritos
- 👤 Panel personal con historial de reservas
- 📧 Confirmaciones por email
- ✏️ Edición de perfil

**Para Restauradores:**
- 🏢 Panel de administración completo
- 🍴 Gestión de información del restaurante
- 🕐 Configuración de horarios y disponibilidad
- 📸 Galería de fotos
- 🍕 Gestión de menú y platos
- 📊 Control de reservas recibidas
- 📝 Edición completa de datos

---

## 🛠️ Stack Tecnológico

### Frontend
- **React.js** - Biblioteca de UI
- **Webpack** - Bundler
- **Bootstrap** - Framework CSS
- **JavaScript ES6+**

### Backend
- **Python 3.x**
- **Flask** - Framework web
- **Flask-JWT** - Autenticación y autorización
- **SQLAlchemy** - ORM
- **Alembic** - Migraciones de base de datos
- **Flask-Mail** - Envío de emails

### Base de Datos
- **PostgreSQL** - Base de datos relacional

### Deployment
- **Render** - Hosting (frontend + backend)
- **Dominio personalizado:** hoynococino.es

---

## 🚀 Instalación y Configuración

### Prerrequisitos

- Python 3.10+
- Node.js 14+
- PostgreSQL
- Pipenv

### Backend

1. **Instalar dependencias:**
   ```bash
   pipenv install
   ```

2. **Configurar variables de entorno:**
   ```bash
   cp .env.example .env
   ```

3. **Configurar DATABASE_URL en `.env`:**

   | Motor      | Ejemplo de URL                                          |
   |------------|---------------------------------------------------------|
   | SQLite     | `sqlite:////test.db`                                    |
   | MySQL      | `mysql://username:password@localhost:3306/database`     |
   | PostgreSQL | `postgres://username:password@localhost:5432/database`  |

4. **Ejecutar migraciones:**
   ```bash
   pipenv run migrate
   pipenv run upgrade
   ```

5. **Poblar la base de datos (opcional):**
   ```bash
   pipenv run insert-test-data
   ```

6. **Iniciar servidor backend:**
   ```bash
   pipenv run start
   ```

### Frontend

1. **Instalar dependencias:**
   ```bash
   npm install
   ```

2. **Iniciar servidor de desarrollo:**
   ```bash
   npm run start
   ```

---

## 📁 Estructura del Proyecto

```
hoy-no-cocino/
├── src/
│   ├── api/              # Backend Flask
│   │   ├── models.py     # Modelos de base de datos
│   │   ├── routes.py     # Endpoints de la API
│   │   ├── commands.py   # Comandos CLI
│   │   └── utils.py      # Utilidades
│   └── front/            # Frontend React
│       ├── js/
│       │   ├── component/  # Componentes reutilizables
│       │   ├── pages/      # Vistas principales
│       │   └── store/      # Estado global
│       └── styles/         # Estilos CSS
├── migrations/           # Migraciones de Alembic
├── .env.example         # Variables de entorno de ejemplo
└── README.md
```

---

## 🔑 Comandos Útiles

### Backend

```bash
# Crear nueva migración
pipenv run migrate

# Aplicar migraciones
pipenv run upgrade

# Revertir última migración
pipenv run downgrade

# Insertar usuarios de prueba
flask insert-test-users 5

# Insertar datos de prueba
pipenv run insert-test-data
```

### Frontend

```bash
# Modo desarrollo
npm run start

# Build para producción
npm run build
```

---

## 🌐 Despliegue

La aplicación está configurada para desplegarse fácilmente en **Render**:

1. Conecta tu repositorio de GitHub
2. Configura las variables de entorno
3. Render detectará automáticamente Flask y React
4. La aplicación estará disponible en tu dominio

📚 [Documentación completa de despliegue](https://start.4geeksacademy.com/deploy)

---

## 🗄️ Modelos de Base de Datos

El proyecto incluye los siguientes modelos principales:

- **Users** - Usuarios del sistema (clientes y restauradores)
- **Restaurants** - Información de restaurantes
- **Dishes** - Platos del menú
- **Schedules** - Horarios de apertura
- **Reservations** - Reservas realizadas
- **Favorites** - Favoritos de usuarios

---

## 🔒 Seguridad

- Autenticación basada en JWT
- Roles de usuario (cliente/restaurador)
- Protección de rutas sensibles
- Validación de datos en frontend y backend
- Variables de entorno para datos sensibles

---

## 📝 Notas Importantes

### Base de Datos en Entornos de Desarrollo

Cada entorno (GitHub Codespaces, local, etc.) tendrá su propia base de datos. Los datos **no se comparten** entre entornos. Para facilitar el desarrollo, utiliza el comando `insert-test-data` para poblar tu base de datos automáticamente.

### PostgreSQL en Codespaces

```bash
psql -h localhost -U gitpod example
```

---

## 🤝 Contribuciones

Este proyecto fue desarrollado como parte del bootcamp de [4Geeks Academy](https://4geeksacademy.com).

---

## 📄 Licencia

Este proyecto está bajo licencia MIT.

---

## 📧 Contacto

Para más información sobre el proyecto, no dudes en contactar.

---

**Hecho con ❤️ para revolucionar las reservas de restaurantes**

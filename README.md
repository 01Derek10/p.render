# Gestor de Facturación y Clientes - ProyectoRender

Una aplicación web moderna para la gestión integral de clientes, facturas e incidencias. Desarrollada con **Laravel 12**, **Vite**, y **Tailwind CSS**, con soporte para despliegue en **Render**.

## 🚀 Características Principales

- **Gestión de Clientes**: Crear, actualizar, eliminar y visualizar clientes
- **Gestión de Facturas**: Sistema completo de facturación con seguimiento
- **Sistema de Incidencias**: Registro y seguimiento de incidencias de clientes
- **Dashboard**: Panel de control interactivo con estadísticas
- **Autenticación**: Sistema de login seguro con sesiones
- **Despliegue Render**: Configuración lista para producción en Render

## 📋 Requisitos

- PHP 8.2 o superior
- Composer
- Node.js 18+ y npm
- Base de datos (MySQL/PostgreSQL)
- Git

## 🛠️ Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/01Derek10/p.render.git
cd p.render
```

### 2. Instalar dependencias de PHP

```bash
composer install
```

### 3. Configurar variables de entorno

```bash
cp .env.example .env
php artisan key:generate
```

Edita el archivo `.env` con tu configuración de base de datos:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=proyectorender
DB_USERNAME=root
DB_PASSWORD=
```

### 4. Instalar dependencias de Node.js

```bash
npm install
```

### 5. Ejecutar migraciones

```bash
php artisan migrate
```

### 6. (Opcional) Ejecutar seeders para datos de prueba

```bash
php artisan db:seed
```

## 📦 Estructura del Proyecto

```
proyecto/
├── app/
│   ├── Http/Controllers/       # Controladores (Clientes, Facturas, Incidencias)
│   └── Models/                 # Modelos (Cliente, Factura, Incidencia)
├── database/
│   ├── migrations/             # Migraciones de BD
│   └── seeders/                # Seeders de datos
├── resources/
│   ├── views/                  # Vistas Blade
│   │   ├── clientes/           # Vistas de gestión de clientes
│   │   ├── facturas/           # Vistas de gestión de facturas
│   │   ├── incidencias/        # Vistas de gestión de incidencias
│   │   └── dashboard/          # Vistas del dashboard
│   ├── css/                    # Estilos CSS/Tailwind
│   └── js/                     # Scripts JavaScript
├── routes/
│   └── web.php                 # Rutas web
└── storage/                    # Almacenamiento de archivos
```

## 🏃 Uso

### Desarrollo Local

Ejecutar servidor de desarrollo con hot reload:

```bash
npm run dev
```

En otra terminal, ejecutar el servidor Laravel:

```bash
php artisan serve
```

La aplicación estará disponible en `http://localhost:8000`

### Compilación de producción

```bash
npm run build
php artisan migrate --force
```

## 🌐 Despliegue en Render

El proyecto incluye configuración específica para Render:

- `Procfile`: Define los procesos para Render
- `start-render.sh`: Script de inicio para Render
- `.env.render`: Variables de entorno para producción

Consulta [RENDER_DEPLOY.md](RENDER_DEPLOY.md) para instrucciones detalladas de despliegue.

### Variables de entorno en Render

Configura las siguientes variables en Render:

```
APP_NAME=ProyectoRender
APP_ENV=production
APP_DEBUG=false
DB_CONNECTION=pgsql
DB_HOST=<tu-host-db>
DB_PORT=5432
DB_DATABASE=<tu-bd>
DB_USERNAME=<tu-usuario>
DB_PASSWORD=<tu-contraseña>
```

## 🧪 Testing

Ejecutar los tests:

```bash
php artisan test
```

Con cobertura de código:

```bash
php artisan test --coverage
```

## 🗄️ Base de Datos

### Tablas principales

- **users**: Usuarios del sistema
- **clientes**: Información de clientes
- **facturas**: Registros de facturas
- **incidencias**: Reporte de incidencias

### Migraciones

Las migraciones se ejecutan automáticamente con:

```bash
php artisan migrate
```

## 📚 API Endpoints

### Clientes
- `GET /clientes` - Listar clientes
- `GET /clientes/{id}` - Ver detalle de cliente
- `POST /clientes` - Crear cliente
- `PUT /clientes/{id}` - Actualizar cliente
- `DELETE /clientes/{id}` - Eliminar cliente

### Facturas
- `GET /facturas` - Listar facturas
- `GET /facturas/{id}` - Ver detalle de factura
- `POST /facturas` - Crear factura
- `PUT /facturas/{id}` - Actualizar factura
- `DELETE /facturas/{id}` - Eliminar factura

### Incidencias
- `GET /incidencias` - Listar incidencias
- `GET /incidencias/{id}` - Ver detalle de incidencia
- `POST /incidencias` - Crear incidencia
- `PUT /incidencias/{id}` - Actualizar incidencia
- `DELETE /incidencias/{id}` - Eliminar incidencia

## 🔐 Autenticación

El sistema incluye autenticación con:

- Login seguro
- Gestión de sesiones
- Control de acceso por rutas

## 🎨 Tecnologías

- **Backend**: Laravel 12
- **Frontend**: Blade Templates, JavaScript, Tailwind CSS
- **Build Tool**: Vite
- **Base de Datos**: MySQL/PostgreSQL
- **Testing**: PHPUnit
- **Contenedorización**: Docker


## 👤 Autor

[@01Derek10](https://github.com/01Derek10)

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios mayores, abre un issue primero para discutir los cambios propuestos.

## 📧 Contacto

Para preguntas o sugerencias, por favor crea un issue en el repositorio.

---

**Última actualización**: Abril 2026

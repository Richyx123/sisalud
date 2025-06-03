# SISALUD

Sistema web de gestión de salud que permite la administración de pacientes, doctores y citas médicas.

## Características

- Sistema de autenticación para múltiples tipos de usuarios (pacientes, doctores, administradores)
- Gestión de perfiles médicos y datos personales
- Sistema de citas médicas con calendario integrado
- Panel de administración completo
- Interfaz web moderna y responsive
- Sistema de notificaciones integrado
- Base de datos SQLite para almacenamiento persistente

## Requisitos del Sistema

- Python 3.13 o superior
- Dependencias principales:
  - Flask==2.2.5
  - Flask-SQLAlchemy==2.5.1
  - Flask-Login==0.6.2
  - Flask-WTF==1.1.1
  - Werkzeug==2.2.3
  - SQLAlchemy==1.4.46
  - PyTZ==2023.3
  - python-dotenv==1.0.0
  - email-validator==2.0.0

## Instalación

1. Clona este repositorio:
```bash
git clone [url-del-repositorio]
cd SISALUD
```

2. Crea y activa un entorno virtual:

En Windows:
```bash
python -m venv venv
.\venv\Scripts\activate
```

En Linux/Mac:
```bash
python3 -m venv venv
source venv/bin/activate
```

3. Instala las dependencias:
```bash
pip install -r requirements.txt
```

## Configuración

1. Crea el archivo `.env` en la raíz del proyecto:
```env
SECRET_KEY=tu_clave_secreta_aqui
FLASK_ENV=development
DATABASE_URL=sqlite:///sisalud.db
```

2. Inicializa la base de datos:
```bash
python create_db.py
```

## Uso

1. Activa el entorno virtual si no está activado:

Windows:
```bash
.\venv\Scripts\activate
```

Linux/Mac:
```bash
source venv/bin/activate
```

2. Ejecuta el servidor:
```bash
python app.py
```

3. Accede a la aplicación:
```
http://127.0.0.1:5000
```

## Estructura del Proyecto

```
SISALUD/
├── app.py              # Aplicación principal Flask
├── create_db.py        # Script de inicialización de BD
├── requirements.txt    # Dependencias del proyecto
├── sisalud.db         # Base de datos SQLite
├── .env               # Variables de entorno
├── static/            # Archivos estáticos
│   ├── css/          # Hojas de estilo
│   ├── js/           # Scripts de JavaScript
│   └── img/          # Imágenes y recursos
├── templates/         # Plantillas HTML
│   ├── base.html     # Plantilla base
│   ├── inicio.html   # Página principal
│   ├── login.html    # Inicio de sesión
│   ├── registro.html # Registro de usuarios
│   └── ...           # Otras plantillas
└── README.md         # Documentación
```

## Funcionalidades Principales

### Gestión de Usuarios
- Registro diferenciado para pacientes y doctores
- Sistema de autenticación con ID único
- Recuperación de contraseña por email
- Perfiles personalizados por tipo de usuario
- Edición de datos personales

### Panel de Administración
- Gestión completa de usuarios
- Estadísticas del sistema en tiempo real
- Control de accesos y permisos
- Gestión de citas y consultas
- Reportes y análisis

### Sistema de Citas
- Calendario de citas interactivo
- Programación y cancelación de citas
- Historial médico digital
- Notificaciones automáticas
- Seguimiento de tratamientos

## Seguridad Implementada

- Protección CSRF en formularios
- Contraseñas hasheadas con Werkzeug
- Sistema de sesiones seguro
- Validación de datos y formularios
- Protección de rutas sensibles
- Sanitización de entradas de usuario

## Equipo de Desarrollo

- **Institución:** Tecnológico Nacional De México Campus Minititlán
- **Materia:** Fundamentos De Ingeniería De Software
- **Integrantes:** 
  - Richard De Jesus Espinoza Francisco
  - Carlos Rafael Martinez Hernandez
- **Profesor:** Kevin David Molina Gomez
- **Equipo:** Rosa

## Soporte y Contacto

Para reportar problemas o sugerir mejoras:
- Crear un issue en el repositorio
- Contactar al equipo de desarrollo

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

⌨️ Desarrollado con ❤️ por el Equipo Rosa usando Flask y Python 
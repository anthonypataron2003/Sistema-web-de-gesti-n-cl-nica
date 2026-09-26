# 🏥 App Security

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Django-5.2.1-green?style=for-the-badge&logo=django" alt="Django">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Gemini-AI-orange?style=for-the-badge&logo=google" alt="Gemini AI">
</p>

<p align="center">
  <strong>Sistema web para la gestión clínica, administración de usuarios y servicios médicos, con integración de inteligencia artificial mediante Gemini.</strong>
</p>

---

## 📌 Descripción

**App Security** es una aplicación web desarrollada con **Django** para gestionar diferentes procesos de una clínica o consultorio médico.

El sistema integra módulos para la administración de pacientes, médicos, especialidades, citas, diagnósticos, pagos y medicamentos. Además, incorpora un **asistente virtual basado en Gemini AI** para proporcionar interacción mediante inteligencia artificial.

El proyecto está diseñado utilizando una arquitectura modular que facilita el mantenimiento, escalabilidad y organización del sistema.

---

## 🖥️ Vista del sistema

> 📸 Agrega aquí capturas reales de tu aplicación.

### 🔐 Inicio de sesión

![Inicio de sesión](docs/images/login.png)

### 📊 Panel principal

![Dashboard](docs/images/dashboard.png)

### 👨‍⚕️ Gestión médica

![Gestión médica](docs/images/medicos.png)

### 🤖 Asistente virtual con IA

![Chatbot Gemini](docs/images/chatbot.png)

### 💳 Gestión de pagos

![Pagos](docs/images/pagos.png)

> **Nota:** Las imágenes anteriores son rutas de ejemplo. Guarda tus capturas dentro de `docs/images/` utilizando esos nombres o modifica las rutas según tus archivos.

---

# 🚀 Funcionalidades

### 🔐 Seguridad y usuarios

* Autenticación de usuarios.
* Gestión de perfiles.
* Control de acceso.
* Administración de usuarios del sistema.
* Protección mediante configuración de Django.

### 👨‍⚕️ Gestión clínica

* Registro y administración de médicos.
* Gestión de pacientes.
* Especialidades médicas.
* Citas médicas.
* Diagnósticos.
* Medicamentos.
* Servicios adicionales.

### 💰 Gestión económica

* Registro de pagos.
* Integración con **PayPal Sandbox**.
* Administración de gastos.
* Generación de documentación y reportes.

### 🤖 Inteligencia Artificial

* Chatbot integrado con **Google Gemini**.
* Asistente virtual para interacción con los usuarios.
* Integración mediante API.
* Procesamiento de consultas desde el sistema web.

### 📄 Reportes y documentos

* Generación de reportes.
* Generación de documentos PDF.
* Gestión de archivos multimedia.
* Carga y almacenamiento de documentación.

---

# 🛠️ Tecnologías utilizadas

| Tecnología         | Uso                          |
| ------------------ | ---------------------------- |
| 🐍 Python          | Lenguaje principal           |
| 🌐 Django          | Framework web                |
| 🐘 PostgreSQL      | Base de datos                |
| 🎨 HTML / CSS      | Interfaz web                 |
| ⚡ JavaScript       | Funcionalidad del frontend   |
| 🅱️ Bootstrap      | Diseño de interfaz           |
| 🤖 Gemini AI       | Asistente inteligente        |
| 🔄 Django Channels | Funcionalidad en tiempo real |
| 📄 ReportLab       | Generación de documentos     |
| 📑 WeasyPrint      | Generación de PDF            |

---

# 📋 Requisitos previos

Antes de ejecutar el proyecto debes tener instalado:

* Python **3.10 o superior**
* pip
* PostgreSQL
* Git
* Entorno virtual de Python

Puedes comprobar Python con:

```bash
python --version
```

Y pip con:

```bash
pip --version
```

---

# ⚙️ Instalación

## 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
```

Ingresar a la carpeta:

```bash
cd app_security
```

---

## 2. Crear el entorno virtual

### Windows

```powershell
python -m venv venv
```

Activarlo:

```powershell
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Instalar dependencias

Si el proyecto contiene `requirements.txt`:

```bash
pip install -r requirements.txt
```

Si el archivo tiene otro nombre, utiliza el nombre correspondiente:

```bash
pip install -r dependencias.txt
```

---

# 🔑 Configuración del archivo `.env`

Crea un archivo llamado:

```text
.env
```

en la raíz del proyecto.

Ejemplo:

```env
SECRET_KEY=tu_clave_secreta
DEBUG=True

DB_ENGINE=django.db.backends.postgresql
DB_NAME=medicos
DB_USER=postgres
DB_PASSWORD=tu_password
DB_HOST=localhost
DB_PORT=5432

GEMINI_API_KEY=tu_api_key

EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=tu_correo@gmail.com
EMAIL_HOST_PASSWORD=tu_password_app
EMAIL_USE_TLS=True
DEFAULT_FROM_EMAIL=tu_correo@gmail.com

PAYPAL_CLIENT_ID=tu_paypal_client_id
PAYPAL_CLIENT_SECRET=tu_paypal_client_secret
PAYPAL_MODE=sandbox
```

> ⚠️ **Nunca subas el archivo `.env` a GitHub.** Contiene información sensible como contraseñas, API Keys y credenciales de servicios externos.

Agrega `.env` al `.gitignore`:

```gitignore
.env
venv/
__pycache__/
*.pyc
```

---

# 🗄️ Configuración de PostgreSQL

Crear una base de datos llamada:

```text
medicos
```

Configuración utilizada por el proyecto:

```text
Base de datos: medicos
Usuario: postgres
Host: localhost
Puerto: 5432
```

Después ejecuta las migraciones:

```bash
python manage.py makemigrations
```

```bash
python manage.py migrate
```

---

# 👤 Crear superusuario

Para acceder al panel administrativo de Django:

```bash
python manage.py createsuperuser
```

Ingresa:

* Nombre de usuario
* Correo electrónico
* Contraseña

---

# ▶️ Ejecutar el proyecto

Inicia el servidor:

```bash
python manage.py runserver
```

Luego accede desde el navegador:

```text
http://127.0.0.1:8000/
```

Panel administrativo:

```text
http://127.0.0.1:8000/admin/
```

---

# 📁 Estructura del proyecto

```text
app_security/
│
├── applications/
│   ├── chatbot/
│   │   ├── services/
│   │   ├── views.py
│   │   └── urls.py
│   │
│   ├── core/
│   ├── doctor/
│   └── security/
│
├── media/
│
├── static/
│
├── templates/
│
├── proy_clinico/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── manage.py
├── requirements.txt
├── README.md
└── .env
```

---

# 🧩 Arquitectura modular

El sistema se encuentra organizado mediante diferentes aplicaciones de Django:

```text
                    ┌─────────────────────┐
                    │     APP SECURITY    │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       ┌───────────┐     ┌───────────┐     ┌───────────┐
       │ Security  │     │   Doctor  │     │   Core    │
       └───────────┘     └───────────┘     └───────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               │
                               ▼
                       ┌──────────────┐
                       │   Chatbot AI │
                       │   Gemini     │
                       └──────────────┘
                               │
                               ▼
                       ┌──────────────┐
                       │ PostgreSQL   │
                       └──────────────┘
```

---

# 🤖 Integración con Gemini

El sistema incorpora un chatbot utilizando la API de Gemini.

Flujo general:

```text
Usuario
   │
   ▼
Interfaz web
   │
   ▼
Django
   │
   ▼
Chatbot Service
   │
   ▼
Gemini API
   │
   ▼
Respuesta
   │
   ▼
Usuario
```

> ℹ️ Para nuevos desarrollos se recomienda utilizar la librería actual de Google para Gemini y evitar depender de paquetes que hayan quedado obsoletos.

---

# 💳 Integración con PayPal

El proyecto incorpora PayPal en modo:

```text
sandbox
```

Esto permite realizar pruebas de integración sin utilizar transacciones reales.

Las credenciales deben almacenarse mediante variables de entorno:

```env
PAYPAL_CLIENT_ID=...
PAYPAL_CLIENT_SECRET=...
PAYPAL_MODE=sandbox
```

---

# 🧪 Comandos útiles

### Crear migraciones

```bash
python manage.py makemigrations
```

### Aplicar migraciones

```bash
python manage.py migrate
```

### Crear superusuario

```bash
python manage.py createsuperuser
```

### Ejecutar pruebas

```bash
python manage.py test
```

### Ejecutar servidor

```bash
python manage.py runserver
```

---

# 🔒 Seguridad

Para un entorno de producción:

```env
DEBUG=False
```

Además:

* No almacenar contraseñas directamente en el código.
* No publicar API Keys.
* No publicar credenciales de PayPal.
* No publicar contraseñas de correo.
* Utilizar variables de entorno.
* Configurar correctamente `ALLOWED_HOSTS`.
* Utilizar HTTPS en producción.
* Mantener las dependencias actualizadas.

---

# 📸 Capturas recomendadas para GitHub

Para que el repositorio se vea más profesional, puedes agregar estas capturas:

```text
docs/
└── images/
    ├── login.png
    ├── dashboard.png
    ├── pacientes.png
    ├── medicos.png
    ├── citas.png
    ├── diagnosticos.png
    ├── pagos.png
    └── chatbot.png
```

Y mostrarlas dentro del README:

```markdown
![Dashboard](docs/images/dashboard.png)
```

---

# 📌 Estado del proyecto

🚧 **Proyecto en desarrollo**

Actualmente cuenta con módulos de gestión clínica, seguridad de usuarios, generación de documentación, pagos e integración de inteligencia artificial.

---

# 👨‍💻 Autor

**Anthony Steven Pataron Naula**

Estudiante de Ingeniería de Software
Universidad Estatal de Milagro — UNEMI

---

# 📄 Licencia

Este proyecto actualmente no especifica una licencia de software.

---

<p align="center">
  <strong>App Security</strong><br>
  Sistema web de gestión clínica y seguridad
</p>

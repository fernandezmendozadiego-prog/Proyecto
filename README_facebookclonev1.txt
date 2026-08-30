SocialClone - Red Social (Flask + MySQL)
Proyecto de red social que permite registro de usuarios, creación de publicaciones con imágenes, sistema de likes, gestión de perfil de usuario y notificaciones.

Requisitos Previos

Antes de ejecutar la aplicación, es necesario contar con el siguiente software instalado:

Python 3.8 o superior.

XAMPP (con los servicios de Apache y MySQL activos).

Servidor web simple para el frontend (extensión Live Server en VS Code o servidor HTTP ejecutable desde la consola).

Configuración de la Base de Datos

Iniciar XAMPP Control Panel y activar los módulos Apache y MySQL.

Abrir phpMyAdmin en el navegador accediendo a la dirección http://localhost/phpmyadmin.

Crear una base de datos con el nombre: instagram_clone.

Importar las tablas del proyecto (usuarios, publicaciones, likes, amistades, notificaciones).

Instalación y Configuración del Backend (Flask)

Clonar el repositorio ejecuctando la siguiente instrucción en la consola:
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio

Crear y activar un entorno virtual:
En Windows:
python -m venv venv
.\venv\Scripts\activate

En Linux o macOS:
python3 -m venv venv
source venv/bin/activate

Instalar las dependencias del proyecto:
pip install Flask flask-cors mysql-connector-python werkzeug

Iniciar el servidor backend:
python app.py

El servidor se ejecutará en http://localhost:5000.

Ejecución del Frontend

El frontend requiere ejecutarse mediante un servidor HTTP local para procesar las solicitudes fetch hacia la API del backend.

Opción A (VS Code):
Abrir la carpeta del proyecto en VS Code, hacer clic derecho sobre index.html y seleccionar Open with Live Server.

Opción B (Línea de comandos):
Ejecutar la instrucción: python -m http.server 8000
Acceder en el navegador a http://localhost:8000.

Estructura del Proyecto

static/uploads/: Directorio donde se almacenan las imágenes y avatares cargados.

app.py: Servidor API RESTful construido en Flask.

app.js: Lógica del cliente y llamadas HTTP a la API.

index.html: Interfaz de usuario de la aplicación.

README.md: Documentación técnica del proyecto.

Solución a Problemas Frecuentes

Error de conexión a MySQL: Verificar que el servicio MySQL en XAMPP esté en ejecución y que las credenciales de conexión en app.py (host, usuario y contraseña) coincidan con las de la instancia local.

Error de CORS o peticiones rechazadas: Asegurar que el backend (app.py) esté en ejecución en el puerto 5000 antes de interactuar con el cliente web.

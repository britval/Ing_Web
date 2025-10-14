# 🧩 Login Laravel – Laboratorio #2: Implementación del Login en Laravel  

**Universidad Tecnológica de Panamá – Facultad de Ingeniería Eléctrica**  
**Curso:** Ingeniería Web – II Semestre 2025  
**Estudiante:** Britney Valoy  
**Correo:** britney.valoy@utp.ac.pa  
**Instructor:** Ing. Irina Fong  

---

![PHP](https://img.shields.io/badge/PHP-8.1%2B-777bb4?logo=php)
![Laravel](https://img.shields.io/badge/Laravel-10.x-FF2D20?logo=laravel)
![MySQL](https://img.shields.io/badge/MySQL-5.7%2B-00618a?logo=mysql)
![VSCode](https://img.shields.io/badge/Editor-VSCode-007ACC?logo=visualstudiocode)
![License](https://img.shields.io/badge/License-Academic-green)

---

## 📘 1. Prerrequisitos  

Ecosistema de desarrollo utilizado para la ejecución del laboratorio:  

- **PHP versión:** 8.1 o superior  
- **Composer:** última versión estable  
- **Laravel Installer:** o instalación por `composer create-project`  
- **Servidor web local:** XAMPP / WAMP / Laragon  
- **Servidor web:** Apache o Nginx  
- **Base de datos:** MySQL o MariaDB  
- **Editor de código:** Visual Studio Code  
- **NPM:** utilizado para compilación de assets  
- **Sistema operativo:** Windows 10  
- **Navegador web:** Google Chrome  

---

## ⚙️ 2. Instalación y Configuración del Proyecto

### 📦 Crear el proyecto  
```bash
composer create-project laravel/laravel login-laravel
cd login-laravel
cp .env.example .env
php artisan key:generate
````

### ⚙️ Configuración del archivo .env

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=login_laravel
DB_USERNAME=root
DB_PASSWORD=
```

### 🧱 Ejecutar migraciones

```bash
php artisan migrate
```

### 🚀 Levantar el servidor

```bash
php artisan serve
# Servidor activo en http://127.0.0.1:8000/
```

---

## 🔐 3. Laravel para Autenticación

### Opción 1: Laravel/ui

```bash
composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev
```

### Opción 2: Laravel Breeze (UI moderna con Blade)

```bash
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate
```

---

## 🧩 4. Introducción – Arquitectura MVC

El patrón **Modelo-Vista-Controlador (MVC)** divide el sistema en tres capas principales:

* **Modelo (`app/Models`)** → manejo de datos y conexión a la base de datos.
* **Vista (`resources/views`)** → interfaz visual del usuario (login, registro, dashboard).
* **Controlador (`app/Http/Controllers`)** → gestiona la lógica del negocio.
* **Rutas (`routes/web.php`)** → define los endpoints del sistema.

```php
Route::get('/', function () {
    return view('welcome');
});
```

---

## 🧮 5. Base de Datos

El sistema utiliza una base de datos MySQL configurada en el archivo `.env`.
Las tablas se generan mediante las migraciones incluidas en Laravel:

```bash
php artisan migrate
```

**Ejemplo de tabla generada:**

* users
* password_resets
* personal_access_tokens

**Respaldo:** Se recomienda generar una copia desde phpMyAdmin en formato `.sql`.

📁 Carpeta sugerida: `/database/backups/login_laravel_backup.sql`

---

## 🖼️ 6. Resultados del Laboratorio

📸 *Insertar las evidencias correspondientes aquí:*

* [ ] Página de inicio de Laravel
* [ ] Formulario de Login
* [ ] Formulario de Registro
* [ ] Vista del Dashboard autenticado
* [ ] Visualización de la tabla `users` en phpMyAdmin


### 📍 Página de inicio de Laravel  
![Página de inicio](https://github.com/britval/Ing_Web/blob/main/imagenes/home-laravel.png)

### 🔐 Formulario de Login  
![Formulario de Login](https://github.com/britval/Ing_Web/blob/main/imagenes/login-formulario.png)

### 📝 Formulario de Registro  
![Formulario de Registro](https://github.com/britval/Ing_Web/blob/main/imagenes/registro-formulario.png)

### 🧭 Dashboard autenticado  
![Dashboard autenticado](https://github.com/britval/Ing_Web/blob/main/imagenes/dashboard-autenticado.png)

---

## ⚠️ 7. Dificultades y Soluciones

| Problema                     | Solución Aplicada                                                           |
| ---------------------------- | --------------------------------------------------------------------------- |
| Error SQLSTATE[HY000] [2002] | Activar MySQL desde XAMPP y revisar credenciales en `.env`.                 |
| NPM no reconocido            | Instalar Node.js y agregar la ruta al PATH del sistema.                     |
| Migraciones con error        | Ejecutar `php artisan migrate:fresh` para limpiar la base.                  |
| Archivos no encontrados      | Revisar permisos de lectura y escritura en `storage/` y `bootstrap/cache/`. |

---

## 📚 8. Referencias

1. [Documentación oficial de Laravel](https://laravel.com/docs)
2. [Laravel Breeze – Starter Kit](https://laravel.com/docs/starter-kits#laravel-breeze)
3. [Composer – PHP Dependency Manager](https://getcomposer.org/)
4. [XAMPP – Apache Friends](https://www.apachefriends.org/)

---

## 🧑‍💻 9. Información del Desarrollador

**Desarrollado por:**
**Britney Valoy**
**Correo:** [britney.valoy@utp.ac.pa](mailto:britney.valoy@utp.ac.pa)
**Curso:** Ingeniería Web
**Instructor:** Ing. Irina Fong
**Fecha de ejecución:** Septiembre 2025

---

## 🏁 10. Entrega del Laboratorio

📅 **Fecha de entrega:** 29 de septiembre de 2025
📂 **Entrega:** a través del repositorio GitHub enlazado a la plataforma académica.


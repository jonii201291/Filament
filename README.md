# Filament

Filament PHP es un paquete para Laravel que es capaz de crear paneles administrativos de una manera rápida y sencilla.

Instalación

- PHP 8.2+
- Laravel v11.28+
- Tailwind CSS v4.1+

1. Creación del proyecto
  composer create-project laravel/laravel proyecto-filament 
  abrir el proyecto en Visual Studio Code

2. Modidificar credenciales de BBDD en .env
  <img width="307" height="166" alt="image" src="https://github.com/user-attachments/assets/17770edf-ed2c-49b5-bd03-94f4d4154d16" />

3. Instalación de filament 
  composer require filament/filament:"~4.0" -W
**Si da errores, en el botón "Config" de Apache en XAMPP, en el archivo php.ini, quitar el ";" de extension=intl y de extension=zip

  Entrar en la carpeta del proyecto:
    cd nombreDelproyecto

  Instalar filamet
    composer require filament/filament
    
  php artisan filament:install --panels
      admin
      no

4. Ejecutar las migraciones
  php artisan migrate

5. env
   <img width="408" height="161" alt="image" src="https://github.com/user-attachments/assets/f1d8ae83-b2c7-482f-8a50-2b063f31dcdb" />

8.  Crear una nueva cuenta de usuario
  php artisan make:filament-user

  <img width="256" height="190" alt="image" src="https://github.com/user-attachments/assets/305de6ef-75d0-4db4-b29d-69ca46f7158d" />

9. 

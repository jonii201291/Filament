# Filament

Filament PHP es un paquete para Laravel que es capaz de crear paneles administrativos de una manera rápida y sencilla.

Instalación

- PHP 8.2+
- Laravel v11.28+
- Tailwind CSS v4.1+

1. Creación del proyecto
  composer create-project laravel/laravel proyecto-filament 

2. Modidificar credenciales de BBDD
  <img width="293" height="155" alt="image" src="https://github.com/user-attachments/assets/3c703fbb-0bb2-477e-b55b-45ff5cfa1609" />

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

5. Ejecutar las migraciones
  php artisan migrate

6. env
   <img width="408" height="161" alt="image" src="https://github.com/user-attachments/assets/f1d8ae83-b2c7-482f-8a50-2b063f31dcdb" />

7.  Crear una nueva cuenta de usuario
  php artisan make:filament-user

  <img width="256" height="190" alt="image" src="https://github.com/user-attachments/assets/305de6ef-75d0-4db4-b29d-69ca46f7158d" />

8. 

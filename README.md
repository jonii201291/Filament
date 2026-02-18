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

8.  Crear una nueva cuenta de usuario con los datos
  php artisan make:filament-user
  
  <img width="256" height="190" alt="image" src="https://github.com/user-attachments/assets/305de6ef-75d0-4db4-b29d-69ca46f7158d" />

9. Arrancar el servidor:
    php artisan serve

10. En URL: localhost:8000/admin/login
    introducir los credenciales del punto 8
    
   <img width="991" height="555" alt="image" src="https://github.com/user-attachments/assets/dde7e867-100c-4c9e-9c1b-b2748e133435" />

11. Crear los recursos en Filament
  En la consola
  php artisan make:model Category -m
  php artisan make:model Post -m

13. En database/migrations/tablaCategories se añade al método up()
    public function up(): void
    {
        Schema::create('categories', function (Blueprint $table) {
            $table->id();
            $table->string('name');                  
            $table->string('description');          
            $table->timestamps();
        });
    }

    Lo mismo con la tabla Post

      public function up(): void
    {
        Schema::create('posts', function (Blueprint $table) {
            $table->id();
            $table->unsignedBigInteger('user_id');                                      // campo añadido
            $table->foreign('user_id')->references('id')->on('users');                  // campo añadido
            $table->unsignedBigInteger('category_id');                                  // campo añadido
            $table->foreign('category_id')->references('id')->on('categories');         // campo añadido
            $table->string('title');                                                    // campo añadido
            $table->text('body');                                                       // campo añadido
            $table->string('image');                                                    // campo añadido
            $table->timestamps();
        });
    }

      - php artisan migrate

15.  Establecer relaciones

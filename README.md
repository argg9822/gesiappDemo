# GesiappDemo

## Descripción

**GesiappDemo** es una versión pública del proyecto original **Gesiapp**

## Requerimientos
   barryvdh/laravel-debugbar
   barryvdh/laravel-dompdf
   barryvdh/laravel-snappy
   fpdf/fpdf
   laravel/breeze
   laravel/reverb
   laravel/sail
   laravel/tinker
   laravel/ui
   maatwebsite/excel
   nesbot/carbon
   nunomaduro/collision
   nunomaduro/termwind
   spatie/laravel-ignition
   vinkla/hashids .

## Instalación de dependencias
1. Instalación con Composer
   Ejecutar dentro de la carpeta del proyecto
   ```bash
   composer install

2. instalación de spatie/browsershot
   ```bash
   composer require spatie/browsershot

3. Node JS
   ```bash
   apt install nodejs

## Configuración del entorno
1. Copiar el archivo `env.example` a `.env`
   ```bash
    cp .env.example .env

3. Generar clave de aplicación
   ```bash
   php artisan key:generate

4. Configurar el archivo .env con los detalles de la base de datos
5. Generar enlace simbólico
   ```bash
   php artisan storage:link

## Configuración de la base de datos
1. Crear la base de datos en el gestor de bases de datos (MySQL, PostgreSQL).
2. Ejecutar las migraciones
   ```bash
   php artisan migrate
3. Cargar datos iniciales de la base de datos
   ```bash
   php artisan db:seed

##Ejecución del servidor
1. Iniciar el servidor
    ```bash
    php artisan serve
    
2. Acceder a la aplicación con la ruta especificada en la terminal, por ejemplo `http://localhost:8000`

## Solución de errores comunes
Error: require(C:/xampp/htdocs/gesilaravel-main/vendor/composer/../symfony/clock/Resources/now.php): Failed to open stream
Puede ocurrir debido a problemas en la instalación de Composer. Para solucionarlo:
1. Eliminar la carpeta "vendor" y el archivo "composer.lock":
   ```bash
   rm -rf vendor composer.lock

2. Reinstalación de dependencias
   ```bash
   composer install

3. Limpiar caché de ser necesario:
   ```bash
   composer clear-cache

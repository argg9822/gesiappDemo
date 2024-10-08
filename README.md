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

2. Node JS (instalar de manera global en servidores Linux)

   Instalar el repositorio de NodeSource para la versión de Node.js
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
   sudo apt-get install -y nodejs

4. Puppeteer v23.3.0
   ```bash
   npm install puppeteer@23.3.0

5. Instalar Puppeteer y otras dependencias globalmente 
   ```bash
   sudo npm install -g puppeteer
   
3. Instalación de spatie/browsershot
   ```bash
   composer require spatie/browsershot
   
4. Instalar Chromium
   ```bash
   sudo apt-get install chromium
   
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

##Ejecución de tareas programadas
1. Verificar si existen tareas programadas
   ```bash
   php artisan schedule:list

2. Ver el estado de las tareas en el sistema (cron jobs)
   ```bash
   crontab -l

3. Si la respues es "no crontab for trakio" significa que no se ha configurado ningún cron job, entonces se ejecuta el siguiente comando para abrir el archivo crontab
   ```bash
   crontab -e

4. Agregar la siguiente línea al archivo crontab para que Laravel ejecute el scheduler cada minuto
   ```bash
   * * * * * cd /home/trakio/htdocs/www.trakio.pro/gesilaravel && php artisan schedule:run >> /dev/null 2>&
   
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

##Ejecución del servidor
1. Iniciar el servidor
    ```bash
    php artisan serve
    
2. Acceder a la aplicación con la ruta especificada en la terminal, por ejemplo `http://localhost:8000`


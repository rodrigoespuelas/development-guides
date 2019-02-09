# LARAVEL

composer install  
.env  
composer dump-autoload  
php artisan migrate:fresh  


## Recursos

https://plataforma.keepcoding.io/  
https://ajgallego.gitbooks.io/laravel-5/  
https://laraveles.com/documentacion/  

## Instalación
`composer global require "laravel/installer"`  
`laravel new blog`

https://github.com/laravel/laravel

### Local Development Server
`php artisan serve`

### Generar una llave para hashing
`php artisan key:generate`

### Generar código boilerplate para autenticación de usuarios
`php artisan make:auth`

### Crear un middleware para verificiar si el usuario tiene una sesión
`php artisan make:middleware HasUserASession`

### Crear modelo Post
`php artisan make:model Post`

### Crear la tabla "posts"
`php artisan make:migration create_posts_table --create posts`  
`php artisan migrate`

### Crear el controlador PostsController
php artisan make:controller PostController --plain

### Crear el controlador PostsController compatible con REST (resource) 
`php artisan make:controller PostsController --resource`

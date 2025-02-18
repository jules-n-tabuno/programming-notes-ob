#php 
#laravel 

## Laravel commands 

```
php artisan serve 
```
#### is a command provided by Laravel's Artisan CLI (Command Line Interface) that starts a local development server for your Laravel application.
- **Purpose**:
    - It provides a quick and easy way to view your Laravel application during development.
    - It uses PHP's built-in development server, so there's no need to set up a full web server.
- **Limitations**:
    
    - It’s **not suitable for production**. The built-in PHP server is not optimized for high-performance or secure environments.
    - Use a proper web server (like Apache, Nginx, or a cloud hosting platform) for deploying your Laravel app to production.
- **Stopping the Server**:
    - Press `Ctrl + C` in the terminal to stop the server.
----
```
php artisan list 
```

- **Purpose:** 
	- It provides the list of commands in artisan 

------
```
php artisan make:controller
```
- **Purpose** 

------
```
php artisan make:model 
```
- **Purpose** 
	- this makes files 

```
php artisan db:seed
```

```
php artisan migrate --seed 
```

```
php artisan migrate: refresh --seed
```

```
php artisan make:controller NoteController --resource --model=Note 
```

```
php artisan make:view note.index  
```

#### 38:08 

# Laravel 9 admin backend

<p align="center">
 <a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="350"></a> <a href="javaxcript:void(0)">
     <a href="https://spatie.be/" target="_blank"><img src="https://cdn.learnku.com/uploads/avatars/25700_1530502088.png" width="100"></a> <a href="javaxcript:void(0)">
 <a class="navbar-brand pt-0" href="https://www.creative-tim.com/live/argon-dashboard-laravel">
<img src="https://argon-dashboard-laravel.creative-tim.com/argon/img/brand/blue.png" width="350" class="navbar-brand-img" alt="...">
</a>
 </p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About this base

This is Admin Backend base, You can use it if you want to start a new laravel project.<br>
You don't need to start from scratch as you will get the following functionality/feature inbuilt.
Such as:

- **User roles and permission**
- **Admin dashboard with Login, Registration**
- **UI Template based on  [Argon](https://www.creative-tim.com/live/argon-dashboard-laravel)**

## Requirements

- PHP version 8 and above
- MySql
- Composer

## Installation

Install my-project with npm

- take `pull` and `cd`to your project
- Run following command one by one

```sh
composer require laravel/ui
```

```sh
composer require laravel-frontend-presets/argon
```

```sh
php artisan ui argon
```

```sh
composer update or composer dump-autoload
```

- create `.env` file and configure database credentials, `APP_URL` etc
- Make Changes (mentoined below) in file `\database\seeders\DatabaseSeeder.php`

```php
    $this->call([
        PermissionTableSeeder::class,
        CreateAdminUserSeeder::class,
        // UsersTableSeeder::class,
    ]);
```

- Check in the file `routes/web.php`, If you find any duplicate/repeated routes. please remove it manually/accordingly.
- Run `artisan storage:link` **Only if** you are using Vagrant with Homestead for development remember to ssh in your virtual machine and run the command from there. **Else** you can skip this.

- Now run following command aganin

```sh
php artisan key:generate
```

```sh
php artisan migrate --seed
```

```sh
php artisan serve
```

```sh
php artisan serve
```

- Its done! and we good to go. Happy `<codding>`😊

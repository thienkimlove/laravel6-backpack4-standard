##  Backpack Standard
### Install

- Backpack : 

`composer require backpack/crud:"4.0.*"`

- Create database 

`CREATE DATABASE db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci; `

and run `php artisan backpack:install`

- Elfinder allow admin to browser and manager files in `public/uploads`

so it not recommend to enable this.

```textmate
Install & set up the File Manager (elFinder)? 

The admin will be able to browse the 'uploads' folder 

and create/read/modify files and folders there. (yes/no) [yes]:
```

- From document of Backpack

```textmate
3) [Optional] You should now:

Change configuration values in config/backpack/base.php to make the admin panel your own. 

Backpack is white label, so you can change everything: menu color, project name, developer name etc.
If your User model has been moved (it is not App\User.php, please go change App\Models\BackpackUser.php and make sure it extends the correct user model;
If you have separate admin panels for Users and Administrators,
and already have a way to differentiate between the two, 
please change app/Http/Middleware/CheckIfAdmin.php, 
particularly checkIfUserIsAdmin($user), 
to make sure all users who get log into the admin panel have a right to do that;
If your application has only one login screen (for the admins), 
that means you're not going to use the auth controllers that Laravel provided by default. 
You're only going to use Backpack's auth controllers. 
You can keep the Laravel ones in your project, of course. 
But some people like to delete them to not get confused later on:
# OPTIONAL! Please read the notice above.
rm -rf app/Http/Controllers/Auth #deletes laravel's demo auth controllers
```

- I remove Laravel Default Auth. 

`rm -rf app/Http/Controllers/Auth`

### Install Addon for backpack

`https://backpackforlaravel.com/docs/4.0/install-optionals`

First install Permission Manager `composer require backpack/permissionmanager`

Follow every step in `https://github.com/Laravel-Backpack/PermissionManager#install`

### Create user

`php artisan backpack:user`

Run `php artisan serve`

### For start new project

Create Database

`CREATE DATABASE db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci; `

Upload project and run `composer install`

Import template from `sqltemplate/template.sql`




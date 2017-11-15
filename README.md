# Laravel Admin Starter with AdminLTE

A starter Admin dashboard built with Laravel+AdminLTE (Laravel 5.5)

### Tutorial
You can read more details about this project [here](http://juancadima.com/integrating-adminlte-laravel/)


### How to install
1) Simply [download](https://github.com/jcadima/laravel-admin/archive/master.zip) or clone the repo:

```
git clone git@github.com:jcadima/laravel-admin.git
```

**NOTE**: If using MariaDB you might see an error about "key too long", to fix this open:

```
 /app/Providers/AppServiceProvider.php
```

make the following changes so that it looks like:

```php
namespace App\Providers;

use Illuminate\Support\ServiceProvider;
// Include Schema
use Illuminate\Support\Facades\Schema;

class AppServiceProvider extends ServiceProvider
{

    public function boot()
    {  
        Schema::defaultStringLength(191) ;
    }

    public function register()
    {
        //
    }
}

```

2a) Run the database seeder:

```
php artisan db:seed
```

The project comes with a UsersTableSedder.php class with the following:

```php
        App\User::create([
            'name' => 'Demo User',
            'email' => 'demo@test.com',
            'password' => bcrypt('demo2017') 
        ]);
```

OR

2b) Import database
[Laravel Admin DB](https://github.com/jcadima/laravel-admin/blob/master/laraveladmin.sql)

Which will create the same demo user from step 2a<br>
user: demo@test.com <br/>
pass: demo2017

### Requirements
* PHP >= 7.0.0
* OpenSSL PHP Extension
* PDO PHP Extension
* Mbstring PHP Extension
* Tokenizer PHP Extension
* XML PHP Extension

**(If you are using Homestead you already met those requirements)**


### Todos && Features
* [X] Built with Laravel 5.5
* [X] Default Users table seeder
* [X] AdminLTE integrated
* [X] Main dashboard page
* [X] Users list in admin dashboard


### Screenshots

![alt LoginDemo](http://juancadima.com/wp-content/uploads/laraveladmin.png)

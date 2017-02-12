# Laravel installation
    Create a new folder
    `laravel new`

    `npm install` to install packages listed in packages.json file // Run this in gitShell
    Include the following as your bootstrap stylesheet and js 
    `<link rel="stylesheet" type="text/css" href="{{ elixir('css/app.css') }}">`
    `<script type="text/javascript" src="{{ elixir('js/app.js') }}"></script>`


##php artisan tinker
    `DB::listen( function($query) { var_dump($query->sql); } );`
    `$card = App\Card::first();`
    `$card->notes;`
    `$card->fresh()`        // Refresh sql query browser

##php artisan serve
    Start a local server


##php artisan
    To get list of all commands

##Routes
    These are defined in 
        routes/web.php

    Passing values to the view
        $people = ['AW', "VW", "PSW"];
        Method 1] return view('welcome', ['people' => $people]);  // ['key' => 'value']
                                                        // in the view `key` will be varible
        Method 2] return view('welcome', compact('people'));
        Method 3] return view('welcome')->with('people', $people);
        Method 4] return view('welcome')->withPeople($people);

        return view('pages.about', ['str' => "just a string"]);
            // `pages` folder `about.blade.php` file

##Creating controller class
    php artisan make:controller PagesController


##Layout files
    @yield('content')  // In layout.blade.php
    
        /* In your views files */
    @extends('layout')
    @section('content')
        // ...
    @stop

##Assets files
    All assets files in `public` directory
    Reference by saying `/folderName`

    or Using elixir
        <link rel="stylesheet" type="text/css" href="{{ elixir('css/app.css') }}">

    `npm install`
    `gulp --production`


##Database
    `config/database.php`
        Edit this file line 29 make it mysql
        On line 55 change the database parameters
        Delete all entries of DB_ in the default .env file

    `php artisan make:migration short_description --create=TableName`
        Edit the migration file to make the fields and data types
        https://laravel.com/docs/5.0/schema

    Step 1] `php artisan migrate`
    Step 2] `php artisan make:model ModelName`

                            If at any point you get error such as `failed to open stream` 
                            execute following 
                                `composer dump-autoload` 
                            addtionally if needed `
                                php artisan migrate:rollback`

    SINGLE STEP] 
        `php artisan make:model ModelName -m`
            This will make the migration as well as the model



#ERROR HANDLING
MassAssignmentException in Model.php 
    `$fillable = ['id', 'name', 'etc'];`


#Faker
https://tutorials.kode-blog.com/laravel-5-faker-tutorial
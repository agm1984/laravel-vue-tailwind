# Laravel-Vue-Tailwind

> Helps you get started by allowing you to analyze the project and config settings.

## Installation

``` bash
$ git clone https://github.com/agm1984/laravel-vue-tailwind.git

$ cd laravel-vue-tailwind

$ valet link

$ valet secure
```

### From Zero

``` bash
# make a laravel app
$ laravel new example-app

# install vue
$ composer require laravel/ui

$ php artisan ui vue

# add auth
$ php artisan ui vue --auth

$ npm install

$ npm run watch
```

### With Tailwind

``` bash
$ npm install --save-dev tailwindcss

$ npx tailwindcss init
```

#### Add files to purge

In **tailwind.config.js**:

```
    purge: [
        'resources/views/**/*.blade.php',
        'resources/js/**/*.js',
        './resources/**/*.vue',
    ],
```

Update **webpack.mix.js**:

``` javascript
mix.js('resources/js/app.js', 'public/js')
    .vue()
    .sass('resources/sass/app.scss', 'public/css', {}, [
        tailwindcss('tailwind.config.js'),
    ])
    .options({
        processCssUrls: false,
    });
```

Add in **app.scss**:

``` css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Database

``` bash
$ mysql -u root -p
```

``` sql
CREATE DATABASE tailwindauth;

CREATE USER 'tailwindauth'@'localhost' IDENTIFIED BY 'tailwindauth';

GRANT ALL PRIVILEGES ON tailwindauth.* TO 'tailwindauth'@'localhost';
```

Don't forget to add the users table:

``` bash
$ php artisan migrate
```

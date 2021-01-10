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

In **tailwind.config.js**,

```
    purge: [
        'resources/views/**/*.blade.php',
        'resources/js/**/*.js',
    ],
```

#### Tailwind in production

By default, Tailwind looks for the config file in the root of the project directory,
so it's not required anymore to explicitly declare it in webpack.mix.js.

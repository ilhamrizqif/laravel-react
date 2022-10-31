# Laravel React

Laravel-React, built using Laravel with Sail. With Sail, you don't need PHP Installed on your machine, you don't need PostgreSQL Installed on your machine, just install Docker then finish. As simple as that.

# Step For Running the Project
 
## Install the Project

Firstly first, you need to install composer / plugins on laravel using Composer. But, if you are not install the composer, you can install using Docker with this command:

```shell
docker run --rm \
  -u "$(id -u):$(id -g)" \
  $(PWD):/var/www/html  \
  -w /var/www/html \
  laravelsail/php81-composer \
  composer install --ignore-platform-reqs
```

## Running This Project

How to Run this project using Sail ?

1.  Go to this Project, then type :

```shell
./vendor/bin/sail up
```

2. However, instead of repeatedly typing vendor/bin/sail to execute Sail commands, you may wish to configure a shell alias that allows you to execute Sail's commands more easily:

```shell
alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'
```

3. then you can type like this:

```shell
sail up
```

## Install Dependencies

We can install any dependencies using composer manager.

1. Inside your Project forlder, You can install using Laravel Sail like this:

```shell
./vendor/bin/sail composer require laravel/sanctum
```

2. Or, if you have created a shortcut Alias, you can do like this:

```shell
sail composer require laravel/sanctum
```

## Running migration

You can running migration with Laravel Sail like you don't use it.
( Assume we have created a shortcut alias ):

1. You can create a migration file like this ( Assume we have created a shortcut alias ):

```shell
sail artisan make:migration create_users_table
```

2. Then, you can execute your migration like this:

```shell
sail artisan migrate
```

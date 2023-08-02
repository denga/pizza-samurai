## Create a new project

see https://symfony.com/doc/current/setup.html

```
composer create-project symfony/skeleton:"6.3.*" pizza-samurai
```
Install all fancy packages for a web application (without docker)
```
composer require webapp
```
Many things installed... twig, test, serializer, profiler, orm and debug :D

## Configure your Database

We want to start fast.. so open the .dev file, comment out the current variable DATABASE_URL with postgres configuration and use sqlite
```
DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"
```

## Run the project

```
cd pizza-samurai/
symfony serve
```
or (without symfony cli)
```
cd pizza-samurai/
php -S localhost:8000 -t public/
```
Now we have an empty page but with an amazing web profiler on the bottom thanks to the profiler-pack recipe 
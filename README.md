## Создание пустого проекта на Laravel 11 в OSPanel
запускаем OSPanel и открываем консоль
```shell
cd domains
```
Создаем папку для проекта 
```shell
mkdir laravel-11.loc
 ```
Переходим в папку с проектом 
```shell
cd 2group.ru
```
Создаем новый проект на Laravel в текушй деректории 
```shell
Composer create-project laravel/laravel .
```
Установливаем поддержку API и модуль Sanctum
```Shell
php artisan install:api
```
Публикуем конфигурационный файл Cors
```Shell
php artisan config:publish cors
```
Создание символической сыллки из деректории 
public/storage к деректории storage/app/public
```Shell
php artisan storag:link
```
В корне проекта создан файл .htaccess
```php
RewriteEngine on
RewriteRule ^(.*)$ public/$1
```

 ## Установка проекта из репозитория 
Склонируем репозитория в папку domains
```Shell
cd domains
git clone https://github.com/382Spitchfabrik/2group.ru.git
```
Перейдем в папку с проектом и устоновим composer-зависимости 
```Shell
sd 2group.ru
composer install
```
Скопируем файл .env.example в файл .env 
```shell
copy .env.exaple .env
```
Генерируем ключ шифрования
```shell
php artisan key:generate
```
Меняем файл конфигурации .env (пример для БД MySQL)
```php
DB_CONNECTION=MySQL
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Имя_БД
DB_USERNAME=Логин_пользователя_БД
DB_PASSWORD=Пароль_пользователя_БД

SESSION_DRIVER=file
```

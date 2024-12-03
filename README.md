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
 

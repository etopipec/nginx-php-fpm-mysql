## laravel, nginx, php-fpm, mysql, composer, artisan

Artisan
```
docker-compose run artisan <command>
```

Composer
```
docker-compose run composer <command>
```

Инструкция:
1. Клонируем репу в любую папку
```
git clone https://github.com/vadimkaKharitonenko/nginx-php-fpm-mysql.git .
```
2. Удаляем .git, .gitignore, /src/.gitkeep
3. Поднимаем контейнеры
```
docker-compose up -d nginx
```
4. Проверяем браузер http://localhost:8000, там должен быть ответ nginx.
5. Ставим laravel
```
docker-compose run composer create-project laravel/laravel .
```
6. Ставим laravel/breeze, выбираем API only
```
docker-compose run composer require laravel/breeze --dev
```
7. Ставим laravel/sanctum
```
docker-compose run composer require laravel/sanctum
```
8. Проверяем http://localhost:8000, должен быть jsonview.
9. Правим src/.env
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel
DB_PASSWORD=password
```
10.  Делаем миграцию
```
docker-compose run artisan migrate
```

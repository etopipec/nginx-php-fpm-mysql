## laravel, nginx, php-fpm, mysql, composer, artisan

Create Laravel project in ./src directory
```
docker-compose run composer create-project laravel/laravel .
```

Run containers
```
docker-compose up -d
```

Down containers
```
docker-compose down
```

Artisan
```
docker-compose run artisan migrate
```

Issuing rights to the project root
```
sudo chmod -R 777 root-folder/
```
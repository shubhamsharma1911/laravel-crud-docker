# laravel-crud-docker

## Prerequisite
Make sure you have [docker](https://docs.docker.com/install/) and [docker-compose](https://docs.docker.com/compose/install/) installed on you machine.

1. `git clone`
2. `create a .env file copy content from .env.docker and do not make any change`

run following command in terminal / power shell
```
docker-compose up -d
```

when docker will finish building the containers, access the "laravel-react-app" container using following command

`docker exec -it lr_app sh`

now you will be inside container

run following commands
1. `composer install && composer update`
2. `php artisan cron:refresh-database`
3. `php artisan key:gen`
4. if npm version < 7 `npm install && npm run dev` else `npm install --legacy-peer-deps && npm run dev`

open browser and check the following address

`http://localhost:8100`


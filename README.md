# laravel-crud-docker

Make sure you have docker and docker-compose installed on you machine.

git clone
create a .env file copy content from .env.docker and do not make any change
run following command in terminal / power shell

docker-compose up -d
when docker will finish building the containers, access the "laravel-react-app" container using following command

docker exec -it lr_app sh

now you will be inside container

run following commands

composer install && composer update
php artisan cron:refresh-database
php artisan key:gen
if npm version < 7 npm install && npm run dev else npm install --legacy-peer-deps && npm run dev
open browser and check the following address

http://localhost:8100

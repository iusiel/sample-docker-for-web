# README NOT YET UPDATED. INFORMATION BELOW MAYBE INACCURATE

# Sample Docker for Web

1. Contains 2 main folders. app and docker
2. app folder contains the php project code
3. docker folder contains the Dockerfiles used for creating the containers.

## How to use
1. Put project files inside app folder
2. Run "docker-compose up --build" on project root
3. Access project.local on browser. (Make sure that project.local is declared on hosts file)

## Run commands inside container
(Make sure to run all commands in project root)
1. docker-compose exec php \<command to run>
- docker-compose exec php php --version
- docker-compose exec composer install (Composer is installed inside the PHP image)
2. docker-compose exec mysql \<command to run>
- docker-compose exec mysql mysql -u root -p
3. docker-compose exec node \<command to run>
- docker-compose exec node npm install

## Services used
1. PHP-FPM 7.4.1 (composer included here)
2. Nginx 1.17.6
3. MySQL 5.7.28
4. Node 12.14.0

## Additional
1. There is a laravel.local.conf at docker/nginx. If you want to use laravel, make sure to change the volume declared in docker-compose.yml
- ./docker/nginx/laravel.local.conf:/etc/nginx/conf.d/laravel.local.conf

### This is intended to be used as a development environment. Do not use in production.
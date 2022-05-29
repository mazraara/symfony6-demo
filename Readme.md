

open /etc/host file on you host machine and
add new line:
 - `0.0.0.0 symfony-local.test`

Open terminal:
 - Run: 'cd <cloned project dir>'
 - Run: `docker-compose build`
 - Run: `docker-compose up -d`
 - Run: `docker-compose exec php /bin/bash`
 - Run: `composer install`
 - Run: `symfony console doctrine:database:create`
 - Run: `symfony console doctrine:migrations:migrate`
 - Run: `symfony console doctrine:schema:update --force`
 
Run unit tests:
- Run: `docker-compose exec php /bin/bash`
- Run: `php bin/phpunit tests`

![example workflow](https://github.com/Anton-Emelyanov/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)


# api_yamdb
Cервис для публикации отзывов, рейтингов и комментариев к различным произведениям.

## Технологии
- Python 3.7
- Django 3.2
- Django REST Framework 3.12
- PostgreSQL 13
- Docker

## Установка
Для запуска проекта необходимо выполнить следующие шаги:

1. Склонировать репозиторий:

``` git clone https://github.com/Anton-Emelyanov/infra_sp2.git ```

2. Перейдите в директорию проекта:

``` cd infra_sp2 ```

4. Запустите проект с помощью Docker Compose:

``` docker-compose up -d --build ```

5. Собирите статику:

``` sudo docker-compose exec web python manage.py collectstatic --no-input ```

6. Примените миграции:

``` sudo docker-compose exec web python manage.py makemigrations ``` \
``` sudo docker-compose exec web python manage.py migrate --noinput ```

7. Создайте суперпользователя:

``` sudo docker-compose exec web python manage.py createsuperuser ```

8. Заполните базу:

``` sudo docker-compose exec web python manage.py loaddata fixtures.json ```

- Для работы с API можно использовать различные инструменты, такие как curl или Postman. Подробнее о том, как использовать API, можно узнать из документации, которая доступна по адресу: 
    
``` http://84.201.130.23/redoc/ ```

## GitHub Secrets
DOCKER_USERNAME - имя пользователя в DockerHub DOCKER_PASSWORD - пароль пользователя в DockerHub HOST - ip-адрес сервера USER - пользователь SSH_KEY - приватный ssh-ключ (публичный должен быть на сервере) PASSPHRASE - кодовая фраза для ssh-ключа TELEGRAM_TO - id чата в телеграме TELEGRAM_TOKEN - токен телеграм бота

### Автор
Антон Емельянов


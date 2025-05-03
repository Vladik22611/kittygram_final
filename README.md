# Kittygram — социальная сеть для обмена фотографиями любимых питомцев.

### Описание проекта
Пользователи могут регистрироваться, загружать фотографии с описанием и смотреть питомцев других пользователей.

## Технологии

- Фронтенд: React
- Бэкенд: Django Rest Framework
- База данных: PostgreSQL
- Nginx
- Docker
- Gunicorn «Green Unicorn»
- Github actions

### Установка
<i>Примечание: Все примеры указаны для Linux</i><br>
1. Склонируйте репозиторий на свой компьютер:
    ```
    git clone https://github.com/Vladik22611/kittygram_final
    ```
2. Создайте файл `.env` и заполните его своими данными. Все необходимые переменные перечислены в файле `.env.example`, находящемся в корневой директории проекта.



## Запуск проекта
# Для адаптации его к вашему серверу добавьте секреты в GitHub Actions:

    ```
    DOCKER_USERNAME                # имя пользователя в DockerHub
    DOCKER_PASSWORD                # пароль пользователя в DockerHub

    TELEGRAM_TO                    # ID вашего телеграм-аккаунта (можно узнать у @userinfobot, команда /start)
    TELEGRAM_TOKEN                 # токен вашего бота (получить токен можно у @BotFather, команда /token, имя бота)

Выполняем запуск:

```bash
sudo docker compose -f docker-compose.yml up
```

## После запуска: Миграции, сбор статистики



```bash
sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py migrate

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend python manage.py collectstatic

sudo docker compose -f [имя-файла-docker-compose.yml] exec backend cp -r /app/collected_static/. /backend_static/static/
```

И далее проект доступен на:

```
http://localhost:9000/
```

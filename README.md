# Kittygram — социальная сеть для обмена фотографиями любимых питомцев.

### Описание проекта
Пользователи могут регистрироваться, загружать фотографии с описанием и смотреть питомцев других пользователей.

### Установка
<i>Примечание: Все примеры указаны для Linux</i><br>
1. Склонируйте репозиторий на свой компьютер:
    ```
    git clone https://github.com/Vladik22611/kittygram_final
    ```
2. Создайте файл `.env` и заполните его своими данными. Все необходимые переменные перечислены в файле `.env.example`, находящемся в корневой директории проекта.

## Технологии

- Фронтенд: React
- Бэкенд: Django Rest Framework
- База данных: PostgreSQL
- Nginx
- Docker
- Gunicorn «Green Unicorn»
- Github actions


## Запуск проекта

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

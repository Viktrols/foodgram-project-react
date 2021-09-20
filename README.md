# REST API для сервиса Foodgram - сайта с рецептами
<тут подробное описание проекта>
## Подготовка и запуск проекта
### Склонировать репозиторий на локальную машину:
```
git clone https://github.com/Viktrols/foodgram-project-react
```
### Создать .env и заполнить переменные окружения:
```
SECRET_KEY=<секретный ключ проекта django>

DB_ENGINE=django.db.backends.postgresql
DB_NAME=<имя базы данных postgres>
DB_USER=<имя пользователя>
DB_PASSWORD=<пароль>
DB_HOST=db
DB_PORT=5432

```
### Собрать docker-compose:
```
docker-compose up -d --build
```
### Собрать статические файлы:
```
docker-compose exec backend python manage.py collectstatic --noinput
```
### Применить миграции:
```
docker-compose exec backend python manage.py migrate --noinput
```
### Создать суперпользователя Django:
```
docker-compose exec backend python manage.py createsuperuser
```
### Проект будет доступен по адресу http://localhost/recipes
### Документация API http://localhost/api/docs/

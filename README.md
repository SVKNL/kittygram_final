![workflow status](https://github.com/SVKNL/kittygram_final/actions/workflows/main.yml/badge.svg)
### Описание проекта:

Сайт про котиков с возможностью добавлять фото и профиль своих котов.

Стэк:

```
Python
Django
DRF
Docker
Nginx
```

Запуск проекта:

```
Скачать репозиторий при помощи команды: git clone <ccылка с github>
Запускаем контейнеры командой: sudo docker compose -f docker-compose.production.yml up
```
Заполнение файла .env в папке проекта:

```
Заполнить данные в формате:
POSTGRES_USER=user
POSTGRES_PASSWORD=password
POSTGRES_DB=django

DB_HOST=db
DB_PORT=5432
SECRET_KEY=djangosecretkey
ALLOWED_HOSTS=your ip adress including 'localhost'
```

Выполнить миграции и сбор статики:

```
sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate

sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic

sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /static/static/
```

Проект доступен по адресу:

```
localhost:9000
```

Автор:
Карпов Степан
[Github](https://github.com/SVKNL)
# YaTube
Социальная сеть для публикации личных дневников.

**Создать requirements.txt**
```
poetry export --without-hashes --format=requirements.txt > backend/requirements.txt
```

**Собрать контейнер**
```
docker-compose up -d --build
```

**Установить миграции**
```
docker-compose exec backend python manage.py migrate
```

**Создать суперюзера**
```
docker-compose exec backend python manage.py createsuperuser
```

**Собрать статику**
```
docker-compose exec backend python manage.py collectstatic --no-input
```

**Остановить контейнер**
```
docker-compose down
```
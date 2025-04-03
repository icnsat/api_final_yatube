# api_final
Проект, имитирующий социальную сеть, с возможностью создания постов, добавления их в группы, написания к ним комментариев и подписки на пользователей.


# Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/icnsat/api_yatube.git
```

```
cd api_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

# Примеры запросов к API:

- Создание поста:
```
POST /api/v1/posts/
{
    "text": "string"
}
```

- Получение части постов:
```
GET /api/v1/posts/?limit=10&offset=40
```

- Добавление комментария:
```
POST /api/v1/posts/{post_id}/comments/
{
    "text": "string"
}
```

- Получение комментариев поста:
```
GET /api/v1/posts/{post_id}/comments/
```

- Получение информации о сообществе:
```
GET /api/v1/groups/{id}/
```

- Подписка:
```
POST /api/v1/follow/
{
    "following": "string"
}
```

- Удаления комментария:
```
DELETE /api/v1/posts/{post_id}/comments/{id}/
```

_Все возможные запросы к API представлены в документации по адресу `/redoc`_

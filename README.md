# API для Yatube

## Описание
Проект представляет собой API для социальной сети Yatube. 
Позволяет создавать посты, комментарии, подписываться на авторов.

## Установка
1. Клонируйте репозиторий
2. Создайте виртуальное окружение: python -m venv venv
3. Активируйте окружение: source venv/bin/activate (для Windows: venv\Scripts\activate)
4. Установите зависимости: pip install -r requirements.txt
5. Выполните миграции: python manage.py migrate
6. Запустите сервер: python manage.py runserver

## Примеры запросов

### Получение списка постов
GET /api/v1/posts/

Ответ:
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": null,
  "results": []
}

### Создание поста
POST /api/v1/posts/
{
  "text": "Текст поста",
  "group": 1
}

### Получение списка комментариев
GET /api/v1/posts/{post_id}/comments/

### Подписки
GET /api/v1/follow/
POST /api/v1/follow/
{
  "following": "username"
}

## Технологии
- Python 3.9+
- Django
- Django REST Framework
- JWT-аутентификация
- SQLite

## Автор
[Ваше имя]

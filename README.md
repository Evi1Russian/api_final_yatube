# Документация проекта yatube_api
 
 Этот api испульзуется для взаимодействия с базой данных проекта yatube.
 ##Здесь можно: 
 Получать список постов пользователей,
 Создавать и редактировать посты,
 Удалять посты,
 Комментировать посты,
 Подписываться на авторов,
 
 ##**Установка проекта:**
 Клонируйте репозиторий,
 Установите виртуальное окружение командой **python3 -m venv venv**
 Активируйте виртуальное окружение командой **source venv/Scripts/activate**
 Подключите зависимости **pip install -r requirements.txt**
 Выполните миграции **python manage.py migrate**
 Запустите проект **python manage.py runserver**
 
 ##**Примеры запросов**
 GET запрос  http://127.0.0.1:8000/api/v1/posts/{id}/
  Выведет информацию о посте с выбранным id
{
 "id": 0,
 "author": "string",
 "text": "string",
 "pub_date": "2019-08-24T14:15:22Z",
 "image": "string",
 "group": 0
}
 POST запрос http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
 Добавит комментарий к выбранному посту
{
"text": "string"
}

GET запрос http://127.0.0.1:8000/api/v1/follow/
Выведет информацию о твоих подписках
[
{
"user": "string",
"following": "string"
}
]


 

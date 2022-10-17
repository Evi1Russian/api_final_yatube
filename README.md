# Документация проекта yatube_api
 <br>
 Этот api испульзуется для взаимодействия с базой данных проекта yatube.<br>
 <br>
 Здесь можно: <br>
 Получать список постов пользователей<br>
 Создавать и редактировать посты<br>
 Удалять посты<br>
 Комментировать посты<br>
 Подписываться на авторов<br>
 <br>
 
 ## Установка проекта: 
 Клонируйте репозиторий,
 
 Установите виртуальное окружение командой **```python3 -m venv venv```**
 
 Активируйте виртуальное окружение командой **```source venv/Scripts/activate```**
 
 Подключите зависимости **```pip install -r requirements.txt```**
 
 Выполните миграции **```python manage.py migrate```**
 
 Запустите проект **```python manage.py runserver```**
 
 ## **Примеры запросов**<br>
 GET запрос  http://127.0.0.1:8000/api/v1/posts/{id}/<br>
  <br>
  Выведет информацию о посте с выбранным id<br>
{
 "id": 0,
 "author": "string",
 "text": "string",
 "pub_date": "2019-08-24T14:15:22Z",
 "image": "string",
 "group": 0
}
 <br>
 POST запрос http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/<br>
 Добавит комментарий к выбранному посту<br>
 <br>
{
"text": "string"
}
<br>
GET запрос http://127.0.0.1:8000/api/v1/follow/<br>
<br>
Выведет информацию о твоих подписках<br>
<br>
[
{
"user": "string",
"following": "string"
}
]
<br>
 

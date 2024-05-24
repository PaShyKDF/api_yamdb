# Ресурс отзывов на книги, фильмы, музыку

### Описание:

Проект собирает отзывы пользователей на произведения. Сами произведения в проекте не хранятся, здесь нельзя посмотреть фильм или послушать музыку. Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка». Список категорий может быть расширен.

Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят оценку в диапазоне от одного до десяти; из пользовательских оценок формируется усреднённая оценка произведения — рейтинг. На одно произведение пользователь может оставить только один отзыв. Добавлять отзывы, комментарии и ставить оценки могут только аутентифицированные пользователи.

### Стек технологий:

<img src="https://img.shields.io/badge/Python-3776ab?style=for-the-badge&logo=python&logoColor=yellow"/> <img src="https://img.shields.io/badge/Django Rest framework-092E20?style=for-the-badge&logoColor=white"/> <img src="https://img.shields.io/badge/JWT-2980b9?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAACVBMVEVGUViMoa/i5+sa4fYGAAAALElEQVQ4y2NgoAtghAMghwkZUFMBgoKJ0l/BqDdpoYCgG+iggA7eJEMBjQEA95EC+R9NCHIAAAAASUVORK5CYII="/> <img src="https://img.shields.io/badge/postman-FF6C37?style=for-the-badge&logo=postman&logoColor=FF4500"/> <img src="https://img.shields.io/badge/json-000000?style=for-the-badge&logo=json&logoColor=white"/> <img src='https://img.shields.io/badge/sqlite-sqlite?style=for-the-badge&logo=sqlite&labelColor=072B8A&color=072B8A'>

### Как развернуть проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:PaShyKDF/api_yamdb.git
```

```
cd api_yamdb
```

Cоздать и активировать виртуальное окружение:

```
python -m venv мenv
```

```
source env/bin/activate
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
 
### Примеры запросов:

GET **/titles/**

```
{
  "count": 0,
  "next": "string",
  "previous": "string",
  "results": [
    {
      "id": 0,
      "name": "string",
      "year": 0,
      "rating": 0,
      "description": "string",
      "genre": [
        {
          "name": "string",
          "slug": "string"
        }
      ],
      "category": {
        "name": "string",
        "slug": "string"
      }
    }
  ]
}
```

POST **/titles/**

Request:

```
{
  "name": "string",
  "year": 0,
  "description": "string",
  "genre": [
    "string"
  ],
  "category": "string"
}
```

Responce:

```
{
  "id": 0,
  "name": "string",
  "year": 0,
  "rating": 0,
  "description": "string",
  "genre": [
    {
      "name": "string",
      "slug": "string"
    }
  ],
  "category": {
    "name": "string",
    "slug": "string"
  }
}
```

GET **/titles/{title_id}/reviews/**

```
{
  "count": 0,
  "next": "string",
  "previous": "string",
  "results": [
    {
      "id": 0,
      "text": "string",
      "author": "string",
      "score": 1,
      "pub_date": "2019-08-24T14:15:22Z"
    }
  ]
}
```

POST **/titles/{title_id}/reviews/**

Request:

```
{
  "text": "string",
  "score": 1
}
```

Responce:

```
{
  "id": 0,
  "text": "string",
  "author": "string",
  "score": 1,
  "pub_date": "2019-08-24T14:15:22Z"
}
```

>Авторы: [Евгений Братанов](https://github.com/ZhenyaSonic), [Борисов Максим](https://github.com/Wayer5), [Клищенко Павел](https://github.com/PaShyKDF).
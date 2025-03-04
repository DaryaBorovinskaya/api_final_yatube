# API_FINAL_YATUBE

## Описание проекта

API для социальной сети yatube. Проект реализован с помощью фреймворка Django с использованием DRF.


## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/DaryaBorovinskaya/api_final_yatube.git
```

```
cd yatube_api
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```
    
## Примеры запросов к API

### POST

Создание публикации: добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.

http://127.0.0.1:8000/api/v1/posts/


Результат:

```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```

### GET

Список сообществ: получение списка доступных сообществ.

http://127.0.0.1:8000/api/v1/groups/ 


Результат:

```
[
  {
    "id": 0,
    "title": "string",
    "slug": "^-$",
    "description": "string"
  }
]
```


### PATCH

Частичное обновление публикации: частичное обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.

http://127.0.0.1:8000/api/v1/posts/{id}/ 

Результат:

```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```
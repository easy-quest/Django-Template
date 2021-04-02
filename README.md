# Разработка Django на Repl.it

- этот шаблон, чтобы начать
- Просто нажмите "Выполнить", чтобы запустить сервер.
- Сервер будет автоматически перезагружен по мере необходимости. Вам не нужно перезапускать сервер вручную.


## Добавьте свой первый просмотр

1. Создайте файл в `mysite` назовите `views.py` со следующим содержанием:

```
from django.http import HttpResponse


def index(request):
    return HttpResponse("Hello, world.")
```

2. Добавьте шаблон URL в `mysite/urls.py`. Должно получиться так: 

```
from django.contrib import admin
from django.urls import path
from . import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.index, name='index'),
]
```

## Shell

Django utilizes the shell for managing your site. For this click on the `?` in the lower-right corner and click "Workspace shortcuts" from there you can open a new shell pane. 

## Database

By default this template utilizes the sqlite database engine. While this is fine for development it won't work with external users of your app as we don't persist changes to files when they happen outside the development environment. 

We suggest bringing a database using an outside service. 

See Django documentation on how to setup a database: https://docs.djangoproject.com/en/3.0/intro/tutorial02/


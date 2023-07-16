#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

# Проект kittygram369 показывает миру фотографии котов
автор Демидов Ю.Е.
В проекте используется технология контейнеризации Docker и автоматизация процесса развертывания Django-проектов.

Примеры запросов:
Главная страница
https://kittygram369.hopto.org/
Админка:
https://kittygram369.hopto.org/admin
Api
https://kittygram369.hopto.org/api

Как запустить проект: Клонировать репозиторий и перейти в него в командной строке:

git clone git@github.com:RV369/kittygram_final.git

cd kittygram_final

Cоздать и активировать виртуальное окружение:

python -m venv env

source env/Scripts/activate

Установить зависимости из файла requirements.txt:

pip install -r requirements.txt

Выполнить миграции:

python3 manage.py migrate

Создать пользователя:

python manage.py createsuperuser

Запустить проект:
Установите Windows Subsystem for Linux по инструкции с официального сайта Microsoft
https://learn.microsoft.com/ru-ru/windows/wsl/install. 
Зайдите на официальный сайт проекта и скачайте установочный файл Docker Desktop.
https://www.docker.com/products/docker-desktop/
Запустите его: на ваш компьютер будет установлена программа для управления контейнерами (докер-демон) и докер-клиенты — графический интерфейс и интерфейс командной строки.

Выполните команду в терминале
docker compose up --build

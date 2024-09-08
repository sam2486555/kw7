**ТРЕКЕР ПОЛЕЗНЫХ ПРИВЫЧЕК С ИСПОЛЬЗОВАНИЕМ DRF.**

**Описание**

Трекер полезных привычек. Создайте привычку и Вы будете получать уведомление о ней в телеграм


**Для работы с проектом необходимо.**  
- Клонировать репозиторий на компьютер используя SSH ключ.
- Создать зависимости, выполнив команду poetry install.
- В файл .env внесите свои данные (необходимые переменные перечислены в файле .env.sample)
- создайте и примените миграции (python manage.py makemigrations, python manage.py migrate)
- установите Redis, запустите командой redis-server
- для запуска проекта наберите в терминале команду python manage.py runserver
- программе Postman, в админке зарегистрируйтесь и создайте привычки
- в терминале запустите celery worker командой:
  celery -A config worker -l INFO  # для Mac и Linux
  celery -A config worker -l INFO -P eventlet  # для Windows
- в другом терминале запустите celery beat командой:
  celery -A config beat -l info -S django
- зайдите в телеграм бот и нажмите START


**Документация API**

Документация API доступна после запуска сервера по адресу: http://localhost:8000/redoc/ или http://localhost:8000/docs/
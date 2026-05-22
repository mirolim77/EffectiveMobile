Запуск 

docker compose -f EffectiveMobile.yaml  up -d


Проверка работоспособности

docker inspect --format='{{.State.Health.Status}}' backend-app


Клиент отправляет запрос → его принимает NGINX → NGINX решает, куда передать запрос дальше → пересылает его на backend-app,   backend обрабатывает логику и возвращает ответ → NGINX отдает ответ клиенту.
Типичная схема:

Пользователь
    ↓
NGINX
    ↓
Backend-приложение

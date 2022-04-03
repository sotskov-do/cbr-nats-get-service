# Получение курсов валют через API ЦБ РФ

Представляет собой композицию следующих сервисов:
1. Сервис **cbr** получает данные о курсах доллара США и Евро из API ЦБ РФ и помещает их в очередь NATS;
2. NATS;
3. Сервис **get-from-nats** позволяет по GET запросу получить накопленные в очереди данные.

## Инструкция по запуску:

~~~
1. git clone https://github.com/Sidio01/cbr-nats-get-service.git
2. cd cbr-nats-get-service
3. docker-compose build
4. docker-compose up
~~~
Запросы следует отправлять на http://127.0.0.1:8080/get/
# Рабочие дни биржи

## Проверить день

> Пример запроса - "Работает ли биржа в следующую пятницу?"

```python
import requests

resp = requests.post("http://data.conomy.ru/api/workingday/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'},
                     data={'date': '9.12.2001'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/workingday?date=9.12.2001" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

По этому адресу можно проверить работает ли биржа в указанный день (дату), как в прошлом так и в будущем.

<aside class="notice">
Еcли этот запрос передать без параметров, то ответом будет результат проверки текущего дня. 
Пример:
<code>http://data.conomy.ru/api/workingday/</code>
</aside>

> Ответный JSON:

```json
{
    "date": "19.12.2001",
    "stock_is_working": true
}
```

### HTTP Request

`GET http://data.conomy.ru/api/workingday?date=<date>`

Параметр | Формат | По Умолчанию | Описание
-------- | -------| ------------ | --------
date | д.м.ггг | Текущий день | Интересующая дата

## Рабочее время

> Пример запроса - "Работает ли биржа в следующую пятницу в пол пятого?"

```python
import requests

resp = requests.post("http://data.conomy.ru/api/workingday/time/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'},
                     data={'datetime': '9.12.2001 18:33:00'})
resp.json()
```

```shell 
curl -X GET "http://data.conomy.ru/api/workingday/time?datetime=9.12.2001 16:33:00 \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

Чтобы узнать работает ли биржа в указаный день в указаное время
передайте в параметре <code>datetime</code> дату и время. Как в примере.

> Ответный JSON:

```json
{
    "datetime": "08.01.2001 16:33:00",
    "stock_is_working": true
}
```

### HTTP Request

`GET http://data.conomy.ru/api/workingday/time?datetime=<datetime>`

Параметр | Формат | По Умолчанию | Описание
-------- | ------ | ------------ | --------
datetime | д.м.гггг чч:мм:cc | Текущий день, текущее время | Интересующая дата и время
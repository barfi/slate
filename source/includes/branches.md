# Отрасли

## Список Отраслей

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/branch/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/branch/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

> Ответный JSON:

```json
[
    {
        "id": 1,
        "url": "/api/stock/branch/1/",
        "name": "IT"
    },
    {
        "id": 2,
        "url": "/api/stock/branch/2/",
        "name": "OIL"
    }
]
```

Этот запрос вернёт список всех отрослей.

### HTTP Request

`GET http://data.conomy.ru/api/stock/branch/`

## Отрасль Детально

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/branch/2/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/branch/2/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```


> Ответный JSON:

```json
{
    "id": 1,
    "url": "/api/stock/branch/1/",
    "name": "IT",
    "issuers": []
}
```

Этот запрос детальную информацию о конкретной отрасли.

### HTTP Request

`GET http://data.conomy.ru/api/stock/branch/<ID>`

### Параметры Запроса

Параметр | Описание
-------- | -----------
ID | Уникальный идентификатор отрасли
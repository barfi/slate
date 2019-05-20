# Облигации

## Список Облигаций

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/bond/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/bond/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "count": 2,
    "next": null,
    "previous": null,
    "results": [
        {
            "url": "/api/stock/bond/RU000A0JUAH8/",
            "symbol": "RU000A0JUAH8",
            "price": null,  
            "name": "РЖД",
            "right": true,
            "right_primary": false,
            "uuid": "1c6cbd29-7116-4332-9188-0b55fdc23bef"
        },
        {
            "url": "/api/stock/bond/007/",
            "symbol": "007",
            "price": null,
            "name": "James",
            "right": false,
            "right_primary": false,
            "uuid": "b39a9894-e435-4896-a962-1c69d5f78b0f"
        }
    ]
}
```

Этот запрос вернёт список всех облигаций.

### HTTP Request

`GET http://data.conomy.ru/api/stock/bond/`

## Конкретная Облигация

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/bond/RU000A0JUAH8/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/bond/RU000A0JUAH8/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "history": "/api/stock/bond/RU000A0JUAH8/history/",
    "price": {},
    "mat_date": "01.06.2019",
    "uuid": "1c6cbd29-7116-4332-9188-0b55fdc23bef",
    "name": "РЖД",
    "pretty_name": "RJD",
    "symbol": "RU000A0JUAH8",
    "conomy_id": 2,
    "min_step": null,
    "lot_size": 1,
    "right": true,
    "right_primary": false,
    "stock_exchange": "micex"
}
```

Этот запрос вернёт детальную информацию о запрошенной облигации.

### HTTP Request

`GET http://data.conomy.ru/api/stock/bond/<symbol>/`

### Параметры Запроса

Параметр | Описание
-------- | -----------
symbol | Символ тикера под которым он зарегистрирован на бирже.

## История Облигации

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/bond/RU000A0JUAH8/history/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/bond/RU000A0JUAH8/history/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "count": 0,
    "next": null,
    "previous": null,
    "results": []
}
```

Этот запрос вернёт исторические данные о запрошенной облигации.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/<symbol>/history/`

### Параметры Запроса

Параметр | Описание
-------- | -----------
symbol | Символ облигации под которым она зарегистрирован на бирже.
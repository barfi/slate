# Тикеры

## Список тикеров

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/ticker/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/ticker/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Этот код вернёт JSON структурированный следующим образом:

```json
[
  {
    "url": "/api/stock/ticker/micex/GZP/",
    "symbol": "GZP",
    "name": "GAZPRM",
    "uuid": "76401d54-0a45-4514-a701-973d79e042ff",
    "price": null,
    "price_date": null,
    "priv": false,
    "stock_exchange": "micex"
  },
  {
    "url": "/api/stock/ticker/micex/LKOH/",
    "symbol": "LKOH",
    "name": "Лукоил",
    "uuid": "c0b0e353-a9fe-4567-8b63-c6c29b133359",
    "price": null,
    "price_date": null,
    "priv": false,
    "stock_exchange": "micex"
  }
]
```

Этот запрос вернёт список всех тикеров.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/`

## Конкретный Тикер

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/ticker/LKOH/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/ticker/LKOH" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "history": "/api/stock/ticker/micex/LKOH/history/",
    "issuer": {
        "uuid": "e234a68c-ddcf-478f-8019-25c1abdff4ca",
        "conomy_issuer_id": 2,
        "edisclosure_id": 2,
        "name": "Лукоил",
        "url": "/api/stock/issuer/e234a68c-ddcf-478f-8019-25c1abdff4ca/"
    },
    "potential": {},
    "price": {},
    "uuid": "c0b0e353-a9fe-4567-8b63-c6c29b133359",
    "name": "",
    "symbol": "LKOH",
    "priv": false,
    "listing_level": 2,
    "liquidity": 2,
    "stock_exchange": "micex",
    "kz_id": null
}
```

Этот запрос вернёт детальную информацию о запрошеном тикере.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/<symbol>`

### Параметры Запроса

Параметр | Описание
-------- | -----------
symbol | Символ тикера под которым он зарегистрирован на бирже.

## История Тикера

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/ticker/LKOH/history/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/ticker/LKOH/history/" \
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

Этот запрос вернёт исторические данные о запрошенном тикере.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/<symbol>/history/`

### Параметры Запроса

Параметр | Описание
-------- | -----------
symbol | Символ тикера под которым он зарегистрирован на бирже.


## Тикер На Бирже

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/ticker/mixec/LKOH/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/ticker/micex/LKOH/" \
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

Этот запрос вернёт детальную информацию о запрошенном тикере торгующемся на указанной бирже.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/<exchange>/<symbol>/`

### Параметры Запроса

Параметр | Описание
-------- | -----------
exchange | Символ интересующей биржи.
symbol | Символ тикера под которым он зарегистрирован на бирже.

<aside class="success">
На данный момент в системе заведены следующие биржи:
<code>micex</code> - Московская фондовая биржа
<code>kasa</code> - Казахская фондовая биржа
</aside>


## История Тикера На Бирже

> Пример запроса:

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/ticker/mixec/LKOH//",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/ticker/mixec/LKOH/history/" \
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

Этот запрос вернёт исторические данные о запрошенном тикере 
торгующемся на указанной бирже.

### HTTP Request

`GET http://data.conomy.ru/api/stock/ticker/<exchange>/<symbol>/history/`

### Параметры Запроса

Параметр | Описание
-------- | -----------
exchange | Символ интересующей биржи.
symbol | Символ тикера под которым он зарегистрирован на бирже.

<aside class="success">
На данный момент в системе заведены следующие биржи:
<code>micex</code> - Московская фондовая биржа
<code>kasa</code> - Казахская фондовая биржа
</aside>

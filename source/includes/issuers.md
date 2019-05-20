# Эмитенты

## Спсиок Эмитентов

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/issuer/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/issuer/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
[
    {
        "uuid": "03c43779-b0dd-49fd-8705-56429ea499c8",
        "conomy_issuer_id": 1,
        "edisclosure_id": 1,
        "name": "Лукоил",
        "url": "/api/stock/issuer/03c43779-b0dd-49fd-8705-56429ea499c8/"
    },
    {
        "uuid": "c436f604-4a80-44f1-98f2-c2be31f5bb79",
        "conomy_issuer_id": 2,
        "edisclosure_id": 2,
        "name": "Яндекс",
        "url": "/api/stock/issuer/c436f604-4a80-44f1-98f2-c2be31f5bb79/"
    }
]
```

Этот запрос вернёт список всех эмитентов.

### HTTP Request

`GET http://data.conomy.ru/api/stock/issuer/`

## Отрасль Детально

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/issuer/c436f604-4a80-44f1-98f2-c2be31f5bb79/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/issuer/c436f604-4a80-44f1-98f2-c2be31f5bb79/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "id": 2,
    "uuid": "c436f604-4a80-44f1-98f2-c2be31f5bb79",
    "conomy_issuer_id": 2,
    "edisclosure_id": 2,
    "branch": {
        "id": 1,
        "url": "/api/stock/branch/1/",
        "name": "IT"
    },
    "tickers": [],
    "potential": {},
    "name": "Яндекс",
    "conomy_id": 2,
    "rsbu_id": 2,
    "msfo_id": 2,
    "yearly_id": 2,
    "conomy_reports_url": "",
    "dividend_id": 2,
    "dividend_url": "",
    "s3cloud_id": null,
    "need_parse": false
}
```

Этот запрос детальнуюинформацию о конкретном эмитенте.

### HTTP Request

`GET http://data.conomy.ru/api/stock/issuer/<uuid>`

### Параметры Запроса

Параметр | Описание
-------- | -----------
uuid | Уникальный идентификатор эмитента
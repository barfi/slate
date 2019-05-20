# Дивиденды

## Список Дивидендов

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/divident/", 
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
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "url": "/api/stock/dividend/444f3915-963a-4cb3-80a5-acde91897f06/",
            "ticker": "LKOH",
            "dividend_period_start": "24.05.2019",
            "dividend_period_end": "24.05.2019",
            "cutoff_OCA": "24.05.2019",
            "cutoff_div": "31.05.2019",
            "cutoff_div_t_plus_2": "29.05.2019",
            "uuid": "444f3915-963a-4cb3-80a5-acde91897f06",
            "amount": "32.0000000000000000000000000",
            "status": "r",
            "date": "2019-05-19"
        }
    ]
}
```

Этот запрос вернёт список дивидендов.

### HTTP Request

`GET http://data.conomy.ru/api/stock/dividend/`

## Детальная информация о дивиденде

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/dividend/444f3915-963a-4cb3-80a5-acde91897f06/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/dividend/444f3915-963a-4cb3-80a5-acde91897f06/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Ответный JSON:

```json
{
    "url": "/api/stock/dividend/444f3915-963a-4cb3-80a5-acde91897f06/",
    "ticker": "LKOH",
    "dividend_period_start": "24.05.2019",
    "dividend_period_end": "24.05.2019",
    "cutoff_OCA": "24.05.2019",
    "cutoff_div": "31.05.2019",
    "cutoff_div_t_plus_2": "29.05.2019",
    "uuid": "444f3915-963a-4cb3-80a5-acde91897f06",
    "amount": "32.0000000000000000000000000",
    "status": "r",
    "date": "2019-05-19"
}
```

Этот запрос вернёт детальную информацию о дивиденде.

### HTTP Request

`GET http://data.conomy.ru/api/stock/dividend/<uuid>/`

Параметр | Описание
-------- | -----------
uuid | Уникальный идентификатор дивиденда.

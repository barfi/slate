# Валюты	

## Список Валют

```python
import requests

resp = requests.post("http://data.conomy.ru/api/currency/",
                     headers={'Authorization': 'Token 7449b408f6a7dd35292dffb7ff198d33636770be'})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/currency/" \
  -H "Authorization: Token 7449b408f6a7dd35292dffb7ff198d33636770be"
```

```javascript

```

> Этот код вернёт JSON структурированный следующим образом:

```json
[
    {
        "name": "Dollar",
        "value": 64.6306
    },
    {
        "name": "Рубль",
        "value": null
    }
]
```

Этот запрос вернёт список всех валют.

### HTTP Request

`GET http://data.conomy.ru/api/currency/`

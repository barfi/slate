# Индексы

## Список индексов

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/index/",
                     headers={},
                     data={})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/index/"
```

```javascript

```

> Ответный JSON:

```json
{
	
}
```

## Детальная информация об Индексе

```python
import requests

resp = requests.post("http://data.conomy.ru/api/stock/index/<symbol>",
                     headers={},
                     data={})
resp.json()
```

```shell 
curl "http://data.conomy.ru/api/stock/index/"
```

```javascript

```
> Ответный JSON:
```json
{
	
}
```

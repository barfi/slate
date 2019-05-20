---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python

toc_footers:
  - <a href=''>Получить API-ключ</a>

includes:
  - tickers
  - bonds
  - dividends
  - currencies
  - branches
  - issuers
  - workingdays
  - errors

search: true
---

# Введение

Добро пожаловать в  Conomy Data  API!   Вы можете использовать наше API для взаимодествия с сервисом Conomy Data.

В документации показаны примеры использования Shell и Python. Вы можете увидеть примеры кода в темной зоне справа, и вы можете переключить язык программирования примеров во вкладках сверху справа.

# Аутентификация

> Пример авторизации при запроседетальной информации об облигации:

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

> Этот код вернёт JSON структурированный следующим образом:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  }
]
```

Data использует API-ключи для разрешения доступа к API. Вы можете зарегистрировать новый Data API-ключ [на портале для разработчиков](http://conomy.ru/developers).

Data ожидает что API-ключи будут вложены в хэдер всех API запросов на сервер. Это выглядит так:

`Authorization: Token <api-key>`

<aside class="notice">
Вы должны заменить <code>api-key</code> на Ваш персональный API-ключ.
</aside>



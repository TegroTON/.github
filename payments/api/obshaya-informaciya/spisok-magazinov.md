# Список магазинов

> **POST** https://tegro.money/api/shops/

Получение списка ваших магазинов

### Запрос

| Header        |        |                 |
| ------------- | ------ | --------------- |
| Authorization | string | Подпись запроса |

| Body     |         |                          |
| -------- | ------- | ------------------------ |
| shop\_id | string  | Shop ID                  |
| nonce    | integer | Уникальный номер запроса |

### Ответ

```json
{
  "type": "success",
  "desc": "",
  "data": {
    "user_id": 1,
    "shops": [
      {
        "id": 1,
        "date_added": "2020-11-03 18:04:07",
        "name": "DEMO1",
        "url": "https://demo1",
        "status": 1,
        "public_key": "D0F98E7DD86BB7500914",
        "desc": "DEMO1 SHOP"
      },
      {
        "id": 2,
        "date_added": "2020-11-03 22:38:58",
        "name": "DEMO2",
        "url": "https://demo2",
        "status": 0,
        "public_key": "1913EA935149B1E5D852A",
        "desc": "DEMO2 SHOP"
      }
    ]
  }
}
```

### Пример запроса

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880
}
```

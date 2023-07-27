# Баланс

> **POST** https://tegro.money/api/balance/

Получение баланса всех кошельков

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
    "balance": {
      "RUB": "1396.68",
      "USD": "0.00",
      "EUR": "1.23",
      "UAH": "0.00"
    }
  }
}
```

### Пример запроса

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880,
  "currency": "RUB",
  "amount": 1200,
  "order_id": "test order",
  "payment_system": 5,
  "fields": {
    "email": "user@email.ru",
    "phone": "79111231212"
  },
  "receipt": {
    "items": [
      {
        "name": "test item 1",
        "count": 1,
        "price": 600
      },
      {
        "name": "test item 2",
        "count": 1,
        "price": 600
      }
    ]
  }
}
```

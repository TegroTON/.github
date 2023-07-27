# Создание заказа

> **POST** https://tegro.money/api/createOrder/

Используйте этот метод для получения прямой ссылки на оплату заказа

### Запрос

<table><thead><tr><th width="329.3333333333333">Header</th><th></th><th></th></tr></thead><tbody><tr><td>Authorization</td><td>string</td><td>Подпись запроса</td></tr></tbody></table>

| Body            |         |                                |
| --------------- | ------- | ------------------------------ |
| shop\_id        | string  | Shop ID                        |
| nonce           | integer | Уникальный номер запроса       |
| currency        | string  | Валюта оплаты, RUB/USD/EUR etc |
| amount          | number  | Сумма оплаты                   |
| order\_id       | string  | Номер заказа в Вашем магазине  |
| payment\_system | integer | ID платежной системы           |
| fields          | array   | Данные о покупателе            |
| receipt         | array   | Данные о корзине               |

### Ответ

```json
{
  "type": "success",
  "desc": "",
  "data": {
    "id": 755555,
    "url": "https://tegro.money/pay/complete/755555/7f259f856e7682a6e98179036a623696/"
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

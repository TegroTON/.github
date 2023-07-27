# Список заказов

> **POST** https://tegro.money/api/orders/

Получение информации о заказах

### Запрос

<table><thead><tr><th width="283.3333333333333">Header</th><th></th><th></th></tr></thead><tbody><tr><td>Authorization</td><td>string</td><td>Подпись запроса</td></tr></tbody></table>

<table><thead><tr><th>Body</th><th width="182.33333333333331"></th><th></th></tr></thead><tbody><tr><td>shop_id</td><td>string</td><td>Shop ID</td></tr><tr><td>nonce</td><td>integer</td><td>Уникальный номер запроса</td></tr><tr><td>page</td><td>integer</td><td>Страница</td></tr></tbody></table>

### Ответ

```json
{
  "type": "success",
  "desc": "",
  "data": [
    {
      "id": 123,
      "date_created": "2020-11-14 23:32:37",
      "date_payed": "2020-11-14 23:33:39",
      "status": 1,
      "payment_system_id": 10,
      "currency_id": 1,
      "amount": "64.18000000",
      "fee": "4.00000000",
      "email": "user@somesite",
      "test_order": 0,
      "payment_id": "Order #4175"
    },
    {
      "id": 124,
      "date_created": "2020-11-14 23:30:05",
      "date_payed": null,
      "status": 0,
      "payment_system_id": 10,
      "currency_id": 1,
      "amount": "64.18000000",
      "fee": "4.00000000",
      "email": "user2@somesite",
      "test_order": 0,
      "payment_id": "Order #4174"
    }
  ]
}
```

### Пример запроса

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880,
  "page": 1
}
```

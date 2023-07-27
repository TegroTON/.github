# Проверка заказа

> **POST** https://tegro.money/api/order/

Получение информации о заказе

### Запрос

| Header        |        |                 |
| ------------- | ------ | --------------- |
| Authorization | string | Подпись запроса |

| Body        |         |                            |
| ----------- | ------- | -------------------------- |
| shop\_id    | string  | Shop ID                    |
| nonce       | integer | Уникальный номер запроса   |
| order\_id   | integer | Номер платежа tegro.money  |
| payment\_id | string  | или номер платежа магазина |

### Ответ

```json
{
  "type": "success",
  "desc": "",
  "data": {
    "id": 1232,
    "date_created": "2020-11-14 23:32:37",
    "date_payed": "2020-11-14 23:33:39",
    "status": 1,
    "payment_system_id": 10,
    "currency_id": 1,
    "amount": "64.18000000",
    "fee": "4.00000000",
    "email": "user@site.ru",
    "test_order": 0,
    "payment_id": "Order #17854"
  }
}
```

### Пример запроса

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880,
  "payment_id": "test order"
}
```

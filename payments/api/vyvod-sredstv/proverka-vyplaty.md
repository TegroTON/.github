# Проверка выплаты

> **POST** https://tegro.money/api/withdrawal/

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

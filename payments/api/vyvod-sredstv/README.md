# Вывод средств

> **POST** https://tegro.money/api/createWithdrawal/

### Запрос

| Header        |        |                 |
| ------------- | ------ | --------------- |
| Authorization | string | Подпись запроса |

| Body            |         |                            |
| --------------- | ------- | -------------------------- |
| shop\_id        | string  | Shop ID                    |
| nonce           | integer | Уникальный номер запроса   |
| currency        | string  | Валюта RUB / USD / EUR etc |
| account         | string  | Номер счета для выплаты    |
| amount          | number  | Сумма                      |
| payment\_id     | string  | Идентификатор вывода       |
| payment\_system | integer | Платежная система          |

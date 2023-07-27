# Список выплат

> **POST** https://tegro.money/api/withdrawals/

### Запрос

<table><thead><tr><th width="250.33333333333331">Header</th><th></th><th></th></tr></thead><tbody><tr><td>Authorization</td><td>string</td><td>Подпись запроса</td></tr></tbody></table>

| Body     |         |                          |
| -------- | ------- | ------------------------ |
| shop\_id | string  | Shop ID                  |
| nonce    | integer | Уникальный номер запроса |
| page     | integer | Страница                 |

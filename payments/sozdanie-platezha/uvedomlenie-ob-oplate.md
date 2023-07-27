# Уведомление об оплате

После оплаты, на указанный в настройках Вашего магазина **URL уведомлений** будет отправлен запрос, содержащий информацию об оплате

<table><thead><tr><th width="412">Ключ</th><th>Описание</th></tr></thead><tbody><tr><td>shop_id</td><td>Публичный ключ проекта</td></tr><tr><td>amount</td><td>Сумма платежа</td></tr><tr><td>order_id</td><td>Идентификатор заказа</td></tr><tr><td>currency</td><td>Валюта платежа (RUB, USD, EUR)</td></tr><tr><td>test</td><td>Если был задан при оплате</td></tr><tr><td>sign</td><td>Подпись запроса</td></tr></tbody></table>

Подпись формируется так же как и при создании формы, но в формировании хеш участвуют все поля, например

```php
<?php 
$secret = 'GB%^&*YJni677';
$data = $_POST;
unset($data['sign']);
ksort($data);
$str = http_build_query($data);
$sign = md5($str . $secret);
```

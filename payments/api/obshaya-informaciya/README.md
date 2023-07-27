# Общая информация

## Получение API ключа

API ключ для доступа к REST сервису Tegro.money можно сгенерировать на странице настроек магазина [https://tegro.money/my/shop-settings/](https://tegro.money/my/shop-settings/)

![](<../../../.gitbook/assets/image (46).png>)

Все данные в запросах к сервису Tegro.money передаются методом POST по протоколу HTTP на адрес https://tegro.money/api/_method_. Параметры сообщения упаковываются в JSON-объект.

Вместе с запросом необходимо передавать подпись. Подписывать необходимо тело запроса целиком, в том виде, в котором оно отправляется на сервер Банка (после сериализации тела запроса в JSON для отправки по HTTP).

> В каждом запросе необходимо передавать параметр **nonce**, отличный от предыдущего! Например, можно использовать текущее время в секундах

Используйте для подписи ваш секретный ключ. Сформируйте подпись с алгоритмом SHA-256.

```php
<?php

$api_key = 'EEFA1913EA9D9351469B1E5D852A';

$data = array(
    'shop_id' =>'1913EA9D9351469B1E5D852A',
    'nonce' => time(),
);

$body = json_encode($data);
$sign = hash_hmac('sha256', $body, $api_key);


$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://tegro.money/api/orders/",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS =>$body,
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer $sign",
    "Content-Type: application/json"
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```

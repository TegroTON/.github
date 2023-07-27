# Отображение взаимозаменяемых токенов

В Tegro Wallet в приоритете в сети те метаданные, которые соответствуют стандарту метаданных токена.&#x20;

Для взаимозаменяемых/Fungible токенов Tegro Wallet будет отображать следующую информацию:

<table><thead><tr><th width="327.9256545410941" align="center">Поле</th><th align="center">Описание</th></tr></thead><tbody><tr><td align="center">Наименование</td><td align="center">Имя токена (например: "Tegro Gusev Ruban")</td></tr><tr><td align="center">Символ</td><td align="center">Символ токена (например: "TGR")</td></tr><tr><td align="center">Изображение</td><td align="center">URI, указывающий на логотип токена.</td></tr></tbody></table>

В случае если у взаимозаменяемого токена имеются поля имени и символа, которые есть и в аккаунте метаданных на цепочке, и в JSON-файле вне цепочки (связанные через поле URI на цепочке), тогда Tegro Wallet отдаст приоритет полям на цепочке.&#x20;

В случае если у взаимозаменяемого токена нет аккаунта метаданных на цепочке, тогда Tegro Wallet станет отображать данные из списка токенов**.** Данный список является устаревшим и не должен использоваться для размещения новых токенов. При чтении из списка токенов Tegro Wallet будет отображать следующую информацию:

<table><thead><tr><th width="325.94852864075295" align="center">Поле</th><th align="center">Описание</th></tr></thead><tbody><tr><td align="center">Наименование</td><td align="center">Имя токена (например: "Tegro Gusev Ruban")</td></tr><tr><td align="center">Символ</td><td align="center">Символ токена (например: "TGR")</td></tr><tr><td align="center">Изображение</td><td align="center">URI, указывающий на логотип токена</td></tr><tr><td align="center">extensions.coingeckoID</td><td align="center">Идентификатор токена, определенный API Coingecko. Tegro Wallet использует его для получения цены токена</td></tr></tbody></table>

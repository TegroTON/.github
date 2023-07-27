---
description: Основы устройства и работы DEX Tegro.Finance
---

# Механика работы

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

## Децентрализованная криптовалютная биржа Tegro.Finance

Tegro.Finance - это автоматизированный протокол ликвидности, который использует формулу постоянного продукта для предоставления ликвидности и обмена токенами. Он является децентрализованным, некастодиальным и безопасным способом для обмена токенами на платформе DEX.&#x20;

Функционал платформы основан на блокчейне TON (The Open Network), что позволяет ей использовать преимущества высокой пропускной способности, асинхронного исполнения и быстрого завершения, которые предлагает этот блокчейн.

Важно отметить, что преимущества блокчейна TON не ограничиваются только быстрой скоростью и асинхронным исполнением. Благодаря своей архитектуре и инновационным технологиям, TON обеспечивает высокую масштабируемость и безопасность для своих пользователей.&#x20;

Это особенно важно для DEX, где безопасность и масштабируемость играют ключевую роль в обеспечении устойчивости и надежности биржи.

Таким образом, использование блокчейна TON в качестве основы для DEX Tegro.Finance позволяет криптовалютной бирже предоставлять своим пользователям быструю и безопасную торговлю, а также устойчивость и надежность в долгосрочной перспективе.

## Пул ликвидности

Tegro.Finance использует смарт-контракты для управления пулом ликвидности, который состоит из резервов двух токенов. Эти токены могут быть добавлены в пул любым поставщиком ликвидности. После этого, поставщик ликвидности получает взамен специальные токены LP-токены, которые отслеживают его долю в общем объеме резервов токенов.

Когда пользователь хочет совершить обмен, система автоматически расчитывает новый курс обмена на основе текущих объемов резерва токенов. Для каждой пары токенов имеется свой пул ликвидности, управляемый своим смарт-контрактом. Каждый обмен приводит к изменению объемов резерва токенов и соответственно к изменению курса обмена.

Кроме того, поскольку поставщики ликвидности получают LP-токены в обмен на резервы токенов, они могут обменять эти токены на базовые токены в любое время, возвращая свою долю резервов.&#x20;

В целом, использование системы пула ликвидности является ключевым элементом для создания автоматизированного протокола ликвидности, так как это позволяет предоставлять надежную и устойчивую торговлю на платформе DEX.
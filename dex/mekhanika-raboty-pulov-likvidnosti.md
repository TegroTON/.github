---
description: Механика работы пулов ликвидности на DEX на примере TGR/TON
---

# ⚙ Механика работы пулов ликвидности

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>Механика работы пулов ликвидности на DEX на примере TGR/TON</p></figcaption></figure>

Обратите внимание, что данный материал создан с целью ознакомления со спецификой работы пулов ликвидности на [DEX Tegro.Finance.](https://tegro.finance/) Приведённые расчёты смоделированы для наглядного примера.

Мы не утверждаем, что нижеприведённые расчёты подходят под каждую криптобиржу: у всех DEX свои особенности, комиссии и прочее. Также хотим подчеркнуть, что помимо прочего обязательно нужно учитывать транзакционные расходы сети TON.

## Особенности пулов ликвидности на DEX-бирже Tegro.Finance <a href="#osobennosti-pulov-likvidnosti-na-dex-birzhe-tegro.finance" id="osobennosti-pulov-likvidnosti-na-dex-birzhe-tegro.finance"></a>

DEX-биржа Tegro.Finance взимает комиссию в размере 0.4% за каждый обмен. Из общей суммы комиссии 0.25% включается в пул ликвидности и распределяется между всеми поставщиками ликвидности.

Становясь поставщиком ликвидности на DEX-бирже важно знать несколько ключевых составляющих:

* При выводе токенов из пула их количество может отличаться от количества, переданного в пул ликвидности изначально. Это происходит из-за того, что в процессе обменов структура пула изменяется по алгоритму ребалансировки, который задан DEX-биржей;
* На итоговый результат влияют транзакционные издержки сети и комиссии при внесении и выведении активов из пула ликвидности;
* Объём комиссии зависит от оборота. Чем больше объём торгов, тем выше доход поставщика ликвидности;
* Держание криптовалюты в кошельке может быть выгоднее, чем внесение токенов в пул ликвидности - если одна из криптовалют сильно растёт или падает, то ребалансировка пула значительно уменьшает объём дорожающей монеты;
* Сумма комиссии распределяется между всеми поставщиками ликвидности: чем больше доля поставщика в пуле, тем выше доход он сможет получать.

## Схема работы пула ликвидности на DEX <a href="#skhema-raboty-pula-likvidnosti-na-dex" id="skhema-raboty-pula-likvidnosti-na-dex"></a>

Представим себе пул из 1500 TGR и 100 TON - мы будем округлять значения для лучшего понимания. Здесь лежит формула постоянного продукта: x\*y=k, где x - TON, y - TGR, k - константа.

Для данного пула ликвидности k = 100 TON \* 1500 TGR = 150,000. Курс x/y = 100 TON / 1500 TGR = 0.07 TON/TGR, можно сделать вывод, что 1 TGR равен 0.07 TON.

<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption><p>Суммы TON и TGR в пуле ликвидности (число TGR на скриншоте может отличаться)</p></figcaption></figure>

Предположим, что новый поставщик ликвидности вносит в пул 50 TON и 750 TGR, тогда k = 100 TON (текущий объём пула в TON) + 50 TON (добавляемый объём TON в пул) \* 1500 TGR (текущий объём пула в TGR) + 750 TGR (добавляемый объём TGR в пул) = 337,500.

Получается, что доля нового участника в пуле - 33.33%, которая высчитывается следующим образом: 50 TON (внесённые участником) / 150 TON (общее количество TON в пуле вместе с его долей).

Оценочная стоимость внесённых токенов: 750 TGR \* 0.07 TON/TGR + 50 TON = 102.5 TON.

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption><p>Внесение в пул 50 TON и 750 TGR (число TGR на скриншоте может отличаться)</p></figcaption></figure>

Допустим, что на DEX-биржу приходит заявка на обмен 10 TON за TGR. В пул ликвидности уходит: 0.25% / 10 TON = 0.025, то есть в пул уходит 10.025 TON = 10 TON + 0.025 TON.

Для сохранения k (337,500) в пуле ликвидности должно остаться 2 109.045 TGR. Получить это число можно так: 337,500 / (150 TON + 10.025 TON) = 2109.045.

Взамен 10 TON пользователь получает 140.955 TGR = 2250 TGR - 2109.045 TGR. По фактическому курсу 0.0709 TON/TGR = 10 TON / 140.955 TGR.

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption><p>Обмен 10 TON на 140.955 TGR (число TGR на скриншоте может отличаться)</p></figcaption></figure>

По итогу курс пула вырос и теперь будет использоваться для расчёта сумм TGR и TON при внесении ликвидности в пул новыми участниками так: 160.025 TON / 2109.045 TGR = 0,07587 TON/TGR.

Схема работы идентична при ситуации, когда на DEX-бирже обменивают TGR на TON.

Обратите внимание: равновесный курс будет снижаться, но при этом объём TGR в пуле ликвидности будет увеличиваться за счёт сокращения TON.

## Итоговые результаты поставщика ликвидности <a href="#itogovye-rezultaty-postavshika-likvidnosti" id="itogovye-rezultaty-postavshika-likvidnosti"></a>

Пользователь с долей в пуле ликвидности равной 33.33% владеет 702.9447 TGR = 33.33% \* 2109.045 TGR, а также 53.3363 TON = 33.33% \* 160.025 TON.

Указанные суммы в TGR и TON будут получены при выводе средств из пула ликвидности.

{% hint style="warning" %}
Обратите внимание: числа отличаются от изначально внесённых 750 TGR и 50 TON.
{% endhint %}

Оценочная стоимость токенов 702.9447 TGR \* 0.07587 TON/TGR + 53.3363 = 106.6687 TON.

Разница с начальной оценкой внесённых средств: 4.1687 TON = 106.6687 TON - 102.5 TON.

{% hint style="warning" %}
Обратите внимание: число не совпадает с ожидаемой долей комиссии: 33.33% \* 0.025 = 0.00833 TON. Это объясняется изменением объёмов криптовалюты TGR и TON в пуле, оценка проводится по обновлённому равновесному курсу.
{% endhint %}

Если бы пользователь не стал поставщиком ликвидности, то у него осталось бы 750 TGR и 50 TON, что по новому курсу: 750 TGR \* 0.07587 TON/TGR + 50 TON = 106.9025 TON.

Выходит, что разница с начальной оценкой получается больше: 4.4025 TON.

Объясняется разница уменьшением объёма TGR и увеличением TON в результате проведённой сделки: участник пула обменял свою долю TGR на TON.

{% hint style="info" %}
Непостоянные потери - разница результатов между внесением активов в пул ликвидности и их удержанием в криптокошельке. Со временем благодаря накоплению комиссии в пуле можно компенсировать возникающую разницу. Если движение цены актива будет слишком сильным, то разница может стать существенной. Будет необходимо длительное время и большое количество обменов на DEX-бирже, чтобы доход от комиссии стал соизмеримым.
{% endhint %}
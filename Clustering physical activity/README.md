# Исследование данных Samsung. Кластеризация физической активности пользователей

В этой работе мы попрактикуемся в решении задач кластеризации и используем полученные знания, чтобы оценить результаты.

## Данные
Мы будем использовать данные, взятые с датчиков акселерометров и гироскопов смартфонов Samsung Galaxy S3.
Телефоны носили в кармане добровольцы в возрасте от 19 до 49 лет. Смартфоны постоянно фиксировали значения 
ускорения и скорости по трём измерениям, а поведение людей записывали на видео, чтобы вручную отметить, какую 
физическую активность осуществлял человек в тот или иной момент.

Данные содержат следующие признаки:
- различные показатели с акселерометра и гироскопа;
- метка активности (физическая активность человека в конкретный момент).

## Задача
Попробуем на основе данных с гироскопа и акселерометра разделить активности людей на некоторые схожие по
своим характеристикам группы. В идеале наблюдения во время ходьбы должны попасть в один кластер, наблюдения
во время подъёма по лестнице — в другой и т. д.

## Метрики
Рассчитываются два типа мер: внутренние (коэф. силуэта, инд. Калински-Харабаса, инд. Дэвиса-Болдина) и внешние (однородность, 
полнота, скорректированный инд. Рэнда).

## Содержание
- Загрузка и обработка данных
- Кластеризация
  * KMeans
    - Расчет внутренних мер
    - Расчет внешних мер
    - Классификация активности
  * AgglomerativeClustering
  * DBSCAN
  * GaussianMixture
    - Расчет внутренних мер
    - Расчет внешних мер
    - Классификация активности
- Итог

## Результат
К сожалению, ни одна из созданных нами моделей не способна верно распознавать типы активностей пользователей смартфонов.
Однако у нас получились в целом три модели, сносно различающих классы типы активностей, характеризующих движение и пассивное
состояние. Лучшей из трех наших моделей является модель, основанная на алгоритме аггломеративной кластеризации.

Наше решение не является идеальным, но и вряд ли исчерпывает возможности алгоритмов кластеризации вообще. Однако,
т.к. данные в нашей задаче имеют разметку, эту самую задачу можно попытаться также решить с помощью алгоритмов
классификации. Но этим все же мы займемся не здесь.

## [Тетрадка с работой](https://github.com/khav-i/ml_works/blob/master/Clustering%20physical%20activity/clustering%20physical%20activity.ipynb)

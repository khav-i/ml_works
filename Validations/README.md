# Валидация данных и оценка модели на примере датасета о качестве воды

## Контекст
Доступ к безопасной питьевой воде имеет важное значение для здоровья, является основным правом человека и компонентом
эффективной политики охраны здоровья. Это важно как вопрос здравоохранения и развития на национальном, региональном и местном уровне.
Было показано, что в некоторых регионах инвестиции в водоснабжение и санитарию могут принести чистую экономическую выгоду,
поскольку сокращение неблагоприятных последствий для здоровья и затрат на здравоохранение перевешивает затраты на проведение мероприятий.

## Коротко о данных
В данной работе мы используем [популярный датасет из Kaggle о качестве воды](https://www.kaggle.com/datasets/adityakadiwal/water-potability).
Датасет содержит показатели качества воды для 3276 различных водоемов.

## Задача
В этой работе мы будем решать задачу классификации: классифицировать воду на пригодную и не пригодную для питья на
основе её химического состава. Заодно рассмотрим методы валидации данных (hold-out, k-fold, leave-one-out) и оценки
качества моделей (pr-кривая, кривая обучения).

## Коротко о работе
Данная работа представляет собой своего рода методичку для более качественной работы с данными и потому содержит демонстрационные примеры
обработки синтетических данных.

## Содержание
1. HOLD-OUT валидация
2. K-FOLD валидация
3. LEAVE-ONE-OUT валидация
4. Дисбаланс выборки
5. Стратифицированное разбиение
6. Выбор метрик в условиях дисбаланса классов
7. Построение модели в условиях дисбаланса классов
   * Взвешивание объектов
   * Выбор порога вероятности. pr-кривая
   * Сэмплирование
8. Переобучение
9. Методы борьбы с переобучением
10. Построение кривой обучения

## Результат
Нам удалось оптимизировать модели для работы с данными с несбалансированными классами. Мы довольно быстро добились 
приемлемых показателей метрики $F_1$ - 0,69. Также мы рсавнили кривые обучения трех разных моделей:

![image](https://github.com/khav-i/ml_works/assets/126453765/29b0f32c-e45d-4487-9499-58467bef5bbc)

В целом же, из данной работе, полагаю, получилось даже собрать некоторое введение в такие сложную и глубокие темы 
как валидация данных и оценка моделей. Мне же будет просто удобно держать такую работу в своем репозитории :)

### [Перенестись к ноутбуку с работой](https://github.com/khav-i/ml_works/blob/master/Validations/validations.ipynb)
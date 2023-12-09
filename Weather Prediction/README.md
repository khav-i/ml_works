# Предсказание погоды

В этой работе мы возьмемся за нетривиальную задачу предсказания погоды — а именно нас интересует прогнозирование дождя на следующий день. Мы воспользуемся несколькими алогритмами, их модифицированными и оптимизированными вариантами, чтобы обучить модель, успешно справляющейся с обозначенной задачей. Критериями отбора модели будут стандартный набор метрик для классификационных задач: precision, recall, f1 score, accuracy, roc-auc.

## Данные
В нашем распоряжении датасет из 145 тысяч наблюдений за 2008-2017 годы из 49 метеорологических станций в Австралии. Данные доступны на [Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package).

## Содержание работы

* Загрузка и обработка данных
* Моделирование
  - Baseline model (LogisticRegression)
  - GaussianNB
  - KNeighborsClassifier
  - LinearSVC
  - SVC
  - SGDClassifier
  - MLPClassifier
  - Optuna(MLPClassifier)
  - DecisionTreeClassifier
  - Optuna(DecisionTreeClassifier)
  - AdaBoostClassifier
  - AdaBoostClassifier on Optuna(DecisionTreeClassifier)
  - Optuna(AdaBoostClassifier)
  - RandomForestClassifier
  - Optuna(RandomForestClassifier)
  - GradientBoostingClassifier
  - Optuna(GradientBoostingClassifier)
  - HistGradientBoostingClassifier
  - Optuna(HistGradientBoostingClassifier)
  - StackingClassifier
  - XGBClassifier
  - CatBoostClassifier
* Итог

## Результаты

В финальной части работы все расчитанные метрики моделей сведены в общую таблицу. Здесь мы ее приводить не станем: она довольно пространная. Выведем лишь таблицу из трех наилучших по сумме метрик моделей.

![image](https://github.com/khav-i/ml_works/assets/126453765/faa2f357-4864-429d-af22-c3fe54184555)

Стэкинг-модель оказалсь на данный момент лучшей, за ней следует классификатор CatBoost, и закрывает тройку оптимизировнный классификатор многослойного персептрона (стэкинг-модель включает и его также).

Стоит отметить характерную черту получившихся моделей — относительно невысокий recall: всем без исключения алгоритмам трудно находить в наших данных надежные обобщающие правила для дождей. Единственный способ улучшить показатели — произвести более качественную работу над данными: их, весьма вероятно, стоит дополнить из сторонних ресурсов.

## Посмотреть на ноутбук с работой можно [по ссылке](https://github.com/khav-i/ml_works/blob/master/Weather%20Prediction/weather_prediction.ipynb)

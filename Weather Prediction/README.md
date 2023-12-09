# Предсказание погоды

В этой работе мы возьмемся за нетривиальную задачу предсказания погоды — а именно нас интересует прогнозирование дождя
на следующий день. Мы воспользуемся несколькими алогритмами, их модифицированными и оптимизированными вариантами, чтобы
обучить модель, успешно справляющейся с обозначенной задачей. Критериями отбора модели будут стандартный набор метрик для 
классификационных задач: precision, recall, f1 score, accuracy, roc-auc.

## Данные
В нашем распоряжении датасет из 145 тысяч наблюдений за 2008-2017 годы из 49 метеорологических станций в Австралии.
Данные доступны на [Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package).

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



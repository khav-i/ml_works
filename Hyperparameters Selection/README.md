# Подбор гиперпараметров модели на примере прогнозирования биологического ответа молекул

Наша работа основана на соревновании [Kaggle: Predicting a Biological Response](https://www.kaggle.com/c/bioresponse) 
(Прогнозирование биологического ответа).

## Коротко о данных

Данные представлены в формате CSV. Каждая строка представляет молекулу. Первый столбец Activity содержит экспериментальные данные, описывающие фактический биологический ответ [0, 1]. 
Остальные столбцы D1-D1776 представляют собой молекулярные дескрипторы — это вычисляемые свойства, которые могут фиксировать некоторые характеристики молекулы, например размер, форму или состав элементов. 
Предварительная обработка не требуется, данные уже закодированы и нормализованы.

## Задача и метрика

Необходимо предсказать биологический ответ молекул (столбец 'Activity') по их химическому составу (столбцы D1-D1776).
В качестве метрики будем использовать F1-score. 
Необходимо обучить две модели: логистическую регрессию и случайный лес. 
Далее мы организуем подбор гиперпараметров с помощью базовых и продвинутых методов оптимизации. 
Будем использовать четыре метода (GridSeachCV, RandomizedSearchCV, Hyperopt, Optuna).

## Содержание

1. Знакомство с данными
2. Базовые модели
    2.1 Baseline Logistic Regression
    2.2 Baseline Random Forest
4. GridSearchCV
    3.1 Logistic Regression & GSCV
    3.2 Random Forest & GSCV
5. RandomizedSearchCV
    4.1 Logistic Regression & RSCV
    4.2 Random Forest & RSCV
6. Hyperopt
    5.1 Logistic Regression & Hyperopt
    5.2 Random Forest & Hyperopt
7. Optuna
    6.1 Logistic Regression & Optuna
    6.2 Random Forest & Optuna
8. Выводы

## Результаты

Коротко результаты можно представить в виде таблицы:

![image](https://github.com/khav-i/ml_works/assets/126453765/ead3297e-0fce-4862-b07b-583bb807da9b)

Подробнее с ходом работы можно ознакомиться в [версии ноутбука с интерактивной визуализацией](https://nbviewer.org/github/khav-i/ml_works/blob/master/Hyperparameters%20Selection/hyperparameters_selection.ipynb).

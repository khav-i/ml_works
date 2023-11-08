# Исследование зависимости продаж от рекламы
## Легенда
Допустим, нам дали задание построить прогностическую модель для продаж некоторого продукта на основе количества денег,
потраченных на рекламу. Более того, нас даже снабдили маленьким, симпатичным датасетиком.

И тут мы решили всласть оттянуться и попробовать написать собственные вариации градиентного спуска, дабы не терять
попусту столь удачный, не иначе как сочувствующим провидением подосланный, случай поправить уязвленное тяжелыми
буднями датасаентиста наше скромное самомненьице.

## Метрика
В качестве метрики мы выбрали среднеквадратическую ошибку, т.к. при сравнении моделей между собой она хорошо
подсвечивает разницу в их точностях.

## Содержание
- Загрузка и подготовка данных
- Классический градиентный спуск
- Координатный спуск
- Стохастический градиентный спуск

## Результат
![image](https://github.com/khav-i/ml_works/assets/126453765/a8a07fb0-8896-4ed3-91a5-6f75ce0e58d0)

Для данной задачи все наши модели показали себя примерно одинаково - с разницей от нескольких десятитысячных до тысячных
среднеквадратической ошибки. Наша модель стохастического градиентного спуска оказалась менее стабильной, чем все другие,
т.к. при реализации стохастического спуска вычисляются градиенты не для всей выборки, а только для случайно выбранной
единственной точки, поэтому от итерации к итерации итоговое значение метрики может несколько колебаться. Надо полагать,
библиотечный SGDRegressor реализован немного по-другому и более интереснее :)

## Непосредственно ознакомиться с проделанной работой можно [здесь](https://github.com/khav-i/ml_works/blob/master/Sales%20and%20advertising/sales_and_advertising.ipynb)
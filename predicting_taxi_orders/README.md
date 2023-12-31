# Прогнозирование заказов такси

Онлайн сервис заказа такси собрал исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. 

**Цель** - построить модель прогнозирования количества заказов такси на следующий час.

По техническому заданию значение метрики *RMSE* на тестовой выборке должно быть не больше 48. В качестве тестовой выборки использовать 10% от исходных данных.

**Использованные библиотеки и методы:** Python, Pandas, Python, Scikit-learn, statsmodels, временные ряды.

**Выводы**

В ходе исследования нами было оценено 5 моделей для прогнозирования количества заказов такси на следующий час. Наилучший показатель RMSE оказался у модели LinearRegression. Именно данная модель будет применяться для прогнозирования заказов!

| Модель                | RMSE               | 
| :---:                 |    :----:          | 
| **LinearRegression**      | **22.22**              |
| LGBMRegressor | 22.40|
| CatBoostRegressor | 22.60 |
| RandomForestRegressor | 22.85 |
| DecisionTreeRegressor | 24.23              | 

Лучшей моделью для прогнозирования количества заказов такси признана модель **LinearRegression**. Итоговое значение RMSE на тестовых данных составило 40.37. 

# Классификация комментариев

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. Клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 
Метрика качества - **F1**, которая должна быть не менее 0.75. В нашем распоряжении набор данных с разметкой о токсичности правок.

**Цель проекта** построить модель классификации комментариев на позитивные и негативные. 

**Использованные библиотеки и методы:** Python, Pandas, BERT, nltk, tf-idf.

**Выводы**

В ходе исследования выполнили:
- загрузку данных;
- токенизацию и лемматизацию;
- избавились от стоп-слов и ненужных символов;
- посмотрели частоту наиболее часто встречающихся слов в токсичном и нетоксичном текстах;
- расширили стандартный список стоп-слов; 
- провели вразделение данных на тренировочную и тестовую выборки;
- обучили и применили TFIDF векторизатор на тренировочных данных для последующей трансформации тестовых данных. 

Мы обучили 3 модели для обнаружения токсичных комментариев. Наилучший показатель метрики F1 оказался у модели LogisticRegression. 

| Модель                | F1 на тренировочной выборке|
| :---:                 |    :----:                  |
| **LogisticRegression**| **0.76**                   |
| LGBMRegressor         | 0.74                       |
| DecisionTreeClassifier| 0.57                       |                      |


Таким образом, лучшей моделью для обнаружения токсичных комментариев признана модель LogisticRegression c гиперпараметрами max_iter = 100, C = 10. Итоговое значение метрики F1 на тестовых данных составило 0.78. Модель успешно прошла тестирование!
# Рекомендация тарифов

В компании оператора связи произошло обновление тарифов, старые тарифы переводятся в архив и больше использоваться не будут. Компании необходим инструмент, который будет рекомендовать для каждого пользователя новый тариф, основываясь на особенностях его использования тарифных опций в прошлом. В нашем распоряжении данные о поведении клиентов, которые уже перешли на новые тарифные планы. 

**Цель** - построить модель для задачи классификации, которая выберет подходящий тариф для пользователя. 

Необходимо построить модель с максимально большим значением *accuracy*, по техническому заданию не менее 0.75. Предобработка данных уже проведена.   

**Использованные библиотеки и методы:** Python, Pandas, Scikit-learn, исследовательский анализ данных.

**Выводы**

В ходе исследования мы построили 3 модели для задачи классификации (распределение пользователей по типам тарифов), где основным параметром качества модели являлось значение **accuracy**.   

`Модель "дерево решений"` имеет **accuracy = 0.7778**, max_depth = 10, min_sample_split = 2.   
`Модель "случайный лес"` имеет **accuracy = 0.7960**, max_depth = 9, min_sample_split = 4, n_estimators = 15.   
`Модель логистической регрессии` имеет **accuracy = 0.7247**, max_iter = 100.   

Таким образом, при построении и обучении моделей на данном датасете, лучшей моделью стала `модель "случайный лес"`.   

Лучшая обученная модель (`"случайный лес"`) на тестовых данных показала значение аccuracy = 0.8035.   

При оценке адекватности разработанной модели проведено ее сранение со случайной моделью. Наша модель показала статистически значимо более высокие результаты качества, р-value = 0.000.
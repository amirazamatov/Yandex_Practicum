# Прогнозирование оттока клиентов (телеком)

Оператору связи требуется разработка модели прогнозирования оттока клиентов. Если модель спрогнозирует, что пользователь планирует уйти, ему будут предложены промокоды и специальные условия, чтобы он остался. Команда оператора собрала и предоставила персональные данные о некоторых клиентах (информацию об их тарифах и договорах) для построения и обучения модели. 
Согласно техническому заданию для оценки и обучения моделей необходимо использовать метрику **ROC-AUC**, дополнительно применять *Accuracy* и *F1*. Построенная модель должна иметь метрику **ROC-AUC >= 0.85**.

**Цель проекта** разработать прогностическую модель оттока клиентов.

**Использованные библиотеки и методы:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, imblearn, light_gbm, catboost, исследовательский анализ данных, визуализация данных, предобработка данных.

**Выводы**

В ходе исследования нами было оценено 4 модели для прогнозирования оттока клиентов. Наилучшие показатели оказались у модели **LGBMClassifier**. Именно данная модель будет представлена заказчику!

| Модель                | ROC_AUC      | Accuracy | F1      | 
| :---:                 |    :----:    |   :---:  | :---:   |
| DecisionTreeClassifier|   0.870      | 0.822    | 0.697   |
| RandomForestClassifier|   0.884      | 0.829    | 0.714   |
| **LGBMClassifier**    | **0.941**    |**0.924** |**0.857** |
| CatBoostClassifier    | 0.911        | 0.890    | 0.799    |     

Проверка работы модели на тестовых данных:
- Значение ROC_AUC на лучшей модели = 0.942
- Значение Accuracy на лучшей модели = 0.888
- Значение F1 на лучшей модели = 0.788

Таким образом, нами выполнено техническое задание - мы построили модель прогнозирования ухода клиентов с точностью предсказания 88%. Показатель ROC_AUC составил 0.942, что свидетельстует о высокой специфичности и чувствительности модели (мы предсказываем почти всех уходящих клиентов и в тоже время редко обозначаем клиента,который останется, как уходящего).

В качестве рекомендаций бизнесу можно посоветовать обратить внимание на характеристики пользователей, которые вошли в модель и имели наибольшую важность:
- оптимизировать методы оплаты
- уделять внимание клиентам, длительность контракта которых подходит к 1,5 годам 
- оптимизировать предоставление услуги Интернет. Многие пользователи вероятно не довольны данной услугой (дорого или плохое качество)
- предоставлять особые предложения пенсионерам, которые также подвержены частому уходу

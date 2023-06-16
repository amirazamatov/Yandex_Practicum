# Исследование объявлений о продаже квартир
В вашем распоряжении данные сервиса недвижимости - архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. 
Нужно научиться определять рыночную стоимость объектов недвижимости. Наша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность.

**Цель** - установить параметры, которые помогут определить рыночную цену квартиры в автоматизированной системе

**Использованные библиотеки и методы:** Python, Pandas, Matplotlib, исследовательский анализ данных, визуализация данных, предобработка данных.

**Выводы**

Анализ данных показал, что большинство объявлений описывают типовые варианты квартир и домов, построенных в советское время.
В целом, если рассматривать полученные результаты, то в автоматическую систему оценки рыночной стоимости квартиры скорее всего войдут следующие параметры:
- общая площадь
- жилая площадь
- площадь кухни
- количество комнат
- расстояние до центра города.
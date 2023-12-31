# Защита персональных данных клиентов
Необходимо защитить данные клиентов страховой компании. Перед нами стоит задача разработать такой метод преобразования данных, чтобы по нему было сложно восстановить персональную информацию. Обосновать корректность его работы.
В тоже время метод кодировки должен быть таким, чтобы при преобразовании качество моделей машинного обучения не ухудшалось. Подбирать наилучшую модель не требуется.

**Цель** - разработать модель анонимизации персональных данных.

**Использованные библиотеки и методы:** Python, NumPy, Scikit-learn

**Выводы**

В ходе исследования мы доказали, что умножение матрицы признаков на обратимую матрицу не изменяет качество модели линейной регрессии. На основе данной закономерности был предложен метод кодировки пользовательских данных. Работоспособность алгоритма была оценена путем сравнения метрики R2 для модели логистической регрессии на исходных и закодированных данных. Значение R2 не изменилось после кодирования данных!

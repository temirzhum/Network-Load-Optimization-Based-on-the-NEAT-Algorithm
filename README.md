# Network-Load-Optimization-Based-on-the-NEAT-Algorithm


Нейросеть, структура и веса которой эволюционируют алгоритмом NEAT, управляет параметром CIO (cell individual offset) базовых станций в гетерогенной сети LTE/5G. Цель: сбалансировать нагрузку и повысить удовлетворённость пользователей. 
Результаты сравниваются с RL (Attiah et al., 2020) и AWF (Gures et al., 2023).

# Требования

Python 3.8+
numpy, matplotlib, networkx, graphviz, torch

Модифицированная версия neat-python, которая входит в прилагаемый .zip. Папку neat нужно положить рядом с остальными библиотеками.



# Запуск

Запустите файл balance_neat.py

По умолчанию выполняется метод test_1, который тестирует выбранную популяцию через run_simulation из course.py.
Чтобы переключиться между NEAT и RL, закомментируй нужную строку в run_simulation (по умолчанию выбран NEAT).

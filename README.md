### Решатель квадратных уравнений

Программа предназначена для решения квадратных уровнений.

### Как использовать

Используя коэфициетны квадратного уравнения находим его корни.

### Как запустить

Скрипт требует для своей работы установленного интерпретатора Python версии 3.5
Импортируем в свой код модуль `python quadratic_equation`

Выполняем для данного модуля метод `get_roots(a, b, c)` где a, b, c - коэфициетнты квадратного уравнения, причём a не равно 0

Например:
```python
from math import sqrt
import sys


def get_roots(a, b, c):
    discriminant = b ** 2 - 4 * a * c
    if discriminant < 0:
        return None, None
    root1 = (-b - sqrt(discriminant)) / (2 * a)
    root2 = (-b + sqrt(discriminant)) / (2 * a)

    if discriminant == 0:
        return root1, None

    else:
        return root1, root2


a, b, c = int(sys.argv[1]), int(sys.argv[2]), int(sys.argv[3])
print(get_roots(a, b, c))
```

Исполнение через bash:

`name@localhost: ~/python3 quadratic_equation.py 2 4 1`

`(-1.7071067811865475, -0.2928932188134524)`

`name@localhost: ~/python3 quadratic_equation.py -2 4 -6`

`(None, None)`


### Цели проекта

Код создан в учебных целях. В рамках учебного курса по веб-разработке ― [DEVMAN.org](https://devman.org)


- # Проект Geometric Lib
Проект содержит функции для высчитывания площади и периметра различных фигур - квадрата, прямоугольника, треугольника, круга. 

Функция Area принимает измерения фигуры в зависимости от того, какие нужны для вычисления её площади.
Пример использования в Triangle.py:
```
def area(a, h): 
    return a * h / 2 
# Принимает сторону и высоту к ней треугольника a и h и возвращает его площадь
def perimeter(a, b, c): 
    return a + b + c 
# Принимает три стороны треугольника a,b,c и возвращает его периметр
print(area(4, 3))
6.0
```
Функция perimeter принимает измерения фигуры в зависимости от того, какие нужны для вычисления её периметра.
Пример Использования в Circle.py:
```
import math
def area(r):
    return math.pi * r * r
# Принимает значение радиуса окружности r и возвращает площадь круга с таким радиусом 

def perimeter(r):
    return 2 * math.pi * r
#  Принимает значение радиуса окружности r и возвращает длину круга с таким радиусом
print(perimeter(10))
62.8
```
История работы над проектом:
```
8c2c696 (HEAD -> Main, origin/Main) error fixed
d3e9c96 New file added
92d6d62 new file added
c48d495 .
d078c8d L-03: Docs added
8ba9aeb L-03: Circle and square added
```
- # Отчёт о тестах
- Цели и задачи тестов:
Определить работоспособность программы, найти ошибки, исправить их
- Тестируемый продукт:
Библиотека программ, вычисляющих геометрические величины разлчичных фигур
- Область тестирования: 
Все функции и программы библиотеки
- Стратегия тестирования:
Подстановка различных значений, натуральных и целых. Функциональное тестирование
- Критерии приёмки:
Правильность выводимых значений функций
- Ожидаемые результаты:
Статусы тестирования
- # Тесты
```
class RectangleTestCase(unittest.TestCase):
    def test1(self):
        self.assertEqual(area(0, 0), 0);
        self.assertEqual(perimeter(0, 0), 0);
    def test2(self):
        self.assertEqual(area(1, 1), 1);
        self.assertEqual(perimeter(1, 1), 4);
    def test3(self):
        self.assertEqual(area(100, 29), 2900);
        self.assertEqual(perimeter(100, 29), 258);

class TriangleTestCase(unittest.TestCase):
    def test1(self):
        self.assertEqual(area(0, 0), 0);
        self.assertEqual(perimeter(0, 0, 0), 0);
    def test2(self):
        self.assertEqual(area(1, 1), 0.5);
        self.assertEqual(perimeter(1, 1, 1), 3);
    def test3(self):
        self.assertEqual(area(100, 2), 100);
        self.assertEqual(perimeter(100, 100, 1), 201);

class SquareTestCase(unittest.TestCase):
    def test1(self):
        self.assertEqual(area(0), 0);
        self.assertEqual(perimeter(0), 0);
    def test2(self):
        self.assertEqual(area(1), 1);
        self.assertEqual(perimeter(1), 4);
    def test3(self):
        self.assertEqual(area(100), 10000);
        self.assertEqual(perimeter(100), 400);

class CircleTestCase(unittest.TestCase):
    def test1(self):
        self.assertEqual(area(0), 0);
        self.assertEqual(perimeter(0), 0);
    def test2(self):
        self.assertEqual(area(1), math.pi);
        self.assertEqual(perimeter(1), 2 * math.pi);
    def test3(self):
        self.assertEqual(area(1000), 1000000 * math.pi);
        self.assertEqual(perimeter(1000), 2000 * math.pi);
```
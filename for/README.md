## Цикл `for`  
#### Цикл `for` нужен, чтобы пройти по элементам списка
  
#### Пример прохода по списку:  
```python
for i in [10 * 5, 2, 3, 4, "Text"]:
    print(i)
```  
## Функция `range() позволяет идти от одного числа до другого. **Второе число не включается!**`  
#### Идем от 0 до 9:  
```python
for i in range(10):
    print(i)
```  
#### Рисуем правильный шестиугольник:  
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(1)

a = 60 #  угол

for i in range(6):
    t.forward(100)
    t.left(a)
```  

####  Идем от 6 до 1 с шагом -2  
```python
for i in range(6, 0, -2):
    print(i)

```  

####  Внутри циклов можно проверять условия с помощью `if/elif/else`  
```python


for i in [1, 2, 2, 1, 2, 1, 2, 1, 2]:
    if i == 1:
        print("Первый")
    else:
        print("Второй")
    
```

#### Оператор `continue()` делает переход на следующую итерацию цикла раньше времени  
```python
for i in [1, 1, 2, 1, 2, 2]:
    if i == 1:
        print("Первый")
        continue
    else:
        print("Второй")
    
    print("Шаг вперед!")
```

#### Оператор `break` нужен, чтобы закончить цикл раньше времени  
```python
N = int(input("Сколько яблок может съесть Петя?"))

while True:
    a = int(input())
    N = N - a
    if N >= 0:
        print("Петя съел", a, "яблок")
    else:
        break
        
```  

#### Рисуем рандомное число рандомных многоугольников  
```python
import turtle
import random
t = turtle.Turtle()
t.speed(10)
# Свой код пишите ниже

a = random.randint(4, 20)  #  число фигур
n = random.randint(3, 11)  # число сторон в фигуре

for k in range(a):
    for i in range(n):
        t.forward(50)
        t.left(360 / n)
    t.left(360 / a)

```

#### Найти индекс(порядковый номер) максимального числа из введенных  
```python
max_i = -1000000  # начальный максимум
max_id = 0  # номер максимума
i = 1  # номер текущего числа

while True:
    n = int(input())  # считываем число
    
    if n == 0: #  Если ввели 0
        break
    
    if n > max_i:
        max_i = n
        max_id = i
    
    i += 1
    

print(max_id)   
    
``
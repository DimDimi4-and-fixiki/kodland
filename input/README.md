### Типы данных в Python <img src="https://vk.com/emoji/e/f09f98bc.png" height="30px"/> <img src="https://vk.com/emoji/e/f09f98bc.png" height="30px"/> <img src="https://vk.com/emoji/e/f09f98bc.png" height="30px"/> :

- int (integer) - целые числа. **Пример: 243**
- float - числа с плавающей точкой. **Пример: 22.45**
- str (string) - строковый тип данных. **Пример: "Hello, world"**



Команда `input()` считывает строку, которую вводит пользователь. Она возвращает тип  **`str`**

## Задачки, которые разобрали на уроке <img src="https://vk.com/emoji/e/f09f98a8.png" height="30px"/><img src="https://vk.com/emoji/e/f09f98a8.png" height="30px"/><img src="https://vk.com/emoji/e/f09f98a8.png" height="30px"/>

#### 1. Привести число из `float` в `int` 

**Код:**

```python
N = 56.78  # int или float?

b = int(N)  # 56,  приводит число N к типу int
print(b)
```

#### 2. Привести строку к типу float

**Код:**

```python
stroka = "12.34"  # str
print(type(stroka))

res = float(stroka)  # float
print(res)
print(type(res))

```

#### 3. Вывести на экран иформацию о себе

**Код:**

```python
Name = "Дима" # str, имя 
Surname = "Калинин" # str, имя
Age = 19  # int, возраст

print("Меня зовут", Name, "и мне", Age, "лет")
```



#### 4. Считать стороны прямоугольника и вывести периметр и площадь

**Код:**

```python
a = float(input())  # float, считываем сторону
b = float(input())  # float, считываем вторую сторону

s = a * b  # считаем площадь
p = (a + b) * 2  # считаем периметр

print(s)
print(p)
```



#### 5. Посчитать площадь круга, пользователь вводит радиус

**Код:**

```python
r = float(input())  # пользователь вводит радиус
p = 3.14  #float, число пи
s = p * (r ** 2)  # считаем площадь
print(s)
```



#### 6. Нужно выводить условия загадок, считывать ответ пользователя и выводить правильные ответы

**Код:**

```python
a = input("Кто под проливным дождем не намочит волосы?")  # первая загадка
print("Лысый")  # правильный ответ
b = input("Как называется боязнь прихода Санта-Клауса?")  # вторая загадка
print("Клаустрофобия")  # правильный ответ
c = input("Как называют корову, которая не даёт молока?")  # третья загадка
print("Жадина-говядина")  # правильный ответ
```




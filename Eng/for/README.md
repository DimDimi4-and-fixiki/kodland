## `for` loop
#### with a `for` loop you can easily loop through the collection  
```python
for elem in [3, "Dima", "Nicole", 10]:
    print(elem)
```

#### The good thing about the `for` loop is that you know how many steps it is going to be  
#### You can draw the rectangle with the `for` loop:  
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed()

for i in [1, 4, 2, 50]: # 4 elements
    t.forward(50)
    t.left(90)
```  
#### The `range()` function gives you a sequence of numbers.   
#### For example, `range(10) will give you 0, 1, ... , 9`  
#### And `range(1, 5)` will give you 1, 2, ..., 4  
#### Let's draw a hexagon using `range()`  
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(1)

for i in range(6):
    t.forward(50)
    t.left(60)

```  
#### You can specify the `step` that you will go with in your `range()` function  
```python
for i in range(10, 1, -2):  # step is -2
    print(i)
```  
#### Countdown with a `for` loop:
```python
import time

num = int(input("Enter the number"))

for i in range(num, 0, -1):
    print(i, "...")
    time.sleep(1)

print("Let's go")
```  

#### Drawing a snowflake with a `for` loop:  
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(2)
for i in range(6):
    t.forward(100)
    t.backward(40)
    t.left(45)
    t.forward(40)
    t.backward(40)
    t.right(90)
    t.forward(40)
    t.backward(40)
    t.left(45)
    t.backward(60)
    t.left(60)
```  
#### Counting from `a` to `b` with a `range()` function:  
```python
a = int(input())
b = int(input())

if a < b:
    for i in range(a, b + 1):
        print(i)
else:
    for i in range(a, b - 1, -1):
        print(i)
```

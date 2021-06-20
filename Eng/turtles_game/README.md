## Turtles racing game  
**Firstly, we need to draw the field for the game**  
**We will do it by drawing lines with a `turtle`**  
```python
from turtle import *
from random import *

t = Turtle()

t.up()
t.goto(-100, 100)
t.down()

t.speed(8)

for i in range(15):
    t.write(i)
    t.right(90)
    t.forward(200)
    t.backward(200)
    t.left(90)
    t.forward(20)

```

**After the field, we are ready to make a competitors**  
```python
from turtle import *
from random import *

t = Turtle()

t.up()
t.goto(-100, 100)
t.down()

t.speed(20)

for i in range(15):
    t.write(i)
    t.right(90)
    t.forward(200)
    t.backward(200)
    t.left(90)
    t.forward(20)


first = Turtle()
first.shape("turtle")
first.color("green")

second = Turtle()
second.shape("turtle")
second.color("blue")

third = Turtle()
third.shape("turtle")
third.color("red")

first.up()
second.up()
third.up()

first.goto(-120, 70)
second.goto(-120, 40)
third.goto(-120, 10)

first.down()
second.down()
third.down()

```  
**`Let them fight!`, we will use the `while` loop to move turtles multiple times**  
```python
from turtle import *
from random import *

t = Turtle()

t.up()
t.goto(-100, 100)
t.down()

t.speed(100)

for i in range(15):
    t.write(i)
    t.right(90)
    t.forward(200)
    t.backward(200)
    t.left(90)
    t.forward(20)


first = Turtle()
first.shape("turtle")
first.color("green")

second = Turtle()
second.shape("turtle")
second.color("blue")

third = Turtle()
third.shape("turtle")
third.color("red")

first.up()
second.up()
third.up()

first.goto(-120, 70)
second.goto(-120, 40)
third.goto(-120, 10)

first.down()
second.down()
third.down()


x_first = 0
x_second = 0
x_third = 0

prediction = input("Who is going to be the winner?")
text = Turtle()
text.up()
text.goto(-120, -120)
text.write("Your prediction is: " + prediction, font = ("Arial", 12, "bold"))

while x_first < 305 and x_second < 305 and x_third < 305:

    first_step = randint(1, 5)
    second_step = randint(1, 5)
    third_step = randint(1, 5)
    
    first.forward(first_step)
    second.forward(second_step)
    third.forward(third_step)

    x_first += first_step
    x_second += second_step
    x_third += third_step

```  


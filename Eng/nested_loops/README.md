## Nested Loops  
### `Nested loops` are basically one loop inside of others  
**Example of the `nested loops`**  
```python
for i in range(1, 4):  # 1, 2, 3
    for j in range(1, 3):  # 1, 2
        print("i=", i, "j=", j)
```  

###  Drawing squares with `nested loops`  
```python

import turtle

t = turtle.Turtle()
side = 100


for j in range(3):  # loop for 3 squares
    for i in range(4):  # drawing one square
        t.forward(side)
        t.left(90)
    t.forward(side)
    t.up()  # making spaces between the squares
    t.forward(20)
    t.down()
```  

### We can use variables inside of the `range()` function  
```python
num = int(input("How many stars do you want on the screen?"))


for i in range(num):
    print("*")
```  

### Drawing given number of squares  
```python
import turtle

t = turtle.Turtle()

num = int(input("Input the number of squares"))
for j in range(num):  # many squares
    for i in range(4):  # drawing one square
        t.forward(100)
        t.left(90)
    
    t.forward(100)
    t.up()  # making a space between squares
    t.forward(20)
    t.down()
```  
### Drawing rotated squares  
```python
import turtle

t = turtle.Turtle()


for j in range(12):
    for i in range(4):  # one square
        t.forward(100)
        t.left(90)
    t.left(30)  # rotating the next square

```
  
### Game about the `doors`  
```python
import random

N = 1  # number of tries

print("there are two doors in front of you, which one will you open?")
print("1) Left")
print("2) Right")
door = int(input())
goodDoor = random.randint(1, 2)

if door == goodDoor:
    print("There are two more doors, 1) and 2)")
    door = int(input())
    goodDoor = random.randint(1, 2)
    if door == goodDoor:
        print("Cool, you have got the treasures")
    else:
        print("Not this time(")
else:
    print("You haven't guessed :(")
    N -= 1
    
```  



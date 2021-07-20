# Tasks on `functions` topic  
### 1. Check if text is a palindrome  
Let's check if reversed line is the same as the usual one and return the value depending on it  
We need to use `text = text.lower()` to make it lowercase  
Use `text = text.replace(" ", "")` to remove all the spaces  
  

```python
def check_text(line):
    reversed_line = line[::-1]
    # If reversed is the same as usual
    if reversed_line == line:
        return 1
    else:
        return 0

# Firstly, we need to input it
text = input("Type some text")
# Makes it lowercase
text = text.lower()
# Removes the spaces
text = text.replace(" ", "")
check = check_text(text)
if check == 1:
    print("It is a palindrome")
else:
    print("No, it is not a palindrome")
```  
### 2. Make a list and find sum, maximum and average values  
We will use a `for` loop here to loop through all the elements
You need to update the `sum` and `max`  
To count the `mean` we will just do `sum / number of elements`
```python
l = [11, 7, 18, 9, 20, 15, 73, 41, 9]
sum = 0
max_num = 0
max = 0
cur_num = 1
for element in l:
    sum += element
    if element > max:
        max = element
        max_num = cur_num

    cur_num += 1
mean = sum / len(l)
print(max_num,sum, mean)
```  
### 3. Random shape with the `turtle`  
Firstly, we will draw the random shape and collect all the points 
Then we will go through them and find the maximum  

```python
from turtle import *
from random import randint

t = Turtle()
xCords = []
yCords = []
t.penup()
t.goto(-100,0)
t.pendown()
for i in range(0,10):
    t.forward(randint(20,50))
    t.left(randint(-60,60))
    xCords.append(t.position()[0])
    yCords.append(t.position()[1])

# Going through all the cordinates
maxnum = 0
maxpos = yCords[0]
for i in range(0,10):
    if yCords[i] > maxpos:
        maxpos = yCords[i]
        maxnum = i
# Print all the cordinates with input, cause we cannot use print here :(
input(yCords)
input(maxpos)
input(i+1)
```  
### 4. Draw ammos with the `turtle`  
We will use the `for` loop here
```python
from turtle import *

def drawAmmo(n):
    for i in range(n):
        t.forward(10)
        t.left(90)
        t.forward(60)
        t.left(90)
        t.forward(10)
        t.left(90)
        t.forward(60)
        t.left(90)
        t.penup()
        t.forward(13)
        t.pendown()

n = 6
t = Turtle()
drawAmmo(n)
```  
## 5. Check if it is a leap year 
We will just use the creteria from the assignment  

```python
def leap(year):
    if year % 4 == 0:
        if year % 100 == 0 and year % 400 != 0:
            return 0
        else:
            return 1
    else:
        return 0
        
year = int(input("Enter the year"))
if leap(year) == 1:
    print("it is a leap year")
else:
    print("the year is not a leap year")
```  
### 6. Assignment with time for work  
You need to use `slice` ([1:3], for example) to get minutes and hours from the line  

```python
def minutesOnWork(start,end):
    startMinutes = int(start[0:2])*60 + int(start[3:5])
    endMinutes = int(end[0:2])*60 + int(end[3:5])
    return endMinutes - startMinutes

start = input("What time did you arrive")
end = input("What time did you leave")
print(minutesOnWork(start,end))
```
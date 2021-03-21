## Data Types in Python 

#### There are 3 types we will use: `str`, which is a text, `int`, which is integer and `float `, which is a decimal number

#### To get the type of the variable we can use `type()`

#### Let's see how we can convert the types:

```python
a = 24  # This is int 
b = float(a)  # Converts int to float

print(a)  # Prints a
print(b)  # Prints b

c = 38.0  # Float type
d = int(c)  # Converts Float to Int

print(c)  # Prints c
print(d)  # Prints d

e = 54.99  # Float type
f = int(e)  # Converts Float to int

print(e)  # Prints e
print(f)  # Prints f

a = "44.2"  # Str type
b = 44.2  # Float type

print(type(a))  # Prints type of a
print(type(b))  # Prints type of b
```



#### Assignment 1. Convert `float` number to `int`:

```python
N = 56.78
a = int(N)  # Converts float to int
print(a)  # Prints out the result
```



#### Assignment 2. Convert `str` to `float`

```python
string = "12.34"  # Str type
a = float(string)  # Converts str to float
print(a)  # Prints out the result
```

#### Print the message with your `name` and your `age`:

```python
Name = "Dima"  # My name
Surname = "Black"  # Surname
Age = 19  # My age
print("My name is", Name, "I am", Age, "years old")
```

#### `input()` waits for the user to input some data

#### `input()`gives you `str` type !!!

#### Example of `input()`

```python
someName = input()  # Waits for the user to input
print(someName)  # Prints the result
someName = input ("Enter your name: ")  # Waits for the user to input
print(someName)  # Prints the result
fahrenheit = float(input())  # Waits for the user to input and converts input to float
print(fahrenheit)  # Prints the number
```



#### Assignment with `input()`

#### The type of the data which is got by `input()` is `str`



```python
answer = input()  # User inputs Data
print(type(answer))  # Prints type of the variable
```

### Hints on home task

#### 1. In the first assignment you do everything like in the previous home task, but you need to modify the `print()` to print out the message and then the result

```python
print("The travel time in hours:", distance / speed)
```

#### 2. We need to read the number that user enters and to print out the next number to this and the previous one

##### To read the number use `num = float(input())`

##### Then the next number will be `num + 1` and the previous one is `num - 1` and you just need to print them using `print()`




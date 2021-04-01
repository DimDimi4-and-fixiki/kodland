### Home Task 3

#### 1. First Assignment. Given a distance and speed, count time and print it in the following format: `The travel time in hours: XX`

**Firstly, we need to count time, so we do**:

```python
distance = 200  # Our distance
speed = 80  # Our speed
t = distance / speed  # time of the journey
```

**Then, we need to print the result in the needed format, this could be done using `print()` function**:

```python
print("The travel time in hours:", t) #  Prints result in the beatiful format
```

#### 2. Second Assignment. Given a number, print the next number and the previous one.

**Firstly, let's read the number using `input()` function. Our number could be `integer` or `float` , so it is better to use `float` type. Let's call the variable where we will store the number `num`. So, the next number would be equal to `num + 1` and the previous one would be equal to `num - 1`. Then we need to print out all the results using `print()` function**

```python
num = float(input())  # Reads the number from the user

next = num + 1  # Next number
previous = num - 1  # Previous number

print("The next number for", num, "is", next)  # Prints next
print("The preceiding number for", num, "is", previous)  # Prints previous
```

#### 3. Last Assignment. Ask user how much money he has, and print the sum of all money.

**For asking user it is a good idea to use `input()`function**

**So we go with:**

```python
cent50 = int(input("How many 50-cent coins do you have?"))  # asks 50 cents
cent25 = int(input("How many 25-cent coins do you have?"))  # asks 25 cents
cent10 = int(input("How many 10-cent coins do you have?"))  # asks 10 cents
cent5 = int(input("How many 5-cent coins do you have?"))  # asks 5 cents

result = cent50 * 50 + cent25 * 25 + cent10 * 10 + cent5 * 5
print("In total, you have", result, "cents")  # Prints the result
```


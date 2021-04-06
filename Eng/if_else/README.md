#### `if`, `elif`, `else` operations

<img src="img_assets/if_else.png"/>

#### Assignments that were on the lesson:
**1. Ask user some questions about the weather**  
**Print what to wear depending on the user's answers**  
**Code:**  
```python
cold = input("Is it cold outside?")
rain = input("Is it raining outside?")
hot = input("Is it hot outside?")

if cold == 'Yes':
    print('Wear a warm hat')
if rain == 'Yes':
    print('Take an umbrella with you')
if hot == 'Yes':
    print('Wear a cap')
    
# your code here

num = int(input("Input number"))
if num > 10:
    print("Your number is more then 10")

if num < 5:
    print("It is a small number")

if num != 20:
    print("Your number is not 20")

```

#### `if` operator with `<=` and `>=`:
```python
answer = 1  # a number

if 5 <= answer <= 10:
    print("You have no more than 5 and no less than 10!")
else:
    print("You are not in the range from 5 to 10.")
```

#### 3. Ask user to input a color and print whether he can cross the road or not  
**Code:**  
```python
color = input("Input the color")

if color == "Red":
    print("You can't cross the road now")

if color == "Orange":
    print("Wait for the green color")

if color == "Green":
    print("Cross now")

```  
#### 4. Conditions with `elif` (else if)  
**Code:**  
```python
cold = input("Is it cold outside?")
rain = input("Is it raining outside?")
hot = input("Is it hot outside?")

if cold == "Yes":
    print("Wear a warm hat")
elif rain == "Yes":
    print("Take an umbrella with you")
elif hot == "Yes":
    print("Wear a cap")

```  
#### 5. User inputs a letter. If the letter is `Q`, print it. If it is `q`, print it, else print that user entered something different  
**Code:**  
```python
letter = input("Input the letter")

if letter == "Q":
    print("Your letter is Q")
elif letter == "q":
    print("Your letter is q")
else:
    print("The user entered something else")
    
```  
#### 6. Ask a user about how many hours he sleeps and print if it is enough or not  
**Code:**  
```python
number = int(input("Enter how many hours you sleep"))


if number > 10:
    print("Too much")
elif 7 < number <= 10:
    print("This is normal")
else:
    print("It is not enough")
```  

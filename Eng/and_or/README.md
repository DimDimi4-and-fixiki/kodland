### `and`,  `or` and `not` in python conditions

#### Assignment about the computer

```python


print("What is the average frequency of your CPU core?")
processor = float(input())  # reads frequency
print("do you have a GeForce GTX 1050 or older video card?")
videocard = input()  # reads answer about videocard
if processor >= 1.5 and videocard == "Yes":
    print("Computer meets requirements")
else:
    print("Computer does not meet the requirements")
```



#### Hogwarts

```python
# your code here

wizard = input("Are you a wizard?")  # Answer about the wizard
age = int(input("What is your age?"))  # type is integer

if wizard == "Yes" and 11 < age < 17:  # if wizzard and between 11 and 17
    print("You are accepted")
else:
    print("You are not accepted")
```

#### Check if person sleeps normally

```python
dream = int(input("How much do you usually sleep?"))  # reads number

if dream < 7 or dream > 9:  # if less than 7 or more than 9
    print("you have trouble sleeping")
else:
    print("you have a normal sleep")
```

#### You can attend the performance if you have a ticket `or` if you are under 7

```python
# your code here

age = int(input("How old are you?"))  # reads age
ticket = input("Do you have a ticket?")  # reads answer about the ticket

if age < 7 or ticket == "yes":
    print("You can attend the performance")
else:
    print("First buy the ticket")
```

#### `not` inverts your condition. So if it was `True` , it is becoming `False` and backwards

```python
age = 5

if not (7 <= age <= 10):  # checks if age is not between 7 and 10
    print("Age is not between 7 and 10")
```

#### There is a list of user names that should not be accepted to enter the server

```python
# your code here

username = input("Input your username")  # reads the username

if username == "Honest_Player" or username == "OffCrocodile" or username == "Pro100John":
    print("You are banned")
else:
    print("Everything is fine")
```

#### Ask user about his age, name and experience. If user is older than 16 and has more than 2 years of experience, he is accepted. If user's name is Kidus, he is also accepted.

```python
# your code here

age = int(input("Input your age"))
name = input("Your name")
exp = int(input("Years of experience"))

if 16 < age and exp > 2 or name == "Kidus":  # age more 16 and exp more 2 or name is Kidus
    print("You are accepted")
```


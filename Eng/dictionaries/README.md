## Dictionaries in `Python`  
**In Python, a `dictionary` binds two elements to each other. In this case, the elements are called key and value. Each element or entry in the dictionary has a key and a value.**  
**Example of dictionaries in `Python`**  
```python
age = {}  # empty dictionary

age["Lucas"] = 10
age["Emine"] = 9
print(age)

age2 = {"Dima": 19, "Emine": 9}
print(age2)
print(age2["Dima"])
print(age2["Emine"])
```  
**Dictionary with food in Eng and French. `You have to do something similar in a HW1 assignment`**  
```python
food = {}

for i in range(3):
    eng_food = input()
    french_food = input()
    food[eng_food] = french_food

print(food)
```  
**You can use `d.keys()` to get a `list with all keys` and `d.values()` to `get all the values`**  
```python
phoneNumbers = {}
phoneNumbers["John"] = "555-1234"
phoneNumbers["Mary"] = "555-6789"
phoneNumbers["Bob"] = "444-4321" 
phoneNumbers["Jenny"] = "867-5309"
print(phoneNumbers)

print(phoneNumbers.keys())
print(phoneNumbers.values())
print(sorted(phoneNumbers.keys()))

del phoneNumbers["Bob"]
print(phoneNumbers)

if "Mary" in phoneNumbers:
    print("We have Mary")

phoneNumbers.clear()
print(phoneNumbers)
```  

**With `d.keys()` we can get all contacts which start with a specific letter**  
```python
phoneNumbers = {}
phoneNumbers["John"] = "555-1234"
phoneNumbers["Mary"] = "555-6789"
phoneNumbers["Bob"] = "444-4321" 
phoneNumbers["Jenny"] = "867-5309"
print(phoneNumbers)

letter = input('Which letter should you display contacts?') 

names = phoneNumbers.keys()
print(names)

for name in names:
    if name[0] == letter:  # Checks that starts with a letter
        print(name, phoneNumbers[name])
```  
**We can use `in` to check if element is in the dictionary**  
```python
phoneNumbers = {}
phoneNumbers["John"] = "555-1234"
phoneNumbers["Mary"] = "555-6789"
phoneNumbers["Bob"] = "444-4321" 
phoneNumbers["Jenny"] = "867-5309"
print(phoneNumbers)

name = input("Input the name")

if name in phoneNumbers:
    del phoneNumbers[name]

print(phoneNumbers)
```
**Duel game :)**  
```python
import time
import random

hero1 = {"Health": 100, "Attack": 3}
hero2 = {"Health": 60, "Attack": 6}


turn = 1

while hero1["Health"] > 0 and hero2["Health"] > 0:
    if turn % 2 == 1:  # Turn of hero 1
        print("Hero1 hits Hero2")
        num = random.randint(1, 4)
        print("Attack is", hero1["Attack"] + num)
        hero2["Health"] -= hero1["Attack"] + num
    else:
        print("Hero2 hits Hero1")
        num = random.randint(1, 2)
        print("Attack is", hero2["Attack"] + num)
        hero1["Health"] -= hero2["Attack"] + num
    
    print("Hero1 has", hero1["Health"])
    print("Hero2 has", hero2["Health"])
    turn = turn + 1
    time.sleep(2)
```  
### Comments for the home task :)  
**Home task 1**  
Please, use something like in assignment with a food  
**This is just an example for you. Please, fill the dictionary with some more countries**  
```python
dict = {'China' : 1395380000, 'Russia' : 146781095, 'France' : 67348000}

x = input()
y = int(input())

dict[x] = y

print(sorted(dict.values(), reverse = True))
```  
**Second Task**  
Please, at the code with duel above and put it inside the `for loop`, also count the points for each player :)

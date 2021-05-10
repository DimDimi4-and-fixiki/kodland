## ` While ` loop



### We need a `while` loop to repeat the code till the condition is satisfied, so it is also called a `conditional loop`

#### Example of a simple `while` loop

```python
str = ""
while (str != "yes"):  # str not equals yes
    print("Loop works")
    str = input("Want to exit the loop?")
print("loop completed")
```

  

#### Assignment with the poem

```python
monkeys = 5

while monkeys > 0:  # while you have some monkeys
    print(monkeys, """little monkeys were jumping on the bed
    One fell off and banged his head The mommy called the doctor And the doctor said No more monkeys jumping on the bed.
    """)
    monkeys = monkeys - 1  # substract a 1 monkey
```

#### `random.randint(a, b)` gives you a random integer number from `a` to `b`

#### Example with rolling a dice

```python
import random

num = random.randint(1, 6)

print("You rolled", num)

if num == 5 or num == 6:
    print("You have run away from a monster!")
else:
    print("Not this time, the monster has got you.")
```

#### Rolling a dice till we have got 5 or 6 on it

```python
import random

num = 0

while num != 5 and num != 6:
    num = random.randint(1, 6)
    print("You got", num)
```

#### `time.sleep()` just makes your program wait for a number of seconds

```python
import time

print("Here comes on the stage...")
time.sleep(5)  # Waits for 5 seconds
print("the Great wizard Magus!")
```



#### The assignment about dragons and caves

```python
import time
import random

print("You have 2 caves to go. In one, there is a friendly dragon, in the other one, you will find a hungry dragon")
time.sleep(1)
num = int(input("Choose the cave, 1 or 2"))
time.sleep(2)
friendly_cave = random.randint(1, 2)
if num == friendly_cave:  # User guessed a good cave
    print("You are safe :)")
else:
    print("You were eaten :(")
```

#### The additional task, `please, use float here`

```python
num = float(input())
end_num = float(input())

res = 0

while num <= end_num: # while we don't reach the end num
    num = num * 1.1
    res = res + 1

print(res)
```


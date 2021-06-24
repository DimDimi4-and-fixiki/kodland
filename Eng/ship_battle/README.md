## Shipbattle game  

**Firstly, we will draw the field**  

```python
from random import randint 

board = []
 
for x in range(4): 
    board.append(["O"] * 4) 

```

**Then we will pick the cordinates for the ship**  
```python
ship_row = randint(0, len(board) - 1) 
ship_col = randint(0, len(board[0]) - 1) 
```  

**Let's ask the player to input the level of difficulty**  
```python
print('1) Easy: 12 attempts') 
print('2) Average: 8 attempts') 
print('3) Difficult: 4 attempts') 
print('4) Impossible: 2 attempts') 
level = int(input('Choose the difficulty level')) 

attempts = 10 
if level == 1: 
    attempts = 12 
elif level == 2: 
    attempts = 8 
elif level == 3: 
    attempts = 4 
elif level == 4: 
    attempts = 2
```

**Then we will print out the field beautifully**  
```python
print("Let's start the game")
for row in board:
    print((" ").join(row))
```  

**Now we are ready to play the game**  
```python
for turn in range(1, 11):
    print("Turn:", turn)
    user_row = int(input("Input the row: 0 - 5"))
    user_column = int(input("Input the column: 0 - 4"))
    
    if user_row == row_number and column_number == user_column:
        print("well done, you have won!!!")
        break
    else:
        print("You missed, try again")
        board[user_row][user_column] = "X"
        for row in board:
            print(("   ").join(row))
```

### Modification. Add 2 more ships  
**To do it we need to modify the line where we generate the ship, so instead of:**
```python
ship_row = randint(0, len(board) - 1) 
ship_col = randint(0, len(board[0]) - 1) 
```  
**We will go with**
```python
    
ships = []  # a list for ships

for i in range(0, 3):
    ship_row = randint(0, len(board) - 1)
    ship_col = randint(0, len(board[0]) - 1)
    ships.append([ship_row, ship_col])
```  
**And in the `for loop` we will add this:**
```python
hit = 0
    for i in range(0, len(ships)):
        if(ships[i] == [guess_row, guess_col]):
            hit = 1
            del ships[i]
            board[guess_row][guess_col] = "S"
            break
        
    if hit > 0:
        print("You guessed the ship")
        if len(ships) == 0:
            print('Congrats')
```  
**So the `for loop` would look like**  
```python
for turn in range(attempts):
    print ("Turn: ", turn)
    guess_row = int(input("Row 0-3:"))
    guess_col = int(input("Columns 0-3:"))
    
    hit = 0
    for i in range(0, len(ships)):
        if(ships[i] == [guess_row, guess_col]):
            hit = 1
            del ships[i]
            board[guess_row][guess_col] = "S"
            break
        
    if hit > 0:
        print("Well done, you guessed")
        if len(ships) == 0:
            print('Yoooouu won!')
    else:
        if (guess_row < 0 or guess_row > len(board)) or (guess_col < 0 or guess_col > len(board)):
            print("Oops, enter the right numbers")
        elif(board[guess_row][guess_col] == "X"):
            print("You have tried these numbers before(")
        else:
            print("Miss")
            board[guess_row][guess_col] = "X"
        
    for row in board:
        print((" ").join(row))
    
    if turn == attempts - 1:
        print("Game ended")
```
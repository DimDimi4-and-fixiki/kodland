## Rock Paper and Scissors Game

### Code of the Game

```python
import random
import time

ourScore = 0  # Player's score
computerScore = 0  # Computer's score

while computerScore < 3 and ourScore < 3:  # While there is no winner

    yourChoice = input("Input rock, paper or scissors")  # Random number
    
    computerChoice = random.randint(1, 3)
    if computerChoice == 1:
        computerChoice = "rock"
    
    if computerChoice == 2:
        computerChoice = "paper"
    
    if computerChoice == 3:
        computerChoice = "scissors"
    
    
    
    
    if yourChoice == "paper" or yourChoice == "scissors" or yourChoice == "rock":
        print("Computer choice is", computerChoice)
        if (yourChoice == "paper" and computerChoice == "rock") or (yourChoice == "rock" and computerChoice == "scissors") or (yourChoice == "scissors" and computerChoice == "paper"):  # Player wins
            ourScore += 1  # Update our score
        elif yourChoice == computerChoice:  # Draw
            ourScore += 1
            computerScore += 1
        else:  # Computer wins
            computerScore += 1
        
        print("Player's score:", ourScore, "Computer's score:", computerScore)
    else:
        print("You entered something wrong")
        
    
```
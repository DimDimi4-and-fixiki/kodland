### Игра камень-ножницы-бумага

#### Задание. Сделать игру камень-ножницы-бумага Игрок против Компьютера до `3` побед <img src="https://vk.com/emoji/e/e29c8cf09f8fbb.png" height="30px"/><img src="https://vk.com/emoji/e/e29c8bf09f8fbb.png" height="30px"/><img src="https://vk.com/emoji/e/e29c8af09f8fbb.png" height="30px"/>

#### Код с комментариями на Python:  <img src="https://vk.com/emoji/e/f09f988a.png" height="30px"/>

```python
import time
import random

yourScore = 0  # наше число очков
computerScore = 0  # число очков у компьютера

while yourScore != 3 or computerScore != 3:
    
    
    playerChoice = input("Выберите камень / ножницы / бумага")
    
    if playerChoice == "камень" or playerChoice == "ножницы" or playerChoice == "бумага":
        computerChoice = random.randint(1, 3)  # компьютер генерирует число
        # 1 - камень; 2 - ножницы; 3 - бумага
        if computerChoice == 1:
            computerChoice = "камень"
        elif computerChoice == 2:
            computerChoice = "ножницы"
        else:
            computerChoice = "бумага"
        
        time.sleep(1)
        print(1)
        time.sleep(1)
        print(2)
        time.sleep(1)
        print(3)
        time.sleep(1)
            
        print("Компьютер выкинул", computerChoice)
        
        
        if computerChoice == playerChoice:
            print("Ничья")
        elif computerChoice == "камень" and playerChoice == "бумага":
            print("Игрок победил")
            yourScore += 1
        elif playerChoice == "камень" and computerChoice == "ножницы":
            print("Игрок победил")
            yourScore += 1
        elif playerChoice == "ножницы" and computerChoice == "бумага":
            print("Игрок победил")
            yourScore += 1
        else:
            print("Победил компьютер")
            computerScore += 1
        
        
    else:
        print("Нужно было ввести камень / ножницы / бумагу")
    
    print("Текущий счет - Игрок:", yourScore, "Компьютер:", computerScore)
    

```




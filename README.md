# Snake-game-in-python.-first-project

import random

'''
1 for snake
-1 for water
0 for gun
'''

computer = random.choice([1, -1, 0])
youstr = input("Enter your choice: ")
youDict = {"s" : 1, "w": -1, "g" : 0 }
reverseDict = {1: "snake", -1: "water", 0: "gun"}

you = youDict[youstr]

# By now we have 2 numbers (variables), you and computer

print(f"you chose{reverseDict[you]}\ncomputer chose {reverseDict[computer]}")

if (computer == you):
    print("Game draw!")

else:
    if(computer == -1 and you == 1):
         print("You win!")

    elif(computer == -1 and you == 0):
        print("You lose!")

    elif(computer == 1 and you == -1):
        print("You lose!")    

    elif(computer == 1 and you == 0):
        print("You win")

    elif(computer == 0 and you == -1):
        print("you win") 

    elif(computer == 0 and you == 1):
        print("you lose!")

    else:
        print("something went wrong:")                    


     

# Guessing-Game
A game where the user has to guess the number that the computer has generated 

import random


rounds = int(input("how many rounds would you like to play?: "))
for i in range (1,rounds + 1):                   #inputs the number of rounds that player wants to play
    target_number = random.randrange(1,11) 
    print("Round",i) #prints the round with each loop
    for i in range(1,4):                          #player gets 3 tries in 1 game to guess the number
        guess = int(input("enter guess here: "))
        if guess > target_number:
            print("too high!")
        if guess < target_number:
            print("too low!")
        if guess == target_number:
            print("that's right!")
            break                                 #break ensures that if players gets answer before using up three tries, the loop will end 
    if guess > target_number or guess < target_number:
        print("game over!")                       #if player gets the answer wrong three times then prints game over 
    else:
        print("well done!")                       #else prints well done if players gets it right 


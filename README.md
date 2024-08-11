# guess-the-number-game
import random
import time

num = random.randint(1,100)
count = 1
print("A number is being generated! Please Wait.")
while(count < 20):
    print("#", end='')
    time.sleep(0.5)
    count+=1
print("\tDone!")

print("\nI have a Number for You. Can you Guess It?")
guess = 0
tries = 1
while(guess != num and tries <= 5):
    print("Enter your Guess....(1-100) : ", end='')
    guess = int(input())
    if guess < 0 or guess > 100:
        print("Invalid Guess! Try Again")
        
    else:
        if(guess < num):
            print("Your Guess is Too Smaller than the Number.Guess Again!")
        elif(guess > num):
            print("Your Guess is  Too Lerger than the Number.Guess Again!")
    tries +=1

    print("Ther Number was : ", num)

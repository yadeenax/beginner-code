# beginner-code
import random

def guess(x):
    random_number = random.randint(1, x)
    guess = 0  
    while guess != random_number:
        guess = int(input (f'Guess a number between 1 and {x}: '))
        if guess < random_number:
            print('sorry, guess again, too low. ')
        elif guess > random_number:
            print('sorry, guess again. too  high.')
        

    print(f'Great, you have guessed the number {random_number}')



#guess the number the user 
def computer_guess(x):
    low = 1
    high = x
    feedback = " "
    while feedback != "c" :
        if low != high:
            guess = random.randint(low, high)
        else: 
            guess = low
        guess =  random.randint(low, high)
        feedback = input(f'Is {guess} too high (H), too low (L), or correct (C)??  ').lower()
        if feedback == "h":
            high = guess - 1
        elif feedback == "l":
            low = guess + 1

    print(f"Great! The computer guessed your number, {guess}, correctly! ")



computer_guess(10)

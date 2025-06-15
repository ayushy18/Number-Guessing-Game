import random

def play_game():
    secret_number = random.randint(1, 100)
    guesses_taken = 0
    print("I am thinking of a number between 1 and 100.")

    while True:
        try:
            guess = int(input("Take a guess: "))
            guesses_taken += 1

            if guess < secret_number:
                print("Your guess is too low.")
            elif guess > secret_number:
                print("Your guess is too high.")
            else:
                print(f"Good job! You guessed my number in {guesses_taken} guesses!")
                break
        except ValueError:
            print("Invalid input. Please enter a whole number.")

play_game()


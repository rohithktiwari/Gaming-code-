# Gaming-code-
it is a gaming code 
import random

def play_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")
    
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    
    # Number of attempts the player has taken
    attempts = 0
    
    while True:
        # Ask the player for their guess
        guess = input("Enter your guess (or type 'quit' to exit): ")

        # Allow the player to quit the game
        if guess.lower() == 'quit':
            print(f"You quit the game. The number was {number_to_guess}.")
            break
             try:
            guess = int(guess)
        except ValueError:
            print("Invalid input. Please enter a valid number.")
            continue
        
        attempts += 1
        
        # Compare the guess with the actual number
        if guess < number_to_guess:
            print("Too low!")
        elif guess > number_to_guess:
            print("Too high!")
        else:
            print(f"Congratulations! You guessed the number in {attempts} attempts.")
            break

if __name__ == "__main__":
    play_game()

# Gameimport random

def guess_the_number():
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100. Can you guess it?")
    
    # Set the initial guess count
    guess_count = 0
    
    while True:
        # Prompt the user for a guess
        try:
            player_guess = int(input("Enter your guess: "))
            guess_count += 1
            
            if player_guess < number_to_guess:
                print("Too low! Try again.")
            elif player_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the right number {number_to_guess} in {guess_count} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")
        
# Start the game
guess_the_number()

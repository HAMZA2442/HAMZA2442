import random

def guess_the_number():
    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    
    # Initialize the number of attempts
    attempts = 0
    
    print("Welcome to the Guess the Number game!")
    
    while True:
        try:
            # Ask the player for their guess
            guess = int(input("Guess the number between 1 and 100: "))
            
            # Increment the number of attempts
            attempts += 1
            
            # Check if the guess is correct
            if guess == secret_number:
                print(f"Congratulations! You guessed the number {secret_number} in {attempts} attempts.")
                break
            elif guess < secret_number:
                print("Try a higher number.")
            else:
                print("Try a lower number.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

if __name__ == "__main__":
    guess_the_number()

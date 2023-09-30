import random

# Generate a random number between 1 and 100
secret_number = random.randint(1, 30)

# Set the number of attempts
max_attempts = 10
attempts_taken = 0

# Game loop
while attempts_taken < max_attempts:
    # Prompt the player for a guess
    guess = int(input("Guess the number between 1 and 30: "))
    
    # Increase the number of attempts
    attempts_taken += 1
    
    # Compare the guess with the secret number
    if guess == secret_number:
        print("Congratulations! You guessed the number correctly.")
        break
    elif guess < secret_number:
        print("น้อยไปไอควาย.")
    else:
        print("สูงไปไอควาย.")

# Check if the player ran out of attempts
if attempts_taken == max_attempts:
    print("Game over! You did not guess the number. The secret number was:", secret_number)


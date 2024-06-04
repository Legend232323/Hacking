# Game Code

import random

def play_game():
  # Game logic here
  print("Welcome to the game!")
  score = 0
  while True:
    # Generate a random number between 1 and 10
    num = random.randint(1, 10)
    # Ask the user to guess the number
    guess = input("Guess the number (or 'q' to quit): ")
    if guess.lower() == 'q':
      break
    try:
      guess = int(guess)
      if guess == num:
        print("Correct!")
        score += 1
      else:
        print("Sorry, try again!")
    except ValueError:
      print("Invalid input. Please enter a number!")
  print(f"Game over! Your score was {score}.")

if __name__ == "__main__":
  play_game()

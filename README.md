import random

def number_guessing_game():
  """A number guessing game where the user selects a range and tries to guess a random integer in the minimum number of guesses."""

  # Get the range from the user
  a = int(input("Enter the lower bound of the range: "))
  b = int(input("Enter the upper bound of the range: "))

  # Generate a random integer in the range
  random_number = random.randint(a, b)

  # Initialize the number of guesses
  number_of_guesses = 0

  # Start the game loop
  while True:

    # Get the user's guess
    guess = int(input("Guess a number between {} and {}: ".format(a, b)))

    # Check if the guess is correct
    if guess == random_number:
      print("Congratulations! You guessed the correct number in {} guesses.".format(number_of_guesses))
      break

    # Give the user a hint if the guess is wrong
    elif guess > random_number:
      # Hint: the number is even
      if random_number % 2 == 0:
        print("Try again! The number is even.")
      # Hint: the number is divisible by a certain number
      elif random_number % 4 == 0:
        print("Try again! The number is odd.")
      # Hint: the number is a multiple of a certain number
      elif random_number % 3 == 0:
        print("Try again! The number is a multiple of 3.")
      else:
        print("Try again! You guessed too low.")
      number_of_guesses += 1

    # If the user has used up all of their guesses, end the game
    if number_of_guesses == 5:
      print("Better luck next time!")
      break

if __name__ == "__main__":
  number_guessing_game()        print("Try again! The number is divisible by 4.")
      else:
        print("Try again! You guessed too high.")
      number_of_guesses += 1
    elif guess < random_number:
      # Hint: the number is odd
      if random_number % 2 == 1:



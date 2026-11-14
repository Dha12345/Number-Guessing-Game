import random  # Built into Python; no installation needed


def get_guess():
    """Ask the user for a valid number."""
    while True:
        user_input = input("Enter your guess (1-100): ")

        try:
            guess = int(user_input)
        except ValueError:
            print("Please enter a whole number.")
            continue

        if guess < 1 or guess > 100:
            print("Your guess must be between 1 and 100.")
            continue

        return guess


def play_game():
    # A new secret number is created every time this function starts.
    secret_number = random.randint(1, 100)
    attempts = 0
    max_attempts = 7

    print("\nWelcome to the Number Guessing Game!")
    print("I am thinking of a new number between 1 and 100.")
    print(f"You have {max_attempts} attempts.\n")

    while attempts < max_attempts:
        guess = get_guess()
        attempts += 1

        if guess == secret_number:
            print(f"\nCorrect! You guessed it in {attempts} attempt(s).")
            return

        if guess < secret_number:
            print("Too low! Try again.")
        else:
            print("Too high! Try again.")

        remaining = max_attempts - attempts
        print(f"Attempts left: {remaining}\n")

    print(f"\nGame over! The secret number was {secret_number}.")


def main():
    while True:
        play_game()

        again = input("\nDo you want to play again? (yes/no): ").lower()
        if again != "yes":
            print("Thanks for playing!")
            break


main()

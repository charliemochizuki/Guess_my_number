import random


def game():
    guess_chances = 8
    num = random.randint(1, 100)
    while True:
        print(f"\nYou have {guess_chances} chances to play")
        guess = int(input("Guess a number between 1 - 100: "))
        guess_chances -= 1

        if guess > num:
            print(f"{guess} is too high")
        elif guess < num:
            print(f"{guess} is too low")
        else:
            print(f"You win. You got it.  and you still have {guess_chances} chance left")
            if input("\n\nDo you want to play again? Tap [ENTER] to play, or [*] to exit: ") != "*":
                game()
            input("\n\n\nGOOD BYE!\n\n\n")
            break

        if guess_chances == 0:
            print(f"You lost. You have {guess_chances} chance left")
            print(f"The answer is {num}")
            if input("\n\nDo you want to play again? Tap [ENTER] to play, or [*] to exit: ") != "*":
                game()
            input("\n\n\nGOOD BYE!\n\n\n")
            break


if input("Tap [ENTER] to Play, or tap [*] to Exit: ") != "*":
    game()
else:
    input("\n\n\nGOOD Bye!\n\n\n\n\n")

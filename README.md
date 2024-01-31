import time
import random

def introduction():
    print("Welcome to the Horror Game!")
    time.sleep(1)
    print("You find yourself in a dark, abandoned mansion.")
    time.sleep(1)
    print("Your objective is to escape without encountering any ghosts.")
    time.sleep(1)
    print("Choose your path carefully!")

def choose_path():
    print("\n1. Go through the creaky door.")
    print("2. Descend into the spooky basement.")
    print("3. Climb the eerie staircase.")
    return input("Choose your path (1, 2, or 3): ")

def ghost_encounter():
    print("\nA ghost appears and sends a chill down your spine!")
    time.sleep(1)
    print("You've encountered a ghost. Game over!")
    exit()

def escape():
    print("\nCongratulations! You successfully escaped the haunted mansion.")

def horror_game():
    introduction()

    for _ in range(3):  # Allow the player three choices
        choice = choose_path()

        if choice == '1':
            print("\nYou cautiously open the creaky door.")
            if random.choice([True, False]):  # 50% chance of encountering a ghost
                ghost_encounter()
            else:
                print("The room is empty. You continue your journey.")

        elif choice == '2':
            print("\nYou decide to descend into the spooky basement.")
            if random.choice([True, False]):  # 50% chance of encountering a ghost
                ghost_encounter()
            else:
                print("You find a hidden passage. You continue your journey.")

        elif choice == '3':
            print("\nYou climb the eerie staircase.")
            if random.choice([True, False]):  # 50% chance of encountering a ghost
                ghost_encounter()
            else:
                print("You discover a secret exit. You continue your journey.")

        else:
            print("Invalid choice. Please choose 1, 2, or 3.")

    escape()

if __name__ == "__main__":
    horror_game()

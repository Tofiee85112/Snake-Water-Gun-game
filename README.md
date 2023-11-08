import random

def get_user_choice():
    choices = ["Snake", "Water", "Gun"]
    print("Choose any from the given list:")
    print(choices)
    user_choice = input("Enter your choice: ").capitalize()
    return user_choice

def get_computer_choice():
    choices = ["Snake", "Water", "Gun"]
    computer_choice = random.choice(choices)
    return computer_choice

def game_logic(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "Tie"
    elif user_choice == "Snake":
        if computer_choice == "Gun":
            return "You Lose"
        else:
            return "You Win"
    elif user_choice == "Gun":
        if computer_choice == "Water":
            return "You Lose"
        else:
            return "You Win"
    elif user_choice == "Water":
        if computer_choice == "Snake":
            return "You Lose"
        else:
            return "You Win"
    else:
        return "Invalid Choice"

def play():
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    print(f"Your choice is {user_choice}")
    print(f"Computer choice is {computer_choice}")
    result = game_logic(user_choice, computer_choice)
    print(result)

play()

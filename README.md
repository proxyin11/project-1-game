 import random

# Function to determine the winner of the game
def gamewin(computer, person):
    # If both choose the same option, it's a tie
    if computer == person:
        return None
    
    # Computer chose Snake (s)
    elif computer == 's':
        if person == 'w':  # Person chose Water (w)
            return False  # Computer wins
        elif person == 'g':  # Person chose Gun (g)
            return True  # Person wins
    
    # Computer chose Water (w)
    elif computer == 'w':
        if person == 'g':  # Person chose Gun (g)
            return False  # Computer wins
        elif person == 's':  # Person chose Snake (s)
            return True  # Person wins
    
    # Computer chose Gun (g)
    elif computer == 'g':
        if person == 's':  # Person chose Snake (s)
            return False  # Computer wins
        elif person == 'w':  # Person chose Water (w)
            return True  # Person wins


# Main game logic
if __name__ == "__main__":
    # Computer's turn: Randomly select Snake (s), Water (w), or Gun (g)
    print("Computer's turn: Snake (s), Water (w), Gun (g)")
    random_number = random.randint(1, 3)
    if random_number == 1:
        computer = 's'  # Snake
    elif random_number == 2:
        computer = 'w'  # Water
    elif random_number == 3:
        computer = 'g'  # Gun

    # Person's turn: Input choice
    person = input("Your turn: Snake (s), Water (w), Gun (g): ").lower()

    # Determine the result of the game
    result = gamewin(computer, person)

    # Display choices
    print(f"Computer chose: {computer}")
    print(f"You chose: {person}")

    # Display the result
    if result == None:
        print("The game is a tie!")
    elif result:
        print("Congratulations! You win!")
    else:
        print("You lose! Better luck next time.")

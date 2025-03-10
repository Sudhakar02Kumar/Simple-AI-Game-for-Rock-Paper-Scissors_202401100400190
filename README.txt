# Rock-Paper-Scissors Game Report

## 1. Title Page

**Rock-Paper-Scissors Game**\
**Author:** Your Name\
**Date:** [Insert Date]

---

## 2. Introduction

This report details the implementation of a simple Rock-Paper-Scissors game using Python. The game allows the user to play against the computer, which makes random choices. The game runs in a loop until the player decides to exit by typing 'quit'.

---

## 3. Methodology

The program follows a structured approach:

1. The player inputs their choice (`rock`, `paper`, or `scissors`).
2. The computer randomly selects one of the three choices.
3. The program determines the winner based on standard Rock-Paper-Scissors rules:
   - Rock beats Scissors
   - Scissors beats Paper
   - Paper beats Rock
4. The result is displayed, and the user is prompted for the next round until they choose to exit.
5. The game ensures valid inputs and provides appropriate feedback.

---

## 4. Code Typed

```python
import random

# Function to randomly select the computer's move
def get_computer_choice():
    return random.choice(["rock", "paper", "scissors"])

# Function to determine the winner of the game
def determine_winner(player, computer):
    if player == computer:
        return "It's a tie!"
    elif (player == "rock" and computer == "scissors") or \
         (player == "scissors" and computer == "paper") or \
         (player == "paper" and computer == "rock"):
        return "You win!"
    else:
        return "Computer wins!"

# Main function to run the game
def main():
    print("Welcome to Rock-Paper-Scissors!")
    
    while True:
        player_choice = input("Enter rock, paper, or scissors (or 'quit' to exit): ").lower()
        
        if player_choice == "quit":
            print("Thanks for playing!")
            break
        
        if player_choice not in ["rock", "paper", "scissors"]:
            print("Invalid choice. Try again.")
            continue

        computer_choice = get_computer_choice()
        print(f"Computer chose: {computer_choice}")
        result = determine_winner(player_choice, computer_choice)
        print(result)
        print("-" * 30)

if __name__ == "__main__":
    main()
```

---

## 5. Screenshots Output

### Example Output:

```
Welcome to Rock-Paper-Scissors!
Enter rock, paper, or scissors (or 'quit' to exit): rock
Computer chose: scissors
You win!
------------------------------
Enter rock, paper, or scissors (or 'quit' to exit): paper
Computer chose: rock
You win!
------------------------------
Enter rock, paper, or scissors (or 'quit' to exit): quit
Thanks for playing!
```

&#x20;

---

## 6. Conclusion

This Rock-Paper-Scissors game demonstrates fundamental Python programming concepts such as user input handling, conditional statements, loops, and the use of the `random` module. The game is interactive, engaging, and allows users to play multiple rounds until they choose to exit.

---

## 7. References

No external references were used in this project. All code is original and created for educational purposes.


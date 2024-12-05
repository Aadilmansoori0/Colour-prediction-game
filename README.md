import random

def color_prediction_game():
    # List of possible colors
    colors = ['red', 'blue', 'green', 'yellow', 'orange', 'purple', 'pink', 'black', 'white']
    
    # Randomly select a color
    selected_color = random.choice(colors)
    
    print("Welcome to the Color Prediction Game!")
    print("I am thinking of a color from the following list:")
    print(', '.join(colors))
    
    # Set number of attempts
    attempts = 5
    
    while attempts > 0:
        guess = input(f"\nYou have {attempts} attempts left. What's your guess? ").lower()
        
        if guess == selected_color:
            print(f"Congratulations! You guessed the correct color: {selected_color}")
            break
        else:
            attempts -= 1
            print(f"Wrong guess. Try again!")
        
        if attempts == 0:
            print(f"Sorry, you're out of attempts. The correct color was {selected_color}. Better luck next time!")
            break

# Start the game
color_prediction_game()

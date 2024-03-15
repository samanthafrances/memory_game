# Save the Ocean Memory Card Game

## Description
- Live site: sam-yates-memory.surge.sh
This is an Ocean Cleanup themed 16 card game that tests the player's memory. 
- There will be 8 matching pairs.
- The player begins by clicking a card, and that card flips over and remains flipped over until another card is clicked. 
- Once the second card is clicked, if it matches the first card, both cards stay flipped over as you continue trying to match the rest of the cards. 

## Wireframes
- Figma https://bit.ly/3TaLHcE

## Pseudocode

- Create an array containing menu links and append them to the menu element.

- Establish variables and arrays to store game elements, graphics, and card states.

- Develop a shuffling function to randomize the graphics array.

- Upon page loading, initiate the game by shuffling the graphics array and assigning icons to the card elements.

- Implement a function named displayCard which:
Quickly exits if the board is locked or if the clicked card is already the first one.
Flips the card, adding 'open' and 'show' classes.
Sets the firstCard variable if no cards are flipped.
Sets the secondCard variable if one card is already flipped, then proceeds to check for a match.

- Introduce a function named reflipCard which:
Locks the board temporarily.
Removes 'open' and 'show' classes from both cards after a delay, resetting the board.

- Define a function called resetBoard to restore the board's initial state variables.

- Establish a function named disableCard which:
Eliminates the click event listener from both cards.
Checks for a win condition and resets the board accordingly.

- Craft a function titled checkMatch which:
Compares the icons of the first and second cards.
Calls disableCard() if they match; otherwise, initiates reflipCard().

- Formulate a function named checkWin which:
Prompts an alert with a win message if all cards are flipped.
Restarts the game and introduces a delay.

- Attach click event listeners to all card elements, directing them to trigger the displayCard function.
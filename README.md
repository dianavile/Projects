# Projects
__How to tackle the MemoryGame Project3__ with `project > requirements > plan > code" strategy`

##  Project specifications
1. __Shuffle Cards__: Shuffle cards randomly on load or restart
The Cards need to be shuffled on load or restart.
2. __Matching Cards__: 
The Game need to know how to handle matched and unmatched cards.
3. __Moves__:  
The Game displays the current number of moves a user has made.
4. __Star Rating__: 
The game shows star rating system (1-3). It reflects player’s performance based on number of moves. 
5. __The Timer__: 
When a player starts a game,  a displayed timer starts. When player wins the game, timer stops.
6. __Restart button__: 
The restart button allows player to reset the gameboard, timer and star rating system.
7. __A Congratulations Modal__: 
When player wins the game, a congratulations modal displays, including: time spend, star rating & play again button 

##  Game Requirements
- A grid with 16 cards
- 8 different pairs of cards
- Cards are randomly placed 
- The symbols face down
- On a click the card must turn and show the icon and stays turned
- On a click on a different card the card must turn and show the icon
- If the 2 turned cards match they stay turned
- If the cards don't match they turn back
- The game ends when all cards are flipped
- When the game ends show a modal
- Reset button
- Star rating
- Timer
- Move counter

##  Plan GAMEDEVELOPMENT: TODO list MEMORYGAME
1  Create an array/ (=A grid with 16 cards)
2  Shuffle cards and store in new array / done 
3  Create a loop and iterate over all cards/ TODO
4  Add each card´s HTML to the page "gameboard": deck > li > i/ TODO
*add li element "cards" & append to UL "deck"

5 Display the cards on the page
- shuffle the list of cards using the provided "shuffle" method below
- loop through each card and create its HTML
- add each card's HTML to the page

6 Create reference to card-deck= deck of all cards in game 

7 function to initialize on page creation 
8 shuffle Card and add cards to the array shuffledCards[]
9 Create a loop that iterates over each card element untill full lenght of cards array is covered. 
10 Each loop adds an EventListener for a click on the card, and runs the displayCard function on click 

11 Toggle
- Run the displayCard function to toggle (Hide/Show) an Element 
- And disable card when "open 

12 function createDeck

13 Shuffle function from http://stackoverflow.com/a/2450976
// @param {array}
// @returns shuffledarray

/**TODO: MEMORY GAME
 * set up the event listener for a card. If a card is clicked:
 *  - display the card's symbol (put this functionality in another function that you call from this one)
 *  - add the card to a *list* of "open" cards (put this functionality in another function that you call from this one)
 
 *  - if the list already has another card, check to see if the two cards match
 * IF MATCH, DO THIS: if the cards do match, lock the cards in the open position (put this functionality in another function that you call from this one)
 * ELSE, IF NO MATCH, DO THIS: if the cards do not match, remove the cards from the list and hide the card's symbol (put this functionality in another function that you call from this one)
 * MOVES increment the move counter and display it on the page (put this functionality in another function that you call from this one)
 * MODAL= if all cards have matched, display a message with the final score (put this functionality in another function that you call from this one)
 */
 
##  Tools

##  Code

##  Progress
DAY1:
1 Read the Project Requirements
2 Download the starterscode
3 Put starterscode in CodePen
4 Create a TODOLIST

##  Questions



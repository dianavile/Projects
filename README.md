# Projects
__How to tackle the MemoryGame Project3__ with `project > requirements > plan > code" strategy`

- Read the [project rubric](https://review.udacity.com/#!/rubrics/591/view) 
- Understand the game logic: write a TODOLIST for the code
- Download Starterscode. Open a new Pen in CodePen. 
- Start with HTML & JavaScript (game logic and functionality first).
- End with CSS (leave styling untill the end)
- Review and understand the given project files structure.

##  Project specifications (game logics & functionality)

### Memory Game Logic
- The game randomly shuffles the cards. 
- A user wins once all cards have successfully been matched.

### Memory Game Functionality
1. __Shuffle Cards__: Shuffle cards randomly on load or restart
The Cards need to be shuffled on load or restart.
2. __Matching Cards__: 
The Game need to know how to handle matched and unmatched cards.
3. __Moves__: The Game displays the current number of moves a user has made.
4. __Star Rating__: The game shows star rating system (1-3). It reflects player’s performance based on number of moves. 
5. __The Timer__: When a player starts a game, a displayed timer starts. When player wins the game, timer stops.
6. __Restart button__: The restart button allows player to reset the gameboard, timer and star rating system.
7. __A Congratulations Modal__: When player wins the game, a congratulations modal displays
including: time spend, star rating & play again button 

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

##  TODO-list MEMORYGAME
BEFORE GAME STARTS

### STEP 1: CREATE A CARD DECK 
__GOAL__: CREATE A GRID OF 16 CARDS (8 pairs of cards)
// Create a GRID for the game
- Create an array with all the icons in it.
- Create a reference to the deck (== deck of all cards in game)

### STEP 2: CREATE A CARD LIST 
__GOAL__: Add each card to the GRID/ Use DOM manipulation. 
//Add each card´s HTML to the page (ul): deck > li > i/ 
- Create a unordered list element (ul) from an array (https://stackoverflow.com/a/11128791/8498100)
- Create a list element (li)
- Add a "CLASS" to the (li)
- Create an icon element (i)
- Add a "CLASS" to the (i) element from the array
- Append (i) to (li) element 
- Append (li) element to (ul) "the deck" 

### STEP 3: CREATE A SHUFFLE ARRAY
- The first array is needed for the shuffle function (param array and returns an array in the end.) 
- The returned array= the shuffled array you put in. 
- Store this in a new array: Create a `const`and assign it the array.
- Check if Array[1] is shuffled with console.log in DEV TOOLS.

### STEP 4: CREATE EVENT LISTENER
// Initiate the Game
- Set up the event listener for a card. 
//Game start when player clicks on first card.
- Start the Game on CLICK (= first click card = `addEventListener`), Don’t start the game on page load.

### STEP 5: SHUFFLE THE CARDS
// Cards are randomly placed 
- Shuffle cards and store in new array= cards are randomly placed
- The symbols face down

START THE GAME
### STEP 6: START THE GAME: WHAT HAPPENS WHEN GAME START? 
//Display the Card
If 1 card is clicked:
- display the card's symbol 
Show the card on the deck.
(put this functionality in another function that you call from this one)

- Add the card to a *list* of "open" cards 
(put this functionality in another function that you call from this one)

If 2 card is clicked:
//If 1 card is clicked 2= same card? user click on the same card more than once, `if` statement to prevent clicking 2 the same card

//If 2 cards is different? 
 - if the list already has another card, check to see if the two cards match

 //IF CARDS MATCH, DO THIS: 
- if the cards do match, lock the cards in the open position 
 (put this functionality in another function that you call from this one)

//ELSE, IF NO MATCH, DO THIS: 
if the cards do not match, remove the cards from the list and hide the card's symbol 
(put this functionality in another function that you call from this one)

IMPORTANT! Do not try to make your cards show on the deck and add the eventListener at the same time 


### FROM HERE DRAFT (working on the logics) ### 

FINISH THE GAME
### STEP 6:  CREATE A FINISH MODAL: WHAT HAPPENS WHEN GAME IS FINISHED? 
// FINAL MODAL= 
- if all cards have matched, (8 pairs= 16 cards, all shown), DO THIS
- display a message with the final score 
(put this functionality in another function that you call from this one)
- Add Winner Message, Rating, Moves, Timer and Play Again button to Modal

### STEP: CREATE A RESTART BUTTON
### STEP: GAME SETTINGS (score)
- Add Rating (Stars)
- Add Moves
- Add Timer
- Add Restart button

### STEP : CREATE A MOVES COUNTER
//MOVES increment the move counter
-  display it on the page 
(put this functionality in another function that you call from this one)

### STEP 6: CREATE A TIMER
//Make a separate function for the timer
- Start the timer on first card click 
- Reset `clear` when restart button clicked.



### STEP 4: Display the cards on the page
- shuffle the list of cards using the provided "shuffle" method below

3  Create a loop and iterate over all cards/ TODO
- loop through each card and create its HTML
- add each card's HTML to the page

 function to initialize on page creation 
shuffle Card and add cards to the array shuffledCards[]

Create a loop that iterates over each card element untill full lenght of cards array is covered. 
Each loop adds an EventListener for a click on the card, and runs the displayCard function on click 

11 Toggle
- Run the displayCard function to toggle (Hide/Show) an Element 
- And disable card when "open 

12 function createDeck

13 Shuffle function from http://stackoverflow.com/a/2450976

###  DRAFT STOPS HERE (working on the logics) ### 

##  Tools & Resources
- Debugging JavaScript in Chrome DevTools: https://developers.google.com/web/tools/chrome-devtools/javascript/ 
- Difference setTimeout /setInterval: https://javascript.info/settimeout-setinterval
- Event Loop: https://www.youtube.com/watch?v=8aGhZQkoFbQ 

## EXAMPLE TUTORIALS
* http://www.thatsoftwaredude.com/content/6196/coding-a-card-deck-in-javascript
* https://scotch.io/tutorials/how-to-build-a-memory-matching-game-in-javascript
* http://www.developphp.com/video/JavaScript/Memory-Game-Programming-Tutorial
* https://www.youtube.com/watch?v=c_ohDPWmsM0&sns=em

##  Code

##  Progress
DAY1:
- 1 Read the Project Requirements
- 2 Download the starterscode
- 3 Put starterscode in CodePen
- 4 Create a TODOLIST

##  Questions



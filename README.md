_"Everyone should learn to program a computer, because it teaches you to think"._ — Steve Jobs

# Projects
__How to tackle a Project__ with `project > requirements > plan > code" strategy`

##__STEP 1: UNDERSTAND__
- Read the __project specifications__
- __Understand the game logic:__ Write the Game Requirements (game logics & functionality)
- Write the "_problems-to-solve_" down  as small steps in a `__TODOLIST__`
- __Research:__ search resources, add them to TODOLIST

##__STEP 2: PLAN__
- Download Starterscode. 
- Open a new Pen in CodePen. OR Create a Repository in GitHub.
- Add TODOLIST in startersfiles as `-COMMENTS-`

##__STEP 3: DIVIDE__
- Solve the `_problems & subproblems_` step-by-step according to TODOLIST.
- Solve each sub-problem one-by-one (not all at once!)
- Once you solved every sub-problem, connect the dots.
- Start with HTML & JavaScript (game logic and functionality first).
- End with CSS (leave styling untill the end.)

##__STEP 4: REVIEW__ `_Debug, Reassess, Research & Practice__`
- `Stuck:` Review and understand the given project files structure.
- `Debug:` figure out what you "really" told your program to do
- `Reassess:` Take a step back: How to solve this problem with general principles on a more global level? 
- Still stuck? `Start anew:` Delete everything and begin again with fresh eyes.
- `Research:` look for solutions for the subproblems.
- `Practice`, practice, practice

##  Resources & Tools
- [Develop Problem solving skill](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2) 
- [Debug JavaScript in Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/javascript/) 

# Project specifications MEMORY GAME 
Read the [project specifications](https://review.udacity.com/#!/rubrics/591/view)

## Game Logics
- The game randomly shuffles the cards. 
- A user wins once all cards have successfully been matched.

## Game Functionality
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

## Game Requirements
__In order to let the game work properly, the following is needed__:
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

# TODO-list
CREATE A grid with 16 cards(8x2 pairs), randomly placed
## STEP 1: CREATE A CARD GRID
- 1.1 `ARRAY[]`[Create an ARRAY of all cards as objects](https://www.w3schools.com/js/js_arrays.asp)
- 1.2 [Duplicate the array to get 8 pairs]=The ARRAY must hold 8 pairs of cards(16 cards=8pairs) 
`<i><img>`Add icons/images twice to array
- 1.3 `<ul>`[Create an ul from an array](https://stackoverflow.com/a/11128791/8498100)

## STEP 2: CREATE LIST OF 8 PAIRS of CARDS
//Show all card elements on the HTML (`Document= = html`)
[DOM manipulation](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- 2.1 `<#ul>`= Create id for <ul> with class .deck (e.g. #deck) 
- 2.2 Delete the class .deck from HTML.
- 2.3 `<ul>`[Create ul element] Create unordered list with length=16.
 -2.4 `<li>`[Create a list element](https://www.w3schools.com/jsref/met_document_createelement.asp)`  
- 2.5 [Add CLASS .card to list elements](https://www.w3schools.com/jsref/met_document_getelementsbyclassname.asp) 
- 2.6 `<li> to <ul> `=Append list as child to #deck.
- 2.7 `<i>`= Create array with 16 icons (fa fa-x) (e.g. cardsArray).

 ## STEP 3: SHUFFLE THE CARDS  & ADD SPECIFIC ICONS
- 3.1 Use `for Of Loop` to loop over each element in the Array (e.g. shuffledArray).
// RESULT: a grid of 16 cards with general icons.
// To create specific icons
- 3.2 `<i>`= Create an icon element.
- 3.3 For every icon in shuffledArray, append as CLASS to <i> `<i class="fa fa-anchor"></i>`
- 3.4 Append <li> element to <ul>=  Append every <i> elements as a child of ul item to #deck with class .card
 `<ulid=”deck”><li class="card"><i class="fa fa-anchor"></i></li></ul>`

## STEP 4: SHOW SYMBOLS FACE DOWN
- 4.1 Use [CSS transform](https://www.w3schools.com/cssref/css3_pr_transform.asp).

## STEP 5: CREATE `AddEventListener` on `Click` 
// Start the Game on `CLICK` to flip the cards and count the moves. Don’t start the game on page load.
- 5.1 Setup on `Click`Event listener as "first card is clicked" 
- 5.2 TURN THE CARD (flip the card) __HOW?__
- 5.3 ADD DELAY to flipped card (= CSS animation)
- 5.3 START THE TIMER: Create var "moveCounter" `onclick.addEventlistener`. Show it above the game.		
-5.4 SHOW ICON of CARD
-5.5 CARD STAYS OPEN (Leave 1st card turned)

 ## STEP 6: ON CLICK = Display 1 Card
//If 1 card is clicked:  display the card's symbol 
- 6.1 Show the card on the deck.= Add CSS class .show to item (functionality, called within event listener function)
- 6.2 Stores the item in a temporary array (“) 
IMPORTANT! Do not try to make your cards show on the deck and add the eventListener at the same time 
- 6.3 Add the card to a *list* of "openCards" (put this functionality in another function that you call from this one)

## STEP 7: Click on 2nd Card
// If 2 card is clicked: OPTION 1 or OPTION 2
7.1 OPTION 1= CARD = SAME CARD= Use`if` statement to prevent User click on the same card twice


- 5.3 Create var matchedArray.
- 5.4 Connect var to <span> tag in <section>.
- 5.5·Add event listener(‘click’) to #deck list items 


//OPTION 2= CARD = DIFFERENT CARD
 - if the list already has another card, check to see if the two cards match
 //IF CARDS MATCH, DO THIS: 
- if the cards do match, lock the cards in the open position 
 (put this functionality in another function that you call from this one)
//ELSE, IF NO MATCH, DO THIS: 
if the cards do not match, remove the cards from the list and hide the card's symbol 
(put this functionality in another function that you call from this one)

### STEP 8: CREATE A "GAME FINISHED" MODAL
// FINAL MODAL= 
- if all cards have matched, (8 pairs= 16 cards, all shown), DO THIS
- display a message with the final score 
(put this functionality in another function that you call from this one)
- Add Winner Message, Rating, Moves, Timer and Play Again button to Modal

RESOURCES:
-  `document.getElementById or `document.querySelector`method 
get an element by id. (From #id in html, the element is available in JavaScript)
- `parent.appenChild(child-to-add)`[`appendChild`method](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)
- [Node interface](https://developer.mozilla.org/en-US/docs/Web/API/Node)
`document.getElementByClassName`,
SHUFFLE THE CARDS
// Cards are randomly placed 
- Shuffle cards and store in new array= cards are randomly placed
- Make a shuffle function (with ARRAY of all cards)	
Loop through the cards: Randomize the cardsArray
The first array is needed for the shuffle function (param array and returns an array in the end.) 
make an empty ARRAY for shuffled cards 		
- The returned array= the shuffled array[] you put in. 
make an ARRAY (const)& assign it	
- Store this in a new array: Create a `const`and assign it the array.
- Check if Array[1] is shuffled with console.log in DEV TOOLS.
DRAFT


<--------### FROM HERE DRAFT (working on the logics) ### 

	
	
				
"3 create matching logic 
              move counter 
              guess(es) counter"				
	if firstguess === secondguess then change css so then won't flip			
				
4 create star rating				
	"If moves >= 3 then change 1 star classname, 
If moves >= 6 then change another star"			
				
5 create a timer				
	Timer should pause when all 16 guesses are right and the time should show on the winning modal			
				
6 create a winning logic				
	In the  code for the matching logic, count 1+ to a variable like winCount and then execute the code for the winning modal screen If winCount = 16			
	if all 16 guesses are right then stop the timer, show modal screen that shows: time, stars, moves, restart button			
				
7 create modal screens				
	The restart button sets timer, star rating, moves, guesses to 0, also the game deck has to flip all cards and randomize them. and modal should close			

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

### STEP : CREATE A TIMER
//Make a separate function for the timer
- Start the timer on first card click 
- Reset `clear` when restart button clicked.

### STEP : Display the cards on the page
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

###  DRAFT STOPS HERE (working on the logics) ### ----------------------------->

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



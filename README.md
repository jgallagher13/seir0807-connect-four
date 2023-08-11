## Analyze the app's functionality

As a user, I want a feature, because of reason 


MVP (Minimal Viable Product)

As a user
- I want to be able to have 2 players, because that is how connect four is played.
- I want to be able to take turns.
- I want to alternate dropping colored discs into 1 of 7 columns.
- I want to be able to win if I get 4 in a row.
- I want to know who won or if it was a tie.
- I want to be able to play the game again if it's over.

If I have some time I would like to add these
- I want a success animation.
- I want a dropping animation.
- I want a difficulty setting.
- I want to choose my color of the disc.
- I want to keep track of total wins and losses.

## Think about the overall design (look & feel) of the app
- clean
- purple and orange discs
- Poppins - font
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@100&display=swap" rel="stylesheet">
```
```css
font-family: 'Poppins', sans-serif;
```

## Wirefram the UI

A wireframe is a way to represent your game (app)

- High fidelity
  - Working demo
  - images
  - buttons might be clickable
  - hover affects happen
  - little more than just a drawing

- Low fidelity
  - just a drawing
  - layout of the page
  - where is the header going?
  - where are my messages to the user going?
  - where are all my buttons going?
  - does this feel too crowded? Does this feel too empty?

## Pseudocode

- Define required constants
  - color constant

- Define required variables used to track the state of the game
  - game board - 1 big array that holds 7 smaller arrays
  - turn - 1 || -1
  - winner - null || 1 || -1 || 'T'

- Cache DOM elements
  - Message place
  - Play again button
  - column buttons/markers

- Upon loading the app should:
  - Init the state variables
    - create the 7 nested arrays
    - turn var should be set to 1 (player 1)
    - winner var should be null
  - Render changes to the DOM
    - Render the board, should be completely blank
    - Render the message Purple's Turn
    - Do not render the play again button
  - Wait for interaction

- Handle a player clicking a column button
  - Update the board array with the player move
  - Update the turn var
  - Check for a winner
  - Re-render the board with the players move

- Handle a player clicking the replay button
  - Reset the state vars 
  - re-render the board

- Check for a winner
  - Check for 4 in a row
  - we will use offsets to count the colors of the discs in the arrays

## Identify the application's state (application-wide data)

- game board - array of 7 nested arrays
```js
let board
```
- turn var 
```js
let turn
```
- winner var
```js
let winner
```

Tic-Tac-Toe Game By Edrees Amiri / Crptk (github)
Video demo: https://youtu.be/HEfmGL1IxcM?si=XSTKhLf9cPo2I68k

Description: My first programming project as well as my final CS50 project, created without the use of Youtube tutorials and with the help of ChatGPT when it comes to CSS layout, as well as Javascript syntax and optimization.
I used the skills I learned from Week 8 especially, mostly with the CSS and HTML, but I especially learned a lot about Javascript as that was a big struggle for me during the course.
The things I asked ChatGPT were things like:
- How do I create for loops in JavaScript?
- How can I make the website sense which element my mouse is clicking in javascript?
- How do I format a grid?
- How do I insert images into my website using Javascript?
etc.

The HTML is fairly simple, I used cells to create the game grid itself, and I used things such as grid display for the game in CSS.
The Javascript works based on one 2D array called gameArray. Once the game starts, all the values are zero. If Player 1 clicks on a cell, the program will figure out which index in the gameArray was clicked,
then it will change that value to 1, and 2 for Player 2.

- The highlightWinningCells function is a quality of life function that'll colour the cells depending on who won.
- The checkWinCondition function is a function that checks every possible winning outcome, and if it finds one, it'll push all of the indexes that were won into a new winningCells array, where it will use those
 values to highlight the corresponding cell id number in highlightWinningCells.
- The checkTieCondition function involves checking the counter for all the filled cells, if all the cells are filled and the game hasn't ended, it will declare a tie.
- The handlePlayerMove function involves checking the row, column, and cell that was clicked, incrementing the filledCells by 1, appending an image under the cell that was clicked on, and checking both
 the win and tie condition to see if the game has ended yet. If it's not game over, it will proceed to Player 2's turn.
- The handleAIMove function is basically the same thing as the handlePlayerMove function, except it has no arguments passed because it randomly generates a cell to choose, as well as a row and column.
- Below the handleAIMove function is a listener for every cell that checks if it's clicked or not. It will stop functioning if the game is over or if its not the player turn, otherwise it will figure
 out which row and column was selected using the cell's id number. It'll then run the handlePlayerMove, and then checks if the game isn't over before proceeding with the AI's move.
- The last function is basically just the reset button, resetting all the values back to default so the game can be played again.
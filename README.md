# Mitesh
AI Tic Tac Toe Game
Project Objective

The aim of this project is to create a Tic Tac Toe game where a user plays against an AI computer player.

The project demonstrates how Artificial Intelligence can be applied in simple games to make decisions.

The AI analyzes the game board and chooses the best move based on the selected difficulty level.

Technologies Used
HTML

HTML is used to create the structure of the game board and buttons.

CSS

CSS is used to design the game board and improve the visual appearance of the game.

JavaScript

JavaScript controls the game logic, player moves, AI moves, and winner detection.

Game Board Representation

The game board consists of 9 cells arranged in a 3 × 3 grid.

In the program, the board is stored using a JavaScript array of 9 elements.

Example:

["X", "", "O",
 "", "X", "",
 "", "", "O"]

Each position can contain:

X – Player
O – AI
Empty – Available space
Game Flow Logic

The game works in the following steps:

Player clicks a cell
The system places X in that cell
The program checks if the player wins
If the game continues, the AI makes its move
The system checks again for a winner or draw
Winning Condition Detection

The game checks 8 possible winning combinations.

Rows
0 1 2
3 4 5
6 7 8
Columns
0 3 6
1 4 7
2 5 8
Diagonals
0 4 8
2 4 6

If any three positions contain the same symbol, the player wins.

Artificial Intelligence Decision Making

The AI selects moves based on the chosen difficulty level.

Easy Mode

The AI selects a random empty position.

Medium Mode

The AI uses simple rules:

Try to win if possible
Block the player if they are about to win
Otherwise choose a random move
Hard Mode

The AI uses the Minimax Algorithm to calculate the best possible move.

Evaluation Function – Tic Tac Toe
Purpose

When the algorithm stops early (cutoff), we need a way to estimate how good a board position is.

Definition

Let p be a board position.

The evaluation function f(p) is defined as:

f(p) = RCDC - RCDO
Meaning

RCDC
Number of rows, columns, or diagonals where the computer can still win

RCDO
Number of rows, columns, or diagonals where the opponent can still win

Interpretation
If the computer has more winning chances → value is positive
If the opponent has more winning chances → value is negative

This gives a numerical score to non-terminal board positions.

Game Tree (Two-Player, Deterministic, Turn-Based)

This concept explains how the game expands as a tree structure.

Each node represents a board position
Each level represents one player's turn
The MAX player (computer) tries to maximize the score
The MIN player (opponent) tries to minimize the score
Tree Structure
Top node → current board state
Branches → possible moves
Levels alternate between players
MAX level → Computer move
MIN level → Opponent move

Leaf nodes (end states) are evaluated using the utility function:

-1  → Opponent wins
0   → Draw
+1  → Computer wins

Large value = good for computer
Small value = bad for computer

Sample Evaluations – Tic Tac Toe
Setup
X = Computer
O = Opponent

For each board position we count:

Rows where X can still win
Columns where X can still win
Diagonals where X can still win

And the same for O.

The evaluation score is:

f(p) = (X chances) - (O chances)
Example

If:

X has 3 possible winning lines
O has 1 possible winning line

Then:

f(p) = 3 - 1 = +2

This means the position is good for the computer.

Even if no one has won yet, the evaluation helps determine who is closer to winning.

Event Handling

The game uses event listeners to detect when a player clicks a cell.

When a cell is clicked:

The move is recorded
The board updates
The system checks for a winner
The AI makes its move
Draw Detection

A draw occurs when:

All 9 cells are filled
No player has won

The system then declares the game as a draw.

Project Limitations

Some limitations of this project:

Only single player mode
No online multiplayer
No score tracking system
Future Improvements

The project can be enhanced by adding:

Multiplayer mode
Scoreboard system
Better UI and animations
Mobile responsive design
Conclusion

This project demonstrates how Artificial Intelligence can be applied to games to make intelligent decisions.

It also showcases the implementation of game logic, algorithms, and user interaction using web technologies.

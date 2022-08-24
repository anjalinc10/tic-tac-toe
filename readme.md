### Project Introduction
**This is Tic Tac Toe Game.**

### Project Description
The game is played by two individuals. First, we draw a board with a 3×3 square grid. The first player chooses ‘X’ and draws it on any of the square grid, then it’s the chance of the second player to draw ‘O’ on the available spaces. Like this, the players draw ‘X’ and ‘O’ alternatively on the empty spaces until a player succeeds in drawing 3 consecutive marks either in the horizontal, vertical or diagonal way. Then the player wins the game otherwise the game draws when all spots are filled.

Libraries Used

1) **pygame library** - Pygame is a great library that will allow us to **create the window and draw images and shapes on the window.** The pygame library is an open-source module for the Python programming language specifically intended to help you make games and other multimedia applications.

How to Install
To implement this game, we will use the basic concepts of Python and Pygame which is a Python library for building cross-platform games. It contains the modules needed for computer graphics and sound libraries. To install the library, you can use pip installer from the command line:

-> pip install pygame

### Steps to Build a Python Tic Tac Toe Game
First, let’s check the steps to build Tic Tac Toe program in Python:

1)Create the display window for our game.

2)Draw the grid on the canvas where we will play Tic Tac Toe.

3)Draw the status bar below the canvas to show which player’s turn is it and who wins the game.

When someone wins the game or the game is a draw then we reset the game.

**1. Initializing game components**
So let’s start by importing the pygame library and the time library because we will use the time.sleep() method to pause game at certain positions. Then we initialize all the global variables that we will use in our Tic Tac Toe game.
Here, the TTT is the main 3×3 Tic Tac Toe board and at first, it will have 9 None values. The height and width of the canvas where we will play the game is 400×400.

**2. Initializing Pygame window**
We use the pygame to **create a new window** where we’ll play our Tic Tac Toe game. So we initialize the **pygame with pg.init() method** and the window display is set with a width of 400 and a height of 500. We have reserved 100-pixel space for displaying the status of the game.

The **pg.display.set_mode() initializes the display** and we reference it with the screen variable. This screen variable will be used whenever we want to draw something on the display.
The pg.display.set_caption method is used to set a name that will appear at the top of the display window.

**3. Load and transform images**
The Python project uses many images like the opening image that will display when the game starts or resets. The **X and O images** that we will draw when the user clicks on the grid. We load all the images and resize them so that they will fit easily in our window.

**4. Define the functions**
 In pygame, the **blit() function** is used **on the surface to draw an image on top of another image.**

So we draw the opening image and after drawing, we always need to update the display with **pg.display.update().** When the opening image is drawn, we wait for 1 second using **time.sleep(1)** and fill the screen with white colour.

Next, we **draw 2 vertical and horizontal lines** on the white background to make the 3×3 grid. In the end, we call the **draw_status() function**

The **draw_status() function draws a black rectangle** where we update the status of the game showing which player’s turn is it and whether the game ends or draws.

The **check_win() function** checks the Tic Tac Toe board to see all the marks of ‘X’ and ‘O’. It calculates whether a player has won the game or not. They can either win when the player has marked 3 consecutive marks in a row, column or diagonally. This function is called every time when we draw a mark ‘X’ or ‘O’ on the board.

The **drawXO(row, col) function** takes the row and column where the mouse is clicked and then it draws the ‘X’ or ‘O’ mark. We calculate the x and y coordinates of the starting point from where we’ll draw the png image of the mark.

The **userClick() function** is triggered every time the user presses the mouse button.

When the user clicks the mouse, we first take the x and y coordinates of where the mouse is clicked on the display window and then if that place is not occupied we draw the ‘XO’ on the canvas. We also check if the player wins or not after drawing ‘XO’ on the board.

The last function is the **reset_game().** This will restart the game and we also reset all the variables to the beginning of the game.

**5. Run the tic tac toe game forever**

To start the game, we will call the **game_opening() function.**

**Input** - 1) **o1.png** 2) **x1.png**

**Output** - **tic_tac.jpg**
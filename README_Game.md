# Missionaries and Cannibals Game (Pygame Implementation)

## Missionary-Cannibal-Problem-in-AI
A simple graphic game to understand and explain the famous "Missionary-Cannibal" problem in AI

## Project Description

This project is a graphical implementation of the classic **Missionaries and Cannibals** puzzle game built using Python and the Pygame library. The game simulates the traditional river crossing problem where three missionaries and three cannibals must cross a river using a boat, while ensuring that cannibals never outnumber missionaries on either side.

The player interacts with the game through a graphical interface, selecting characters to board a boat and transporting them across the river. The program keeps track of the game state, number of moves, and whether the player wins or loses.

## Objective

The objective of the game is to safely transport all missionaries and cannibals from the left shore to the right shore without violating the puzzle rules.

## Game Rules

1. The boat can carry **a maximum of two people** at a time.
2. The boat cannot move without at least **one passenger**.
3. If cannibals outnumber missionaries on either shore (and missionaries are present), the missionaries get eaten and the game ends.
4. The goal is to move **all three missionaries and three cannibals** safely to the other side.

## Features

* Graphical game interface using Pygame
* Interactive character selection using mouse clicks
* Animated boat movement across the river
* Real-time display of game state and actions
* Move counter to track player progress
* Game over detection when rules are violated
* Winning screen when puzzle is solved
* Background music and sound effects
* Sound on/off toggle
* New game restart option

## Technologies and Libraries Used

Python 3

Libraries:

* Pygame – Used for graphics rendering, game loop, audio, and event handling

## Additional Assets Used

The game requires several external files for images and audio.

Images:

* boat.png
* bg1.png
* missionary.png
* missionary1.png
* cannibal.png
* cannibal1.png
* newgame.png
* newgame1.png
* gameover.png
* winner.png
* go.png
* go1.png
* soundon.png
* soundoff.png

Audio:

* bgmusic.mp3
* gameover.wav
* won.wav

Additional Python Files:

* Person.py
* Boat.py

These files contain the class definitions used to represent characters and boat behavior.

## How the Game Works

1. The program initializes the Pygame window and loads all game assets.
2. Three missionary objects and three cannibal objects are created.
3. The boat is positioned on the left side of the river initially.
4. The player selects characters to board the boat by clicking on them.
5. The boat moves across the river when the player presses the **Go** button.
6. The game updates the current state after each move.
7. The system checks whether the game rules are violated.
8. If cannibals outnumber missionaries on either side, the game ends.
9. If all characters reach the right shore safely, the player wins.

## Game State Representation

The game state is stored using a list:

```
state = [missionaries_left, cannibals_left, boat_position]
```

Example:

```
[3, 3, 1]
```

Meaning:

* 3 missionaries on the left side
* 3 cannibals on the left side
* Boat is on the left side

## Action Representation

Actions represent the number of missionaries and cannibals currently in the boat.

Example:

```
action = [missionaries_in_boat, cannibals_in_boat]
```

The game updates the state after each boat movement.

## How to Run the Program

Step 1: Install the required library

pip install pygame

Step 2: Ensure all required image and audio assets are present in the same project directory.

Step 3: Make sure the additional files are available:

* Person.py
* Boat.py

Step 4: Run the program

python missionaries_cannibals_game.py

The game window will open and gameplay will begin.

## Game Controls

Mouse Click
Select missionaries or cannibals to place them on the boat.

Go Button
Moves the boat across the river.

New Game Button
Restarts the game.

Sound Button
Toggles background music on or off.

Close Window
Exit the game.

## Possible Improvements / Future Work

* Add AI solver for the puzzle
* Add hint system for optimal moves
* Add animations for character movement
* Improve UI design and graphics
* Add difficulty levels
* Track best score or least number of moves
* Add tutorial or instructions screen
* Support keyboard controls

## Conclusion

This project demonstrates how a classic logical puzzle can be implemented as an interactive graphical game using Python and Pygame. It highlights concepts such as game state management, rule validation, user interaction, and multimedia integration.

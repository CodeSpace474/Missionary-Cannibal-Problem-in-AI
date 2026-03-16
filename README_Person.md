# Person Class – Missionaries and Cannibals Game

## Project Description

This file defines the **Person class**, which represents the characters in the Missionaries and Cannibals game developed using Python and Pygame. Each character in the game (either a missionary or a cannibal) is represented as an object of this class.

The class is responsible for storing the character’s position, type, movement behavior, and visual representation in the game interface.

## Purpose of the Person Class

The Person class manages:

* Representation of missionaries and cannibals
* Character positions on shores or in the boat
* Character movement during boat travel
* Displaying the character on the screen
* Highlighting a character when selected

## Class Attributes

The class defines two static attributes representing the dimensions of the character image:

```
width  = 40
height = 100
```

These values help determine the clickable area for interaction.

## Position System

The variable **pos** represents the logical position of the character in the game. The positions are defined as follows:

```
0 → Character on the left shore
1 → Character on the right shore
2 → Left seat of boat on the left shore
3 → Left seat of boat on the right shore
4 → Right seat of boat on the left shore
5 → Right seat of boat on the right shore
```

This system helps track where each missionary or cannibal currently exists in the game.

## Constructor (Initialization)

The constructor initializes the character object with position, movement, and image parameters.

Parameters:

* x : X-coordinate of the character on the screen
* y : Y-coordinate of the character on the screen
* x_change : Horizontal movement speed for animations
* pos : Current logical position of the character
* char : Character type ('M' for Missionary, 'C' for Cannibal)
* leftright : Indicates which shore the character belongs to
* image1 : Default character image
* image2 : Highlighted character image
* gameDisplay : Pygame display surface used for rendering

Example:

```
person(x, y, x_change, pos, char, leftright, image1, image2, gameDisplay)
```

## Internal Attributes

The constructor also creates two rectangle coordinates used for mouse interaction:

```
rect_x = x + 12
rect_y = y
```

These values represent the clickable region for the character.

## Methods

## display()

This method draws the character on the game screen using the default image.

Function:

* Displays the missionary or cannibal image at the current coordinates.

Example behavior:

```
gameDisplay.blit(image1, (x, y))
```

## highlight()

This method highlights the character when the player hovers over or selects it.

Function:

* Displays the alternate image (highlight version) of the character.

Example behavior:

```
gameDisplay.blit(image2, (x, y))
```

## Game Interaction

During gameplay:

1. Characters are displayed on the shore.
2. The player can hover over a character.
3. The character becomes highlighted using the `highlight()` method.
4. Clicking the character moves them to the boat.
5. The character then travels with the boat to the other shore.

## Dependencies

This class requires:

* Python 3
* Pygame library

Install Pygame if needed:

```
pip install pygame
```

## Integration with the Game

The Person class is used in the main game script to create the six characters required for the puzzle.

Example:

```
missionary = person(x, y, 0, 0, 'M', 'left', missionary_img, missionary_highlight_img, gameDisplay)

cannibal = person(x, y, 0, 0, 'C', 'left', cannibal_img, cannibal_highlight_img, gameDisplay)
```

These objects are stored in a list and managed during gameplay.

## Possible Improvements

* Add walking animations for characters
* Improve collision detection for clicks
* Use sprite classes from Pygame for better structure
* Add character sound effects
* Add smooth transitions when boarding the boat

## Conclusion

The Person class plays a key role in representing missionaries and cannibals in the game. It handles character positioning, display rendering, and interaction logic, making it an essential component of the Missionaries and Cannibals puzzle game implementation.

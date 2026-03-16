# Boat Class – Missionaries and Cannibals Game

## Project Description

This file contains the **Boat class**, which is used in the Missionaries and Cannibals game implemented using Python and Pygame. The class represents the boat positions and handles the display behavior when characters (missionaries or cannibals) interact with the boat.

The Boat class is responsible for managing the placement and visual highlighting of passengers when they are selected to board the boat. It works together with the main game logic and the character objects defined in the `Person` class.

## Purpose of the Boat Class

The Boat class manages:

* Boat slot positions where characters can sit
* Highlighting the correct position when a character is selected
* Displaying missionary or cannibal images in the correct boat seat
* Interacting with the main game display

## Class Structure

Class Name:

```
boat
```

Class Attributes:

```
width  = 40
height = 100
```

These attributes define the approximate dimensions of the boat interaction area.

## Constructor (Initialization)

The constructor initializes the boat object with position and display parameters.

Parameters:

* x : Horizontal position of the boat slot
* y : Vertical position of the boat slot
* pos : Logical boat position identifier (values 2, 3, 4, 5)
* image1 : Image used for displaying a missionary
* image2 : Image used for displaying a cannibal
* gameDisplay : Pygame surface used to render graphics

Example:

```
boat(x, y, pos, missionary_image, cannibal_image, gameDisplay)
```

## Method Description

## highlight(a, b, c)

This method visually highlights a character position on the boat.

Parameters:

* a : Current boat X coordinate
* b : Current boat Y coordinate
* c : Character type ('M' for missionary, 'C' for cannibal)

Functionality:

1. Determines which seat position on the boat is being used.
2. Checks whether the character is a missionary or cannibal.
3. Displays the corresponding character image on the boat.

Boat Position Logic:

* Position 2 or 3 → Left side seat of the boat
* Position 4 or 5 → Right side seat of the boat

Depending on the seat position, the character image is drawn at a specific offset relative to the boat.

Example Logic:

```
if pos == 2 or pos == 3:
    display character on left seat
elif pos == 4 or pos == 5:
    display character on right seat
```

## Integration with Game

This class is used by the main game script to control how characters are displayed when they board the boat.

Workflow:

1. Player selects a character.
2. The game determines the available boat seat.
3. The `highlight()` method is called.
4. The selected character image is rendered in the correct seat.

## Dependencies

This class requires:

* Python 3
* Pygame library

Install Pygame if necessary:

```
pip install pygame
```

## How It Is Used

Example usage in the main game:

```
boat_slot = boat(x, y, pos, missionary_img, cannibal_img, gameDisplay)

boat_slot.highlight(boat_x, boat_y, character_type)
```

This displays the selected character in the appropriate position on the boat.

## Possible Improvements

* Add animated boarding and disembarking
* Add visual indicators for available seats
* Implement boat capacity checking within the class
* Add sound or animation effects when passengers board
* Improve position management using seat objects

## Conclusion

The Boat class is a supporting component of the Missionaries and Cannibals game that manages the graphical representation of passengers sitting on the boat. It helps organize the game’s visual logic and ensures that characters appear in the correct boat positions during gameplay.

# ZTypeWorld Game

## Overview
**ZTypeWorld** is an engaging Java game where words fall from the top of the screen, and your mission is to type the correct letters to eliminate them before they hit the bottom. It's a fun way to sharpen your typing skills while testing your speed and accuracy!

This game was developed as part of my **Fundamentals of Computer Science 2** course, where I explored object-oriented programming, interface-driven design, and functional decomposition to create an interactive project.

---

## Features
- **Interactive Gameplay:** Type letters to clear falling words.
- **Dynamic Word Movement:** Words descend gradually, and the game becomes more challenging over time.
- **Random Word Generation:** New words appear periodically to keep you on your toes.
- **Game Over Screen:** If a word reaches the bottom of the screen, the game ends with a "GAME OVER" message.

---

## How to Play
1. Launch the game.
2. Words start falling from the top of the screen.
3. Type the first letter of a word to activate it.
4. Keep typing the remaining letters to clear the word.
5. The game ends if a word reaches the bottom of the screen.

---

## Core Components

### Interfaces:
- **ILoWord:** Represents a list of words, with methods for managing, drawing, and checking game conditions.
- **IWord:** Represents individual words (active or inactive) and handles player interactions.

### Classes:
- **MtLoWord:** Represents an empty list of words.
- **ConsLoWord:** Represents a non-empty list of words.
- **ActiveWord:** A word the player is actively typing.
- **InactiveWord:** A word waiting to be typed.
- **Utils:** Contains helper functions like random word generation.
- **ZTypeWorld:** The main game logic, handling user input, ticks, and rendering.

### Constants (defined in `IConstant`):
- **Screen dimensions:** `B_WIDTH = 500`, `B_HEIGHT = 600`
- **Alphabet:** `ALPHABET = "abcdefghijklmnopqrstuvwxyz"`

---

## How It Works

### Word Management
- Words are stored in linked lists (`ILoWord`) for dynamic addition and removal.
- Words can be **Active** (typed by the player) or **Inactive** (waiting to be typed), with colors distinguishing them (active = black, inactive = red).

### Gameplay Mechanics
- **Typing:** Type letters to match and clear words. Matching letters activate a word and remove the typed letter.
- **Movement:** Words drop 1 unit every tick. If a word reaches the bottom, the game ends.
- **Random Words:** New words are generated and added every few ticks.

### End Condition
The game ends when a word reaches the bottom of the screen (`y >= 600`).

### Controls
- **Keyboard:** Type the first letter to activate a word, then continue typing to clear it.

---

## Development

### Prerequisites
- **Java Development Kit (JDK):** Make sure Java is installed.
- **Tester Library:** For testing the game logic.
- **JavaLib Library:** For graphics and world-building.

### Running the Game
1. Clone the repository or save the provided `.java` file.
2. Import the project into your preferred IDE (e.g., IntelliJ IDEA, Eclipse, VS Code).
3. Add the Tester and JavaLib libraries to your project build path.
4. Run the `ZTypeWorldExamples` class to start the game.
   - The game opens in a 500x600 pixel window.

### Testing
- Unit tests are included in the `ZTypeWorldExamplesGame` class.
- Run `testBigBang()` for full game testing or use individual test methods like `testAddToEnd` or `testMoveDown` to check specific functionalities.

---

## Customization
- **Word Length:** Modify the `randomLetters` method in the `Utils` class.
- **Speed:** Adjust the tick rate or movement increment in `addY`.
- **Difficulty:** Change how often new words are generated.

---

## Acknowledgments
- **Libraries:** `javalib.worldimages`, `javalib.funworld`
- **Inspiration:** Typing games like **ZType**

---

Enjoy playing and boost your typing speed! 🚀

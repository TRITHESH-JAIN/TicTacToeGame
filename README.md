# Tic Tac Toe Game – Java Project

## Revision Notes for Tic Tac Toe Game Implementation

### Overview
This project implements a classic Tic Tac Toe game using Object-Oriented Programming (OOP) principles and design patterns in Java. The goal was to build the game in a modular, scalable, and maintainable way.

---

### Key Concepts

#### 1. Building the Game Architecture
- Model Classes: 
  - Classes such as `Player`, `Board`, `Move`, `Cell`, and `Symbol` were created to handle specific responsibilities.
- Game Class:
  - Maintains the list of players, game board, list of moves, current game state (e.g., IN_PROGRESS, WIN, DRAW), and winning strategies.
  - Contains the business logic and controls the overall game flow.

#### 2. Design Patterns

- Builder Pattern:
  - Used to construct complex objects like the game instance.
  - Helps in step-by-step object creation using a private constructor and builder class.

- Strategy Pattern:
  - Allows different winning strategies (row, column, diagonal) to be defined and used independently.

#### 3. Constructors and Enums
- All model classes have proper constructors to avoid null pointer exceptions.
- Enums are used for defining constants such as `PlayerType` (HUMAN, BOT) and `BotDifficultyLevel` (EASY, MEDIUM, HARD).

#### 4. Validations
- Duplicate Symbol Check: Ensures no two players use the same symbol.
- Player Count vs. Board Dimension: Verifies appropriate player count relative to board size.
- Bot Count Validation: Restricts the number of bots allowed in the game.

#### 5. Game Flow
- The game is driven by a main class that interacts with the controller to handle moves and state updates.
- Uses `Scanner` for taking player inputs and continues until a win or draw condition is met.

#### 6. Game State and Board Operations
- Logic for displaying the board after every move.
- Updates the board and checks for a win or draw condition after each move.

#### 7. Exception Handling
- Custom exceptions are defined to handle specific validation errors such as:
  - `DuplicateSymbolException`
  - `MoreThanOneBotException`

---

### Conclusion
This project demonstrates how to develop a software model for a Tic Tac Toe game using solid design principles. The use of Builder and Strategy patterns ensures clarity and flexibility in the codebase. Validation checks and error handling add robustness. 

Future enhancements could include:
- Adding a graphical user interface (GUI)
- Introducing more advanced rules
- Integrating AI for bot moves

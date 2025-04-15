# 🎮 2048 Game in C++  

A classic 2048 puzzle game implemented using C++ with real-time console rendering. Slide and merge numbered tiles on a 4x4 grid to reach the 2048 tile and keep going to achieve the highest score! 

## 🌟 Table of Contents
- Project Description
- Key Features
- Installation
- Gameplay Controls
- How To Play
- Data Structure Analysis
- Object-Oriented Structure
- Key Member Functions
- Code Structure
- Prerequisite

## 📄 Project Description
This is a console-based implementation of the famous puzzle game *2048, developed entirely in C++. The game board is a 4x4 grid where the player moves numbered tiles. When two tiles with the same number collide during a move, they merge into a new tile with their sum. The goal is to create a tile with the number **2048*. The game also features real-time score tracking,and high score storage.

## 🚀 Key Features
- **Classic 2048 Gameplay**: Slide, combine, and grow your tiles to hit the 2048 goal
- **Real-Time Console Rendering**: Efficient and clean updates without flickering
- **High Score Tracking**: Keeps your best score saved across sessions
- **Platform Compatibility**: Works on Windows
- **Color Output Support**: Visual appeal using color formatting
- **Restart Option**: Restart any time and try again

## 🛠 Installation
To run the 2048 game, follow these steps:

1. *Clone the Repository*:
```bash
git clone https://github.com/rahul-badgujar/2048-Game-Console-Version.git
cd 2048-Game-Console-Version
Compile the Code (using g++):
```
Copy
```bash
g++ main.cpp Game.cpp Player.cpp Utilities.cpp -o 2048_game.exe
```
For Running the Game, Copy
```bash
./2048_game.exe
```

## 🎮 Gameplay Controls
- **WASD Keys (Alternative Controls) :**
    - `W`→ Move Up
    - `A`→ Move Left
    - `S`→ Move Down
    - `D`→ Move Right
- **Other Controls :**
    - `X`→ Exit the Game
    
## 🕹 How To Play

- **Objective :** Merge matching tiles on a 4x4 board to create a tile with the number 2048.
- **Gameplay Mechanics :**
    - Each move shifts all tiles in the chosen direction
    - If two adjacent tiles have the same number, they merge into one tile of double value
    - A new tile (2 or 4) is spawned after every move in a random empty spot

    - The game continues until you either:
        - Win by reaching 2048
        - Lose when no more moves are possible (i.e., the board is full and no merges can be made)
- **Scoring System :**
    - Every successful merge adds the merged value to your score
    - Your current and best scores are displayed during gameplay   

## 📊 Data Structure Analysis

- **2D Array (int board[4][4]) :** Represents the 4x4 game board
- **Text File (highscore_data.txt) :** Stores the highest score achieved
- **Enums / Constants :** Used for direction mapping and status flags

## 🧱 Object-Oriented Structure

| Class/Sturct           | Responsibility                                                   |
|----------------|-----------------------------------------------------------------|
|`Game`|Core Game mechanics : logic, board updates, movement, and rendering |
|`Player`|Tracks player score and high score from file|
|`Utilities`|Provides helper functions like rendering the board, printing messages, and delay utilities|
|`Debugger`|(Optional) Debugging features for development and testing|

## 🔑 Key Member Functions

### Game Class
- `initilizeGame()` → Sets the board to all zeros and spawns two random tiles
- `move(direction)` → Handles the main title movement and mearging logic
- `fillRandomTile()` → Spawns a 2 or 4 tile at a random empty location
- `undoMove` → Reverts the board to its last state using a stack
- `isGameOver()` → Returns true if no more valid move exists
- `isGameWon()` → Returns true if a tile with 2048 is found
- `drawBoard()` → Prints the board with borders and colored tiles
- `saveGameState()` → Saves the current board state for Undo
- `resetGame()` → Clears the board and resets score

### Player Class
- `getScore()` → Returns current score
- `addScore(value)` → Adds merged value to the player's score
- `updateHighScore()` → Saves new high score if exceeded

### Utilities
- `printMessageCenter(text)` → Prints a message in the centre of the screen
- `delay(ms)` → Introduces a delay for smoother transitions
- `clearScreen()` → Clears the console output

## 🤔Additional features that could be added 
- **🔢 Move Counter**
    - ✅Description : Counts the number of moves the player has made so far.
    - 🧠 How it Works : 
        - Start a counter at 0
        - Increment it each time a valid move is made
- **🎮 Game Save & Load**
    - ✅Description : Lets players save their current progress and load it later—super useful for long sessions!
    - 🧠 How It Works:
        - Save the current board, score, and maybe highScore to a file (like savegame.txt).
        - Load it back when the game starts (or when the player presses L).

- 🔁 Undo Move
    - ✅ Description: Lets the player revert the game to the previous state before their last move—very useful if they make a mistake.
    - 🧠 How It Works:
        - Before every move, save a copy of:
            - The board (2D array)
            - The score
        - If the player presses U (for undo), restore those saved values.

## 📁 Code Structure
**2048-Game-Console-Version/**  
│── bin/    
│── obj/    
│── screenshots/  
│── main.cpp    
│── Game.cpp / Game.h  
│── Player.cpp / Player.h  
│── Utilities.cpp / Utilities.h  
│── Debugger.cpp / Debugger.h  
│── rlutil.h  
│── highscore_data.txt  
│── README.md  
│── 2048 Game Console Version.cbp (Code::Blocks Project File)

## ✅ Prerequisites
- A C++ compiler (e.g., g++, clang++)
- Windows OS
- Console with ANSI escape code support (for colored output)

🎉 Thanks for checking out this investigation project! Hope you enjoy playing! 🚀

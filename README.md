# 💣 Retro-Mindsweeper Game Project 💣

### Short Description
A desktop implementation of the classic **Minesweeper** game developed in Python using the **Tkinter** GUI framework. This was used as my AP Computer Science Principles project, and since the year is finished with scores all released, I decided to post it as my first-ever GitHub repo and share my proud game with other users! 

The project combines a graphical user interface with randomized mine generation, dynamic difficulty configuration, recursive cell revealing, flag management, win/loss detection, and an integrated game timer. Bombs are placed **after** the first click, preventing users from dying on the first click, ensuring that the opening click can never result in an unavoidable loss. I coded this feature after my teacher encountered it during a test run, showing the importance of collaboration in Coding. The name "Retro-Mindsweeper" was created due to its 8-Bit graphics and the fact that I thought the game was called MindSweeper instead of Minesweeper. **Funny, right?**

## Features

* **Three difficulty levels**

  * Easy Mode — 9 × 9 board with 10 mines
  * Medium — 12 × 12 board with 35 mines
  * Hard — 12 × 12 board with 99 mines
* Graphical interface built with Tkinter
* Integrated game timer
* Right-click flag placement and removal
* First-click safety
* Automatic revealing of connected empty cells
* Win and loss detection
* Dynamic mine counter
* Reset and replay functionality
* Built-in instructions and configuration screens

## Screenshots
Here are some screenshots from the output of my code! 

### Main Menu

![Main Menu](screenshots/Main-Menu)

### Gameplay

![Gameplay](screenshots/Gameplay)

### Difficulty Selection

![Difficulty Selection](screenshots/Difficulty-Menu)

### Win Screen
This image is slightly different, as I had to change some of the code and run it on different software, as my original platform broke and I needed to code it again.

![Win Screen](screenshots/Win-Screen)

### Loss Screen

![Loss Screen](screenshots/Loss-Screen)

## Gameplay Explanation

The objective is to reveal every non-mine cell without detonating a mine.

### Controls

| Action              | Input        |
| ------------------- | ------------ |
| Reveal a cell       | Left-click   |
| Place/remove a flag | Right-click  |
| Reset the board     | Reset button |
| Return to menu      | Menu button  |

Numbers displayed on revealed cells indicate the number of mines present in the surrounding eight cells.

## Difficulty Configuration

| Difficulty | Board Dimensions | Mines |
| ---------- | ---------------: | ----: |
| Easy       |            9 × 9 |    10 |
| Medium     |          12 × 12 |    35 |
| Hard       |          12 × 12 |    99 |

Difficulty settings are stored in a dictionary, allowing the board dimensions and mine count to be updated dynamically when the player changes difficulty.

## Technical Implementation

### Board Representation

The game represents the board as a two-dimensional list. Each cell contains a dictionary storing its current state, including:

* Mine status
* Revealed status
* Flag status
* Number of adjacent mines

This structure allows the game to independently track and update each cell.

### Mine Generation

(I stated this at the start, but in case you skipped over the description)

Mines are generated randomly after the player's first move rather than when the board is initially created.

The first selected cell is excluded from mine placement, guaranteeing that the player's opening move is safe.

### Recursive Cell Revealing

When a cell contains no adjacent mines, the game recursively evaluates its neighbouring cells and reveals additional safe cells.

This provides the familiar Minesweeper behaviour where connected empty areas are revealed automatically.

### Game State Management

Several variables maintain the current state of the game, including whether the game has started, whether it has ended, the number of remaining flags, and the timer state.

### Event Handling

Tkinter event bindings connect mouse interactions to the game's logic. Left-clicks reveal cells, while right-clicks manage flags.

## Technologies

* **Python**
* **Tkinter (Import)**
* `random` — randomized mine placement
* `time` — game timing
You can import most of these as done in the code.

## Installation & Execution

### Requirements

* Any type of coding software or service that uses Python
* Tkinter

The project does not require any third-party Python packages.

### Running the Game

Clone the repository:

```bash
git clone (https://github.com/ohNwghtEG/retro-mindsweeper)
```

Navigate to the project directory:

```bash
cd Retro-Minesweeper
```

Run the application:

```bash
python main.py
```

The Tkinter application will launch in a separate desktop window.

## Project Structure

```text
Retro-Minesweeper/
│
├── main.py
├── README.md
└── screenshots/
    ├── main-menu.png
    ├── gameplay.png
    ├── options.png
    └── win-screen.png
```

## Development & Testing

This project was developed independently using Python and Tkinter.

I consulted online tutorials to learn Tkinter concepts and programming techniques, but did not directly reproduce code from those tutorials.

The game was also tested with peers to identify bugs, usability issues, and potential improvements. Feedback from testing was used to refine the game's functionality through debugging and iterative development.

## Key Learning Outcomes

This is my first **PLAYABLE** game, as I am still relatively new to coding. Here are the most important skills I've learned through coding "Retro-Mindsweeper":

* GUI development
* Event-driven programming
* Recursive algorithms
* Two-dimensional data structures
* Dictionaries and nested data structures
* Randomized algorithms
* State management
* User input handling
* Debugging and iterative development

## Future Development

Potential improvements include:

* New game modes (for example, infinite mode, where you try to get the highest score possible or story mode, where there is an actual plot and lore. Even a mode where the player has lives and etc!)
* Multiplayer with competition (for example, you and a friend compete for the highest score or fastest time)
* Persistent high scores and fastest completion times (leaderboards)
* Additional board configurations (adding more buttons or something)
* Custom difficulty settings (Players can choose the exact number of bombs placed, tiles, time, etc.)
* Sound effects and visual feedback (for when you click a tile, explode a bomb, or even main menu music)
* Additional themes (different backgrounds and better visuals)
* Improved accessibility (for mobile users)
* More advanced statistics and performance tracking 

## License

This project was developed as a personal/student programming project. For more information, check the License section in this repo.

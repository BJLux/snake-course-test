# Project: Python Snake Game

A classic arcade-style Snake game implemented in Python using the Pygame library.

## Project Overview
This project provides a functional and interactive Snake game. It features a snake that grows as it eats food, score tracking, collision detection (walls and self), and a game-over screen with restart functionality.

- **Main Technology:** Python 3.12+
- **Graphics Library:** Pygame 2.6.1
- **Architecture:** Monolithic script (`snake.py`) containing initialization, the game loop, event handling, and rendering logic.

## Building and Running

### Prerequisites
- Python 3.6 or later installed on the system.

### Installation
To install the necessary dependencies, run:
```powershell
python -m pip install -r requirements.txt
```

### Running the Game
To start the game, execute:
```powershell
python snake.py
```

### Testing
Currently, the project does not have an automated test suite. Manual verification by running the game is the primary testing method.

## Development Conventions

### Coding Style
- **Naming:** Predominantly uses `snake_case` for variables and constants, though `gameLoop` uses `camelCase`. Future additions should prioritize `snake_case` for consistency with Python (PEP 8) standards.
- **Constants:** Colors and display dimensions are defined as global constants at the top of the file for easy adjustment.
- **Structure:** Logic is encapsulated within a `gameLoop()` function to allow for easy restarts.

### Adding Features
- **Visuals:** Use the predefined color constants or add new ones at the top of `snake.py`.
- **Difficulty:** Adjust `SNAKE_SPEED` to change the game pace.
- **Grid:** The game operates on a 20x20 grid defined by `SNAKE_BLOCK`.

## Key Files
- `snake.py`: The heart of the application containing all game logic.
- `requirements.txt`: Manages the project's external dependencies.
- `README.md`: User-facing documentation for setup and controls.

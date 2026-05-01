# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```powershell
# Install dependencies
python -m pip install -r requirements.txt

# Run the game
python snake.py
```

There is no automated test suite — manual verification by running the game is the primary testing method.

## Architecture

Single-file application (`snake.py`) with a monolithic structure:

- **Global constants** at the top: colors (WHITE, YELLOW, BLACK, RED, GREEN, BLUE), display dimensions (800×600), `SNAKE_BLOCK` (20px grid unit), `SNAKE_SPEED` (5 FPS)
- **Helper render functions:** `show_score()`, `draw_snake()`, `message()`
- **`gameLoop()`** — the entire game lifecycle: input handling, state updates, collision detection, rendering, and restart (recursive call when player presses C)

The game operates on a 20×20 pixel grid across an 800×600 canvas. Three collision types are checked each frame: wall bounds, self-intersection, and food pickup.

## Conventions

- Use `snake_case` for new identifiers (PEP 8). The existing `gameLoop` name is a legacy exception — do not propagate `camelCase`.
- Add new color constants at the top of `snake.py` alongside the existing ones.
- Adjust `SNAKE_SPEED` to change difficulty; adjust `SNAKE_BLOCK` to change grid size (both values affect layout math throughout the file, so change them together).

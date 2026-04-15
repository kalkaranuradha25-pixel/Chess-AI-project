# Chess AI Game

A simple chess game built with Python and Pygame, featuring a playable 1-player mode against an AI opponent.

## Project Structure

- `chess/ChessMain.py` - Main game loop, rendering, and user input handling.
- `chess/ChessEngine.py` - Chess game state, move generation, rules enforcement, and special moves.
- `chess/ChessAI.py` - AI move selection using negamax alpha-beta pruning with board evaluation.
- `chess/images/` - Piece image assets used by the game.
- `requirements.txt` - Python dependencies.

## Features

- Human vs AI chess gameplay
- Standard chess rules including:
  - legal move generation
  - check and checkmate detection
  - stalemate detection
  - castling
  - en passant captures
  - pawn promotion (automatic promotion to Queen)
- Move history panel
- Undo last move with `Z`
- Reset game with `R`

## Requirements

- Python 3.x
- `pygame`

Install dependencies with:

```bash
pip install -r chess/requirements.txt
```

## Running the Game

From the project root, run:

```bash
python chess/ChessMain.py
```

## Controls

- Click a piece to select it.
- Click a destination square to make a move.
- `Z` - undo last move.
- `R` - reset the game.
- Close the window to exit.

## Notes

- The current image loader in `chess/ChessMain.py` uses an absolute path to the piece assets:
  - `C:/Users/Anuradha/Desktop/chess/images/`
- If you move the project or run it from a different folder, update `loadImages()` in `ChessMain.py` so it points to the correct `chess/images/` directory.

## Improvements

Possible future enhancements:

- let the player choose promotion pieces instead of always promoting to Queen
- support human vs human play
- improve AI search depth and move ordering
- add sound effects and richer UI feedback

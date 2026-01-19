# Rebounce

A semi-finished prototype game inspired by Pong, built with Python and Pygame. Navigate a paddle through waves of bouncing balls while managing your health and scoring points.

## Overview

Rebounce is an arcade-style game where you control a paddle in the center of the screen, defending against balls that spawn from both sides. The game features a health system, scoring mechanics, and a dash ability for quick movement.

## Features

- **Dynamic Ball Spawning**: Balls spawn from both left and right sides of the screen every 3 seconds
- **Health System**: Start with 5 health points - lose one when a ball escapes
- **Scoring System**: Gain points by eliminating balls (balls have limited bounces before they disappear)
- **Dash Mechanic**: Use Shift or Space while moving to dash at 2x speed with visual trail effects
- **Visual Effects**: Fade-out trails for dash movements and ball death animations
- **Sound Effects**: Audio feedback for bounces, dashes, and ball eliminations
- **FPS Counter**: Toggle FPS display with 'Q' key
- **Fullscreen Mode**: Toggle fullscreen with 'F' key
- **Delta Time**: Frame-rate independent movement for consistent gameplay

## Installation

### Prerequisites

- Python 3.11 or higher
- pip (Python package manager)

### Setup

1. Clone or download this repository
2. Install the required dependencies:

```bash
pip install pygame
```

Or if using a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install pygame
```

## How to Run

Simply execute the main Python file:

```bash
python main.py
```

## Controls

| Key | Action |
|-----|--------|
| `W` or `↑` | Move paddle up |
| `S` or `↓` | Move paddle down |
| `Shift` or `Space` | Dash (while moving) |
| `F` | Toggle fullscreen mode |
| `Q` | Toggle FPS counter |
| `ESC` | Exit game |

## Gameplay

- **Objective**: Survive as long as possible and score as many points as you can
- **Ball Mechanics**: 
  - Balls spawn from random sides and move toward your paddle
  - Each ball has 3-5 bounces before it can be eliminated
  - Balls bounce off walls and your paddle
  - If a ball escapes the screen, you lose 1 health
- **Health**: You start with 5 health points. When health reaches 0, the game ends
- **Scoring**: Eliminate balls by letting them bounce enough times to reduce their life to 0
- **Dash**: Hold Shift or Space while moving to dash, creating a visual trail effect

## Project Structure

```
Rebounce/
├── main.py           # Main game loop and logic
├── framework.py      # Utility functions (delta time, distance calculations)
├── menus.py          # Menu system (currently not integrated)
├── assets/
│   ├── fonts/
│   │   ├── GothamMedium_1.ttf
│   │   └── times new roman.ttf
│   └── sfx/
│       ├── bounce.wav
│       ├── dash.wav
│       ├── dead1.wav
│       └── dead2.wav
└── README.md
```

## Technical Details

- **Framework**: Pygame 2.6.1
- **Target FPS**: 120 FPS
- **Window Size**: 1200x675 (windowed mode)
- **Delta Time**: Frame-rate independent movement calculations
- **Collision Detection**: Rectangle-based collision using Pygame's Rect system

## Configuration

Key game constants can be modified in `main.py`:

- `PONG_SPEED`: Base movement speed (default: 10)
- `PONG_WIDTH` / `PONG_HEIGHT`: Paddle dimensions (default: 25x100)
- `BALL_SIZE`: Ball radius (default: 18)
- `PONG_HEALTH`: Starting health (default: 5)
- `DASH_MULTIPLIER`: Dash speed multiplier (default: 2)
- `FPS`: Target frames per second (default: 120)

## Development Status

⚠️ **Note**: This is a semi-finished prototype. Development has been paused, and some features (like the menu system) are not fully integrated.

## Known Issues / Future Improvements

- Menu system exists but is not integrated into the main game loop
- Game over screen not implemented
- No high score tracking
- Limited visual polish

## Credits

Built with Python and Pygame. Sound effects and fonts included in the assets folder.

## License

This project is provided as-is for educational and personal use.

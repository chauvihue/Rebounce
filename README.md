<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">

<img src="readmeai/assets/logos/purple.svg" width="30%" style="position: relative; top: 0; right: 0;" alt="Project Logo"/>

# <code>❯ rebounce</code>

<em>A pong-inspired arcade game with unique mechanics and dynamic gameplay</em>

<!-- BADGES -->
<!-- local repository, no metadata badges. -->

<img src="https://img.shields.io/badge/Status-WIP-yellow" alt="Work in Progress">
<img src="https://img.shields.io/badge/Python-3.x-3776AB.svg?style=default&logo=Python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/pygame-2.x-3776AB.svg?style=default&logo=python&logoColor=white" alt="pygame">

</div>
<br>

---

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Features](#features)
- [How to Play](#how-to-play)
- [Project Structure](#project-structure)
    - [Project Index](#project-index)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Usage](#usage)
- [Technologies](#technologies)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Overview

⚠️ **Work in Progress**: This project is currently under active development and is NOT accepting contributions, forks, or pull requests at this time. This is a personal learning project.

**rebounce** is a pong-inspired arcade game that puts a unique spin on the classic paddle-and-ball formula. Instead of competing against an opponent, you defend against waves of bouncing balls that spawn from both sides of the screen. Each ball has a limited number of bounces (3-5) before it naturally expires, creating a dynamic and fast-paced gameplay experience.

The core gameplay loop revolves around defending your paddle against incoming balls while managing your health and scoring points. The game features a dash movement mechanic that allows for quick repositioning with a visual trail effect, adding both strategic depth and visual flair. With delta-time based physics ensuring consistent gameplay across different frame rates, fullscreen support, and an FPS counter toggle, rebounce offers a polished arcade experience built with pygame.

---

## Features

- **Dynamic Ball Spawning System**: Balls spawn from both left and right sides with randomized trajectories, creating unpredictable and challenging gameplay
- **Dash Movement Mechanic**: Quick dash ability (SPACE/SHIFT) with visual trail effects that fade over time, allowing for rapid repositioning
- **Health and Scoring System**: Start with 5 health points; lose health when balls escape past your paddle, and score points when balls expire naturally after their maximum bounces
- **Ball Life System**: Each ball bounces 3-5 times before disappearing, adding strategic depth as you track which balls are about to expire
- **Fullscreen Mode Support**: Toggle between windowed and fullscreen modes with the F key
- **FPS Counter Toggle**: Monitor performance with an optional FPS counter (Q key)
- **Delta-Time Based Physics**: Frame-rate independent physics ensure consistent gameplay regardless of system performance

---

## How to Play

### Controls

- **W / ↑ Arrow**: Move paddle up
- **S / ↓ Arrow**: Move paddle down
- **SPACE / SHIFT**: Dash (faster movement with cooldown, creates visual trail)
- **F**: Toggle fullscreen mode
- **Q**: Toggle FPS counter
- **ESC**: Exit game

### Objective

Defend your paddle against balls bouncing from both sides of the screen. Each ball has a limited lifespan of 3-5 bounces before it naturally disappears. Your goal is to prevent balls from escaping past your paddle while maximizing your score.

### Health System

You start with **5 health points**. Each time a ball escapes past your paddle (goes off-screen on your side), you lose 1 health point. When your health reaches 0, all balls are cleared and the game effectively ends.

### Scoring

You earn points when balls expire naturally after reaching their maximum bounce count. This encourages strategic play where you can let balls bounce out their lives for points, but risk them escaping and losing health.

---

```sh
└── /

    ├── assets
    │   ├── fonts
    │   └── sfx
    ├── framework.py
    ├── main.py
    ├── menus.py
    └── README.md

```

### Project Index

<details open>
	<summary><b><code>/</code></b></summary>
	<!-- __root__ Submodule -->
	<details>
		<summary><b>__root__</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ __root__</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/framework.py'>framework.py</a></b></td>
					<td style='padding: 8px;'>Provides utility functions for distance calculation and delta-time management for frame-rate independent physics</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/main.py'>main.py</a></b></td>
					<td style='padding: 8px;'>- This code initializes the game environment, handles user input, updates game state, and renders graphics<br>- It coordinates all game components, including physics, collision detection, and rendering<br>- The main loop processes events, updates game objects, and ensures smooth gameplay<br>- This central controller integrates with other modules for rendering, input handling, and game logic.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/menus.py'>menus.py</a></b></td>
					<td style='padding: 8px;'>Implements pause menu system with semi-transparent overlay and input handling</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/thinking.txt'>thinking.txt</a></b></td>
					<td style='padding: 8px;'>- Manage dash animations by tracking positions and applying fade effects<br>- This approach efficiently handles the visual transition during dashes, ensuring smooth rendering and maintaining performance within the games rendering architecture.</td>
				</tr>
			</table>
		</blockquote>
	</details>
</details>

---

## Getting Started

### Prerequisites

This project requires the following dependencies:

- **Programming Language:** Python 3.x
- **Game Engine:** pygame library
- **Assets Structure:** The project requires an `assets` folder with:
  - `fonts/` subdirectory containing font files
  - `sfx/` subdirectory containing sound effect files

### Installation

1. **Clone the repository:**

    ```sh
    ❯ git clone <repository-url>
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd Rebounce
    ```

3. **Install the dependencies:**

    ```sh
    ❯ pip install pygame
    ```

### Usage

Run the game with:

```sh
❯ python main.py
```

---

## Technologies

This project is built using:

- **pygame**: Game engine and multimedia library for Python
- **Python Standard Libraries**: 
  - `time`: For delta-time calculations and timing
  - `random`: For randomized ball trajectories and spawn positions
  - `sys`: For system-level operations and exit handling
  - `os`: For file path operations and asset loading

---

## Roadmap

> **Note**: This is a personal WIP project. The roadmap below is for the author's reference only.

- [X] **`Task 1`**: <strike>Implement basic ball physics and collision detection.</strike>
- [ ] **`Task 2`**: Complete menu system implementation.
- [ ] **`Task 3`**: Add sound effects and visual polish.

---

## Contributing

⚠️ **This project is currently a work-in-progress and is NOT accepting contributions.**

This is a personal learning project. Forks, pull requests, and contributions are not being accepted at this time. Thank you for your understanding!

---

## License

This is a personal/educational project. All rights reserved. This project is for viewing and learning purposes only.

---

## Acknowledgments

- Built with [pygame](https://www.pygame.org/), a cross-platform set of Python modules designed for writing video games
- Inspired by classic arcade games and pong-style mechanics

<div align="right">

[![][back-to-top]](#top)

</div>


[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-151515?style=flat-square


---

# Leecho
# Retro SFML Platformer (Beta 0.02)

A nostalgic window into my early programming days. This is a classic 2D side-scrolling platformer built with C++ and the SFML library circa 2017. It features a hardcoded tilemap, custom sprite sheet animations, collision handling, and a vintage main menu.

## 📜 Backstory
This repository contains one of my very first codebases written 9 years ago. Looking back, it perfectly captures the raw excitement of early game development: managing delta time manually, dealing with hardcoded magic numbers, and implementing structural logic within single files. It stands as a baseline milestone of where my software engineering journey began.

## 🛠️ Tech Stack & Features
* **Language:** C++
* **Graphics Library:** SFML (Simple and Fast Multimedia Library)
* **Architecture:** Monolithic single-file project with a primitive `player` class.
* **Tilemap System:** An ASCII-based custom grid (`TileMap[20][160]`) parsing walls (`w`) and boundaries (`B`).
* **Camera Movement:** A continuous horizontal and vertical camera lerp based on `offsetX` and `offsetY` tracking the player's coordinates.

## 🎮 Gameplay & Controls
You control a custom character (using Sonic sprite-sheet layouts) moving through a retro map.

* **Left / Right Arrow Keys:** Move horizontally (flips the sprite orientation dynamically via negative texture rectangle bounds).
* **Up Arrow Key:** Jump (enabled only when the `onGround` structural check is verified).

## 🗂️ Project Structure Quirks (A Trip Down Memory Lane)
* **The "Wild" Menu Logic:** Includes an explicit screen-clear color comment (`фон ебанутого меню`) and hardcoded bounding boxes for custom UI mouse-hover events.
* **Hardcoded Collision Matrix:** A nested double loop checks bounding boxes against specific ASCII characters (`B`, `w`, `q`, `e`, `r`) scaled by a hardcoded factor of 32.
* **Framerate-Independent Movement:** Early attempts at delta-time scaling using `clock.getElapsedTime().asMicroseconds() / 300`.

## 🚀 How It Ran
To compile and run this artifact, you needed the SFML development binaries linked to your compiler environment (e.g., Visual Studio or GCC).

```bash
# Compilation example via g++
g++ -c Code.cpp
g++ Code.o -o sfml-app -lsfml-graphics -lsfml-window -lsfml-system
```
Required Assets
The game expected the following local directory setup to fetch texture sheets:

image/sonic.png — Player animation frames (Walk, Idle, Jump).

image/map.png — Environment tileset.

image/newgame.png, image/exit.png, image/k.png — Main menu UI components.

"Keep moving forward, but never forget the code that compiled your foundations."

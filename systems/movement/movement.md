# Movement System

This document explains the logic behind the player's movement between different game screens.

## 1. Concept

The game is composed of multiple, distinct scenes or "screens." The player can move between these screens to explore the world. Each screen is a self-contained shooting gallery with its own unique background and set of enemies.

## 2. Player Controls

Movement is initiated in two ways:

-   **On-Screen Arrows**: The player can click arrow buttons located at the edges of the screen (top, bottom, left, right) to move to the adjacent screen in that direction.
-   **Keyboard Arrows**: The player can use the arrow keys on the keyboard as an alternative to the on-screen buttons.

## 3. State Persistence

When the player moves from one screen to another, key aspects of their state are preserved. This ensures a seamless transition and continuous experience. The following data is carried over:

-   **Snapshots**: The history of the player's last five captured images remains intact.
-   **Player Position**: The player character's coordinates on the screen are maintained.
-   **Crosshair Position**: The position of the player's aiming crosshair is also kept, so the player doesn't have to constantly readjust their aim after moving to a new screen.

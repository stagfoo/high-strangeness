# Battle System Logic

This document explains the core mechanics of the battle screen.

## 1. The Game Concept

The battle screen is a simple shooting gallery game. The player controls a targeting crosshair to aim at moving enemies. The objective is to "hit" the targets, which in this game, means taking a photo of them.

## 2. On-Screen Elements

-   **Game World**: The primary area where all action takes place.
-   **Player Character**: A static character image positioned near the bottom of the screen.
-   **Enemies**: Simple, rectangular enemies that move around the screen.
-   **Layered Depth (Z-Index)**: The game world is not flat; it's composed of multiple layers (e.g., foreground, midground, background). Enemies and environmental objects can be placed on these different layers.
-   **Targeting Crosshair**: The player's aiming reticle.
-   **Spotlight Effect**: The area around the crosshair is brightly lit, while the rest of the screen is darkened.
- **Movement Arrows**: Buttons for moving to another screen.

## 3. Player Controls

-   **Aiming**: The player moves the crosshair using a dedicated control area or the mouse.
-   **Shooting (Capturing)**: The player takes a photo by tapping the "SHOOT" button or pressing the `Space` bar.
- **Movement**: The player uses arrow keys or on-screen buttons to move between screens.

## 4. Core Mechanics

-   **Enemy Movement**: Enemies move in predefined patrol patterns specific to each screen.
-   **Shooting and Hit Detection**: When the player shoots, the game checks if an enemy is within the crosshair. A successful "hit" is a successful photograph.
-   **Capture Feature**: Every time the player shoots, a snapshot of the crosshair area is taken. These images are stored temporarily. The number of photos you can take is limited by your camera's capacity.
- **Fear Mechanic**: When the player's crosshair is over an enemy, their health bar will slowly decrease.

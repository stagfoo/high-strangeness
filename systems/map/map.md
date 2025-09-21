# World Map System (Level Movement)

This document explains the high-level structure of the game world and how the player navigates it.

## 1. Concept

The game world is not a single, continuous area, but is instead divided into a grid of individual, interconnected "screens" or "scenes." Each screen represents a distinct location in the world.

## 2. Structure

-   **Grid-Based Layout**: The screens are arranged in a logical grid. A screen can have connections to adjacent screens to its north, south, east, and west.

-   **Screen Types**: There are two primary types of screens:
    -   **Battle Screens**: The most common type of screen. These are the hostile shooting galleries where the player finds and photographs enemies.
    -   **Hub Screens**: Special, non-hostile locations that provide services. The primary hub is the **Trailer**.

-   **The Trailer (Hub)**: This is the player's home base. It is a unique, safe location on the map. From the trailer, the player can access the **Blog System** to upload photos and earn donations. It is the central point of the game's progression loop.

## 3. Navigation

The player moves from one screen to the next using the dedicated movement controls. The goal is often to explore the battle screens, fill the camera with photos, and then navigate back to the Trailer hub to continue the progression cycle.
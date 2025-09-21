# Enemy Patrol System (Battle Movement)

This document explains how enemies move within a single battle screen. This can be thought of as "Battle Movement," as it defines the motion that happens during the shooting gallery gameplay.

## 1. Concept

Instead of being static targets, enemies within each screen are dynamic and move according to predefined patterns. These patterns are now tied to a specific layer, adding a sense of depth to the gameplay.

## 2. Patrol Patterns

-   **Screen-Specific Patterns**: Each screen in the world map has its own unique set of enemy patrol patterns. When the player enters a new screen, the enemies on that screen will behave differently from the enemies on the previous one.

-   **Layer-Based Patrols**: A patrol pattern now also includes a layer attribute (e.g., foreground, midground, or background). An enemy's movement is tied to its assigned layer. This has several implications:
    -   **Visuals**: Enemies on background layers might appear smaller or move more slowly than those on foreground layers to simulate distance.
    -   **Gameplay**: An enemy's path might take it behind environmental objects on a closer layer, temporarily obscuring it from the player's view.
    -   **Complexity**: This allows for more intricate level design where the player must pay attention to multiple depths of the battlefield.

-   **Types of Movement**: The system supports various types of movement patterns, including:
    -   **Simple Linear Patrols**: An enemy moves in a straight line (horizontally or vertically) until it reaches a boundary, at which point it reverses direction.
    -   **Complex Paths**: Future patterns could involve enemies moving in more complex paths, such as squares, circles, or zig-zags.

## 3. Implementation

The movement of each enemy is independent. For a given screen, the system will define the starting position, path, speed, and layer for each enemy that appears. This ensures that the behavior of enemies is consistent every time a player visits that screen.
# Game Objective System

This document explains the core objectives of the game, including hit consequences, scoring, and win/loss conditions.

## 1. Concept

While the core gameplay is a shooting gallery, this system defines the purpose and goal of that activity. It answers the question: "What happens when an enemy is successfully hit?"

## 2. Hit Consequences

When the player successfully hits an enemy (as determined by the Battle System's hit detection), one or more of the following should occur:

-   **Enemy Defeat**: The enemy is considered "defeated" and is removed from the battle screen for the current session.
-   **Score Award**: The player is awarded points for each successful hit. The number of points could vary depending on the type of enemy or the difficulty of the shot (e.g., distance, speed).

## 3. Level Objective

Each screen or level within the game world will have a specific objective the player needs to complete. Examples include:

-   **Score Target**: The player must reach a certain score threshold.
-   **Timed Challenge**: The player must defeat a certain number of enemies within a time limit.

## 4. Win/Loss Conditions

-   **Winning**: A player "wins" a level by completing its specific objective. Upon winning, they might be rewarded with access to a new area on the world map or a new item for their inventory.
-   **Losing**: A player "loses" a level if a failure condition is met. The most direct failure condition is the player's health (as defined by the Fear Mechanic) dropping to zero.

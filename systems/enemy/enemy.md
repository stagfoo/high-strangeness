# Enemy Definition System

This document explains how different types of enemies (or paranormal entities) are defined and managed in the game.

## 1. Concept

To create a varied and engaging world, the game needs a system for defining a database of unique enemies. Each enemy type has a set of properties that determines its appearance, behavior, and value to the player.

## 2. Enemy Properties

Each enemy type in the game is defined by a collection of properties, such as:

-   **ID**: A unique identifier for the enemy type (e.g., `red_duck`, `blue_blob`).
-   **Name**: The common name of the entity (e.g., "Red Duck," "Blue Blob").
-   **Appearance**: A reference to the image or animation used to render the enemy on the screen.
-   **Behavior**: Defines which patrol patterns the enemy can use. Some enemies might only move in straight lines, while others might have complex, erratic movements.
-   **Rarity**: A classification of how common the enemy is (e.g., Common, Uncommon, Rare). This is a key factor in determining its value.
-   **Base Value**: A base score or donation value for a standard photograph of this enemy.

## 3. Example Definition

An enemy could be defined in a data structure like this:

```json
{
  "id": "sky_serpent",
  "name": "Sky Serpent",
  "appearance": "path/to/serpent.png",
  "behavior": ["sky_patrol_fast", "sky_patrol_slow"],
  "rarity": "Rare",
  "base_value": 500
}
```

## 4. Integration

-   **World Map System**: The world map will use these enemy definitions to populate each battle screen with specific types of entities.
-   **Photo Scoring System**: The `rarity` and `base_value` properties are used by the photo scoring system to calculate the final donation amount for a picture.

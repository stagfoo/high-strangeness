# Inventory & Equipment System

This document explains the core logic of the player's inventory and equipment.

## 1. Concept

The inventory is a user interface that allows the player to manage items and equipment they have collected or purchased. It provides a visual representation of the items, along with details and the ability to interact with them.

## 2. UI Layout

The inventory screen is divided into several key areas:

-   **Inventory Grid**: Displays all consumable items the player possesses.
-   **Equipment Slots**: Dedicated slots for equippable items like the Camera.
-   **Item View**: A detailed view of the currently selected item or piece of equipment, showing a description and its properties.

## 3. Core Mechanics

-   **Data Management**: The inventory is managed by a list of all the items the player has. Each item has properties like its name, description, and quantity.
-   **State Tracking**: The system keeps track of which item is currently selected by the player.
-   **Dynamic Updates**: The UI instantly updates to reflect any changes in the inventory.

## 4. Equipment

A key part of the inventory is the **Equipment** system. Unlike consumable items, equipment provides the player with core abilities and can be upgraded.

-   **The Camera**: The primary piece of equipment. The camera is an item in the inventory with specific properties, such as:
    -   **Capacity**: The maximum number of photos it can store. This directly impacts the gameplay loop, as a full camera forces a return to the trailer.
    -   **Quality/Lens**: A property that could affect the clarity of photos, which in turn affects the donations received from the **Blog System**.

-   **Upgrades**: Using currency from the **Blog System**, the player can upgrade their equipment. For example, upgrading the camera could increase its photo capacity or improve its lens quality.

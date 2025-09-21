# State and Saving System

This document explains how the game's state, particularly the player's captured images, is managed and persisted.

## 1. Concept

To maintain player progress and create a continuous experience, the game needs to save certain pieces of data. This allows the player to retain important items or information across game sessions.

## 2. Saved Data

The primary piece of data that is saved is the collection of "snapshots" the player takes with the Capture Feature. This includes the running history of the last five images captured during gameplay.

## 3. Saving Mechanism

The game will use one of two methods to store this data:

-   **Local Storage**: The most likely method, where the snapshot images are stored directly in the user's browser. This is a standard web technology for persisting small amounts of data.
-   **Save File**: Alternatively, the game might save the information to a local file on the user's computer. This would be more common in a downloadable, standalone application rather than a web-based one.

In either case, when the player starts a new game session, the game will check for this saved data and load the snapshots back into the UI, allowing the player to see their previously captured images.

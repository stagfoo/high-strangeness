# Photo Scoring System

This document explains how the game calculates the quality and value of the photos the player takes. This system is the crucial link between the **Battle System** and the **Blog & Donations System**.

## 1. Concept

Not all photos are created equal. To reward skillful play, the game uses a scoring algorithm to evaluate each snapshot. The resulting "quality score" directly determines the amount of donations (currency) the player receives when they upload the photo to their blog.

## 2. Quality Criteria

The final value of a photo is calculated based on a combination of factors:

-   **Base Value**: Each enemy has a base value determined by the **Enemy Definition System** (factoring in its rarity).
-   **Centering Bonus**: A multiplier is applied based on how close the enemy is to the exact center of the photograph. A perfectly centered shot gets the highest bonus.
-   **Clarity Bonus**: A multiplier based on the visual clarity of the enemy. An enemy on a foreground layer will be clearer and receive a higher bonus than one on a background layer that appears smaller or is partially obscured.
-   **Completeness Bonus**: A multiplier that rewards capturing the entire enemy within the frame. A photo that cuts off part of the enemy will receive a lower bonus.
-   **Action Shot Bonus**: A potential multiplier for capturing an enemy during a specific or interesting animation/action (e.g., a rare attack, a unique movement).

## 3. Scoring Algorithm Example

The final donation value could be calculated with a formula like:

`Final Value = (Enemy Base Value) * (Centering Bonus) * (Clarity Bonus) * (Completeness Bonus)`

-   **Example**: A rare enemy with a base value of 500, captured perfectly centered (1.5x bonus), in the foreground (1.2x bonus), and fully in frame (1.1x bonus) would be worth:
    `500 * 1.5 * 1.2 * 1.1 = 990` donations.

## 4. Integration

-   This system runs when the player is in the **Trailer** and chooses to upload photos to their blog.
-   The resulting scores are displayed to the player, providing feedback on their photography skills before the final donation amount is awarded.

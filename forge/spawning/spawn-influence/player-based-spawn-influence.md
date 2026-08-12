---
description: >-
  Explains how player positioning, line-of-sight, and death locations
  dynamically influence spawn weighting.
---

# Player-Based Spawn Influence

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While developers can manually adjust the weighting of spawns using [Spawn Volumes](spawn-volumes.md), player activity on a map provides additional dynamic influence over spawn points.

## Dynamic Spawning Influences

Spawns are constantly being influenced by the players currently active on the map, meaning that even without manual volume adjustments, spawning behavior will shift as players move through an area.

### Positioning Factors

Players' locations in relation to one another affects where spawns occur. Generally, players are more likely to spawn near their teammates and away from enemies. The specific weight values applied by these positioning factors have not been reverse-engineered.

#### Line-of-Sight Mechanics

Player line-of-sight (LoS) functions differently than other positional influences. Rather than applying a set weight to a spawn point, the player's presence within a line-of-sight cone acts as a "hard switch." This mechanism can entirely enable or disable a specific spawn point based on whether it is visible to a player.

## Impact of Player Death

A player's death also leaves a temporary mark on the spawning logic. When a player dies, a weight of `-9.00` is placed on that location. This negative influence persists for 10 seconds before fading out.

***

## Source Data

* Discord thread: [Player-Based Spawn Influence](https://discord.com/channels/220766496635224065/1536620322705510530/1536620322705510530)

#### <mark style="color:green;">Contributors</mark>

Okom
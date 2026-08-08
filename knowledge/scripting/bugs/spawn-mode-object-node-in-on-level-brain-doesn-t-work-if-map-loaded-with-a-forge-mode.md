---
description: >-
  Forwarded message:
---

# Spawn Mode Object Node In On-Level Brain Doesn't Work If Map Loaded With a Forge Mode

In certain scenarios involving custom game modes, the [Spawn Mode Object](../../../scripting/nodes/game-mode/spawn-mode-object.md) node in an on-level `Mode Brain` fails to clone its target object. This issue occurs when the map is loaded as part of a custom Forge mode—specifically variants like a "Minigame" constructed from empty brains—rather than through official matchmaking modes.

## Bug Behavior and Context

When run within these specific custom Forge Modes, objects targeted for spawning are not cloned. Instead, gameplay feedback via the killfeed indicates that the output object is invalid. 

### Scripting Implementation

The issue involves a node graph utilizing `Spawn Mode Object` to clone an on-level reference from within an on-level brain.

<figure><img src="../../../.gitbook/assets/HaloInfinite_EUV8Y6YgUz.webp" alt="Spawn Mode Object Node In On-Level Brain Doesn't Work If Map Loaded With a Forge Mode source image"><figcaption></figcaption></figure>

## Reproduction Steps

There are two documented ways to observe this behavior:

### Method 1: Direct Comparison
1. Load a map using an official mode such as "Arena:Slayer". Mark the ground and verify that the red `Primitive Block` is cloned correctly and provides data in the killfeed.
2. Reload the same map using a custom Forge Mode (such as an Example Minigame Forge Mode). Mark the ground and observe that the object fails to clone, with the killfeed reporting an invalid output object.

### Method 2: Detailed Debug Workflow
1. In Forge Play Mode on an empty canvas, place a `Primitive Block` (with a Spawn Order of 50) and a `Mode Brain` (with a Spawn Order of 5).
2. Implement the node graph using the `Spawn Mode Object` node and confirm it functions correctly in Play Mode by observing its print values.
3. Create a `Mode Prefab` by placing two `Mode Brains` with different Spawn Orders (e.g., 10 and 20) and setting the mode variant to "Minigame".
4. Delete the prefab, save the map, and load it in an official mode like "Arena:Slayer" to verify normal behavior.
5. Load the saved map using your custom Forge Mode; observe that spawning no longer functions as intended.

## Expected Result

The `Spawn Mode Object` node should successfully clone the target object because it maintains a valid reference to the on-level object, regardless of whether the map is loaded via an official mode or a custom Forge Mode.

{% hint style="info" %}
This issue appears localized to scenarios where the active game state is governed by user-defined Forge modes rather than official matchmaking settings.
{% endhint %}

***

## Source Data

* Discord thread: [Spawn Mode Object Node In On-Level Brain Doesn't Work If Map Loaded With a Forge Mode](https://discord.com/channels/220766496635224065/1535589156984725625/1535589156984725625)

#### <mark style="color:green;">Contributors</mark>

Okom
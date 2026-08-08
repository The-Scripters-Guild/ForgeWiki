---
description: >-
  Forwarded message:
---

# Spawn Mode Object Node In On-Level Brain Doesn't Work If Map Loaded With a Forge Mode

<figure><img src="../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Users have reported that the [Spawn Mode Object](../scripting/nodes/game-mode/spawn-mode-object.md) node fails to clone objects when a map is played within a custom game loaded with a Forge Mode, such as a Minigame variant composed of multiple empty Mode Brains. This occurs even when using on-level brains and valid object references.

## Cloning Failures in Custom Forge Modes

When an "on-level" Brain contains a script utilizing the `Spawn Mode Object` node to clone another on-level object, functionality depends heavily on how the map is loaded into play.

### Comparison of Standard and Forge Game Modes

The outcome of cloning operations differs significantly between official game modes and custom modes:

* **Official/Standard Modes:** When loading a map using an official mode (such as "Arena:Slayer"), the `Spawn Mode Object` node works as expected, successfully cloning objects. In these instances, the killfeed provides relevant data regarding the spawned objects.
* **Custom Forge Modes:** When playing via a custom Forge Mode or Minigame variant, the object is not cloned. Although the script may have valid object references that load correctly in other contexts, the resulting output object appears as an "invalid object" within the killfeed.

<figure><img src="../.gitbook/assets/HaloInfinite_JG6yLKlIOM.webp" alt="Spawn Mode Object node setup"><figcaption></figcaption></figure>

{% hint style="info" %}
Even when object references are valid and function correctly in standard modes, they may fail to execute the cloning process within custom Forge modes.
{% endhint}

{% endhint %}

Even when object references are valid and function correctly in standard modes, they may fail to execute the cloning process within custom Forge modes.
{% endhint}

## Reproduction Methods

The following scenarios have been identified as methods for reproducing this issue:

### Option 1: Mode-Based Verification
* Load a map using an official mode (e.g., "Arena:Slayer"). Verify that objects, such as Primitive Blocks, clone correctly and report to the killfeed.
* Reload the same map using a custom Forge Mode or Minigame variant to observe the cloning failure.

### Option 2: Void Canvas and Prefab Testing
This method involves testing within the Forge editor before applying the settings to a saved map:
1. In an empty Void canvas, place one Primitive Block (Spawn Order 50) and one Mode Brain (Spawn Order 5).
2. Implement the node graph script and verify it functions correctly in Forge Play Mode.
3. Place two additional Mode Brains with varying Spawn Orders (e.g., 10 and 20).
4. Create a Mode Prefab from these brains, setting the Mode Variant to "Minigame".
5. Delete the Mode Prefab and save the map.
6. Load the map in an official mode like "Arena:Slayer" to confirm correct operation.
7. Load the map using the saved custom Forge Mode to observe the failure of the `Spawn Mode Object` node.

***

## Source Data

* Discord thread: [Spawn Mode Object Node In On-Level Brain Doesn't Work If Map Loaded With a Forge Mode](https://discord.com/channels/220766496635224065/1535589156984725625/1535589156984725625)

#### <mark style="color:green;">Contributors</mark>

Okom
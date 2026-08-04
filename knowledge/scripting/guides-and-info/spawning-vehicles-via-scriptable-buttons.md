---
description: >-
  Learn how to use object references and the Spawn Mode Object node to
  spawn vehicles via scripts, bypassing the limitations of vehicle
  pads.
---

# Spawning Vehicles via Scriptable Buttons

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When designing game modes that rely on button-triggered spawns, developers may encounter difficulties attempting to reference vehicle pads directly within a script brain. This article outlines why this approach is restricted and provides an alternative method for spawning vehicles using object references.

## Constraints of Vehicle Pads
Vehicle pads are classified as [Forge Kit Objects](../../../forge/forge-basics-and-ui/forge-interface/object-browser/forge-kit-objects.md), which means they cannot be referenced within a script brain. Furthermore, even if a reference to a pad could be established in a script, the internal spawning logic of those pads is not accessible via scripting to trigger spawns on command.

## Spawning Vehicles via Object References
The recommended approach for triggering vehicle spawns—such as through a Scriptable Button press—is to use direct vehicle object references combined with the **[Spawn Mode Object](../../../scripting/nodes/game-mode/spawn-mode-object.md)** node. This method allows you to duplicate an existing vehicle instance at a specific location in the level.

### Implementation Workflow
To implement this setup, follow these steps:
* Place the desired vehicle (such as a Wasp) on the map and create a reference for that object within your script.
* Use the **`Spawn Mode Object`** node to handle the duplication logic.
* Feed the vehicle object reference into the spawning node along with a position where the new instance should be created.

{% hint style="info" %}
This method provides more flexibility than pads, as it allows you to spawn vehicles at arbitrary coordinates or via various custom triggers.
{% endhint %}

***

## Source Data

* Discord thread: [Spawning Vehicles via Scriptable Buttons](https://discord.com/channels/220766496635224065/1534086222018908192/1534086222018908192)

#### <mark style="color:green;">Contributors</mark>

Alex\
Guild Archivist\
Okom
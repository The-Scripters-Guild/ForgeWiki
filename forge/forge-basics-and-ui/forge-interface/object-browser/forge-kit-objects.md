---
description: >-
  Dynamic Forge objects used for item spawning or map event logic via
  adjustable properties.
---

# Forge Kit Objects

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Forge Kit objects are dynamic entities within Forge that feature various adjustable properties. They are primarily used to spawn items on a map or provide specific gameplay functionality beyond the physical presence of the object itself.

### Item Spawners
* Classic Equipment Spawn
* Classic Grenade Spawn
* Equipment Dispenser
* Equipment Pod
* Grenade Dispenser
* Power Equipment Pad
* Classic Vehicle Spawn
* Vehicle Pad
* Weapon Pad
* Weapon Pod
* Weapon Rack
* Weapon Trunk

### Match Flow Objects
* Map Intro Camera
* Team Intro Arrow Front
* Team Intro Line Left
* Team Intro Line Right
* Winning Team Outro

## Referencing Forge Kit objects in scripts

Forge Kit objects cannot be referenced directly in node graph scripts like standard dynamic objects. Attempting to reference one of these objects using an `Object Reference` node will result in the error: "Cannot reference kit object".

To use a Forge Kit object within a script, you must find and store a reference to it during gameplay through one of the following methods:

* **Label:** Add an available label (e.g., "Dodgeball Overtime Zone") to the Forge Kit object and then use the [Get Objects By Label](../../../../scripting/nodes/objects/get-objects-by-label.md) node to find all objects with that specific label.
* **Area Monitor:** Place a different object with an area monitor boundary near the kit object, then use the [Get Objects In Area Monitor](../../../../scripting/nodes/objects/get-objects-in-area-monitor.md) node to detect it.

Note that attempting to reference these objects by altering their Spawn Order and finding objects with matching Spawn Order values is not a supported method for obtaining references to Forge Kit objects via scripting.

***

## Source Data

* Discord thread: [Forge Kit Objects](https://discord.com/channels/220766496635224065/1534009211808387215/1534009211808387215)

#### <mark style="color:green;">Contributors</mark>

Okom

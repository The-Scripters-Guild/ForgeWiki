---
description: >-
  Learn how to generate equipment object references within Mode
  Scripting to spawn equipment at arbitrary positions on any map.
---

# Creating an Equipment Object Reference with Mode Scripting

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

In Mode Scripting, creating an equipment object reference is necessary for spawning equipment at specific coordinates across different maps. Because standard kit objects, such as Classic Equipment Spawns, cannot have an object reference held within a Mode Brain, developers must use specific workarounds to generate these references dynamically.

## Challenges with Equipment References

Attempting to manage equipment via standard means often presents limitations depending on the desired implementation.

### Limitations of Standard Methods

Several common approaches to equipment management are insufficient for creating dynamic object references in a mode:

* **Classic Equipment Spawns**: These are kit objects and cannot be provided an object reference in a Mode Brain.
* **Clones**: Player clones are unable to pick up equipment.
* **Bots**: While bots can pick up equipment, they do not drop it, making it impossible to generate a dropped object reference.
* **Player Death Workarounds**: One method involves granting equipment to a player and then killing them to detect the dropped object using `Get All Objects With Spawn Order` (0). However, this is unideal for multi-round modes or modes utilizing Team Revive options, as it requires player death and necessitates complex systems to return players to their original spawn positions.

## The Forceful Drop Method

A more effective solution for generating an equipment object reference is to forcefully drop equipment that has been granted to a player. This method is viable on most maps because most core map setups include at least one equipment spawner, and the method requires an existing equipment on-level.

### Implementation Workflow

To implement this, you must first obtain an existing equipment object reference to trigger the drop function.

1. Use a `Get All Objects With Spawn Order` (0) loop.
2. Filter the objects to identify one that is of an equipment type.
3. Once an equipment reference is found, use it to fire the function that forcefully drops the player's currently granted equipment.

{% hint style="success" %}
Most maps with a standard core setup feature at least one equipment spawner, which can be used to find the initial reference needed for this process.
{% endhint %}

Demo map with a working script: [Spawn Equipment at Position demo](https://www.halowaypoint.com/halo-infinite/ugc/maps/baf55080-bfd8-49b2-a61a-384db38dc547)

#### Side Effects and Considerations

The primary gameplay-facing side effect of this method is that players may hear the sound of equipment being picked up during the initial intro cameras. This occurs when the system identifies and interacts with the existing equipment reference.

***

## Source Data

* Discord thread: [Creating an Equipment Object Reference with Mode Scripting](https://discord.com/channels/220766496635224065/1478308233667022889/1478308233667022889)

#### <mark style="color:green;">Contributors</mark>

Okom

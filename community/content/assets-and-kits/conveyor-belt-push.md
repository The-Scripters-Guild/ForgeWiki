---
description: >-
  Methods for creating conveyor belt movement that interacts with
  players and physics objects.
---

# Conveyor Belt Push

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Creating conveyor belt movement that effectively interacts with players and physics objects can be difficult, as standard translation methods may not provide the necessary physical interaction required for gameplay.

## Implementation Methods

### Translation and Position Nodes

The [Translate Object To Point](../../../scripting/nodes/objects-transform/translate-object-to-point.md) node can be used to move objects, though players cannot walk against the direction of movement or jump out of the affected area. Additionally, all objects within the area monitor are subject to this movement. To prevent non-player objects from being moved, a [Get Is Player](../../../scripting/nodes/players/get-is-player.md) node can be used to verify the identity of objects within the area monitor.

<figure><img src="../../../.gitbook/assets/image-7adc.webp" alt="Node graph"><figcaption><p>The node graph displays logic for moving objects.</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-5754.webp" alt="Node graph"><figcaption><p>This node graph shows an alternative setup for object positioning.</p></figcaption></figure>

Alternatively, moving both the conveyor belt and the player simultaneously using `Set Position` can create an illusion of continuous movement. However, `Set Position` functions as a teleportation rather than a continuous translation over time.

## Physics-based Conveyor Belts

Using the normal physics option on a conveyor belt allows for native physics interactions, such as moving players or physics crates placed on the surface.

<figure><img src="../../../.gitbook/assets/image-f609.webp" alt="Crates on a conveyor belt"><figcaption><p>Physics crates move along the surface of a conveyor belt.</p></figcaption></figure>

This method introduces specific movement dynamics:
* Players run faster when moving in the same direction as the belt.
* Players run slower when moving against the direction of the belt.
* Stationary players being moved by the belt might not appear on radar.

{% hint style="warning" %}
Spawning multiple physics objects closely together in a constrained space may lead to instability; spawning objects individually and moving them one at a time can result in more reliable behavior.
{% endhint %}

***

## Source Data

* Discord thread: [Conveyor Belt Push](https://discord.com/channels/220766496635224065/1048495100042416218/1048495100042416218)

#### <mark style="color:green;">Contributors</mark>

Koma\
TheProgrammer163\
Okom\
green
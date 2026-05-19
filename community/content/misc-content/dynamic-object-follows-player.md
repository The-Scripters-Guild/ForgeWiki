---
description: >-
  Learn how to create a dynamic chasing mechanic by applying constant
  velocity to an object towards a player using a continuous loop.
---

# Dynamic object follows player?

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This technique allows an object, such as a Fusion Coil, to track and move toward a player as they enter a designated area. By applying constant velocity in a continuous loop, the object can maintain a pursuit regardless of whether the player is standing still or running.

## Calculating Direction and Velocity

To make an object move toward a player, you must determine the direction of travel and apply it as a velocity. This is achieved by calculating the vector between the object and the player.

### Directional Math

The direction is found by taking the player's position and the object's position and feeding them into the [Subtract Vectors](../../../scripting/nodes/math/subtract-vectors.md) node. The resulting output is a vector pointing from the object toward the player.

To control the speed of the pursuit, use the [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node on this directional output. Adjusting the scalar value in the `Scale Vector` node determines how fast the object moves toward the target. Once the vector is scaled, it can be applied to the object using a velocity node.

{% hint style="warning" %}
Using high velocities with objects like Fusion Coils can cause them to frequently collide with floors or walls, potentially causing them to blow up during pursuit.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Screenshot_2026-05-16_194845.webp" alt="Cover image"><figcaption><p>The initial script attempt results in the coil frequently colliding with the floor.</p></figcaption></figure>

{% file src="../../../.gitbook/assets/51626-testingresult.mp4" %}
The Fusion Coil struggles to maintain stability while moving towards the player.
{% endfile %}

### Movement Behavior and Limitations

While this method provides a functional chase mechanic, there are specific behaviors to keep in mind:

* **Target Origin:** Objects will track the player's feet, as that is where the player's position originates from.
* **Airborne Tracking:** The object will continue to follow the player even if they are airborne. To prevent this, you can implement a condition using the [Get Is Airborne](../../../scripting/nodes/units/get-is-airborne.md) node.
* **Target Selection:** Simple implementations may only target the first player detected in an area's player list. A more advanced system would involve calculating distances to all players in the zone to ensure the object pursues the closest target.

## Implementing a Continuous Tracking Loop

Because velocity must be constantly applied to maintain a pursuit, a "heartbeat" script is required to run the logic repeatedly.

### The Heartbeat Method

One method to create this loop is using the [Every N Seconds](../../../scripting/nodes/events-custom/every-n-seconds.md) node within `Events Custom`. For a responsive chase, a frequency of every 0.10 seconds is often used. 

To ensure the loop only runs when necessary, you can manage players within an [Object List](../../../scripting/nodes/variables-basic/object-list.md):
1. [Add](../../../scripting/nodes/math/add.md) players to an `Object List` when they enter a `Generic Zone`.
2. Remove players from the list when they exit the zone.
3. Use the [Get List Size](../../../scripting/nodes/objects/get-list-size.md) node combined with [Branch](../../../scripting/nodes/logic/branch.md) and `Comparison` nodes to check if the list size is greater than 0.
4. If players are present, execute the chase logic for the players in the list.

Alternatively, an `Object Scoped Boolean Variable` can be set to true when a player enters the area and false when they exit, which the loop can check before running the movement scripts.

{% hint style="info" %}
Using an `Object List` to track players in a zone allows the script to scale more easily for multi-player environments.
{% endhint %}

<figure><img src="../../../.gitbook/assets/object-follow-player-script.webp" alt="Cover image"><figcaption><p>This script uses a heartbeat loop to move objects toward the first detected player in a zone.</p></figcaption></figure>

{% file src="../../../.gitbook/assets/obj-follow-player-demo.mp4" %}
The object successfully tracks and follows the player's movement through the area.
{% endfile %}

***

## Source Data

* Discord thread: [Dynamic object follows player?](https://discord.com/channels/220766496635224065/1505172135445008424/1505172135445008424)

#### <mark style="color:green;">Contributors</mark>

What's The Password?\
Okom\
AddiCt3d 2CHa0s
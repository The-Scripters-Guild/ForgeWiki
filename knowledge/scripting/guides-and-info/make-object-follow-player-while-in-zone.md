---
description: >-
  Learn how to make an object continuously track and move towards a
  player when they enter a specific zone using velocity and looping
  logic.
---

# Make Object Follow Player While in Zone

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This technique allows objects, such as Fusion Coils, to actively pursue players within a designated area. By calculating a direction vector and applying it as a constant velocity, the object can move toward the player's position as long as they remain within the zone.

## Pursuit Movement Logic

To move an object toward a target, you must calculate a vector that represents the direction from the object to the player.

### Calculating Direction and Velocity

This is achieved by retrieving the position of both the object and the player and feeding them into a [Subtract Vectors](../../../scripting/nodes/math/subtract-vectors.md) node. The resulting output is a vector indicating the direction the object should travel to reach the player.

To apply this movement, this vector is used to set the object's velocity. The speed of the pursuit can be controlled by passing the direction vector through a [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node. Adjusting the scalar value in this node determines how quickly the object moves toward the player.

<figure><img src="../../../.gitbook/assets/Screenshot_2026-05-16_194845.webp" alt="Initial scripting attempt"><figcaption><p>An early implementation of the pursuit logic shows the object attempting to track the player's position.</p></figcaption></figure>

{% file src="../../../.gitbook/assets/51626-testingresult.mp4" %}
A demonstration of the object movement and potential issues with floor collision.
{% endfile %}

## Maintaining the Pursuit Loop

Because velocity must be applied continuously to maintain pursuit, a looping mechanism is required. This loop should only execute while a player is detected within the target area to prevent the object from chasing players outside the intended zone.

### Multi-player Support via Object Lists

A robust way to manage multiple players is to use an [Object List](../../../scripting/nodes/variables-basic/object-list.md) to track who is currently in the zone.

* **Entry/Exit Logic:** [Add](../../../scripting/nodes/math/add.md) players to the `Object List` when they enter the zone and remove them when they exit.
* **The Heartbeat Script:** Use the "[Every N Seconds](../../../scripting/nodes/events-custom/every-n-seconds.md)" node (found in `Events Custom`) to create a "heartbeat" that runs at a frequent interval, such as every 0.1 seconds.
* **Detection:** Within this heartbeat, use [Get List Size](../../../scripting/nodes/objects/get-list-size.md) and a [Branch](../../../scripting/nodes/logic/branch.md) node to check if the list contains any players.
* **Execution:** If the list size is greater than 0, use the [For Each Object](../../../scripting/nodes/logic/for-each-object.md) node to run the pursuit logic for the players in the list.

The following setup demonstrates a heartbeat loop checking for players in a zone to apply continuous velocity.

<figure><img src="../../../.gitbook/assets/object-follow-player-script.webp" alt="Final script layout"><figcaption><p>The completed script uses a heartbeat loop to check for players in a zone and apply velocity.</p></figcaption></figure>

{% file src="../../../.gitbook/assets/obj-follow-player-demo.mp4" %}
A demonstration of the functional tracking script in a live environment.
{% endfile %}

## Implementation Considerations

When implementing this behavior, there are several technical details and potential issues to keep in mind:

* **Player Position Origin:** Objects will follow the player's feet, as the player's position originates from that point.
* **Airborne Tracking:** By default, objects will follow a player even if they are airborne. To prevent this, you can implement a condition using the [Get Is Airborne](../../../scripting/nodes/units/get-is-airborne.md) node.
* **Targeting Limitations:** The simple approach of using the first player detected in the zone list will only target one person. A more advanced system would involve calculating the distance between the object and every player in the list to target the closest one.
* **Collision Risks:** When using objects like Fusion Coils, there is a risk they may explode if they drag against the floor or collide with walls while pursuing a player.

{% hint style="warning" %}
Be cautious when using Fusion Coils for pursuit, as they may trigger explosions due to floor or wall collisions.
{% endhint %}

***

## Source Data

* Discord thread: [Make Object Follow Player While in Zone](https://discord.com/channels/220766496635224065/1505172135445008424/1505172135445008424)

#### <mark style="color:green;">Contributors</mark>

What's The Password?\
Okom\
AddiCt3d 2CHa0s
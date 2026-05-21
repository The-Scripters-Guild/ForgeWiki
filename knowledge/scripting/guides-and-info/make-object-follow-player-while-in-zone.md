---
description: >-
  A method for making objects move toward a player using a constant
  velocity loop while they are within a specific zone.
---

# Make Object Follow Player While in Zone

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This technique allows a specific object, such as a Fusion Coil, to track and move toward a player as long as they remain within a designated area. By applying a continuous velocity in the direction of the player, the object can act as an automated threat or environmental hazard.

## Implementation Logic

To create an object that actively chases a player, the script must continuously calculate the distance and direction between the two entities and apply a movement force.

### Calculating Direction and Velocity

The primary method for movement involves calculating a direction vector. This is achieved by using the [Subtract Vectors](../../../scripting/nodes/math/subtract-vectors.md) node, with the player's position and the object's position as inputs. The resulting vector provides the direction the object needs to travel to reach the player.

* To move the object, apply this direction as a constant velocity.
* The [Scale Vector](../../../scripting/nodes/math/scale-vector.md) value can be adjusted to determine how fast the object moves toward the target.

### Managing the Movement Loop

Because the player is constantly moving, the velocity must be updated frequently to maintain tracking. This can be achieved by creating a "heart beat" script using the [Every N Seconds](../../../scripting/nodes/events-custom/every-n-seconds.md) node within `Events Custom`. A frequent update rate, such as every 0.1 seconds, is recommended for smooth movement.

To ensure the chase only occurs when the player is in the correct area, you can use one of the following methods:

* **[Object List](../../../scripting/nodes/variables-basic/object-list.md) Tracking:** [Add](../../../scripting/nodes/math/add.md) players to an `Object List` when they enter a `Generic Zone` and remove them when they exit. The script can then use the [Get List Size](../../../scripting/nodes/objects/get-list-size.md) node and a [Branch](../../../scripting/nodes/logic/branch.md) to check if the list contains any players. If the list size is greater than 0, the script executes the chase logic for the players in that list.
* **[Boolean](../../../scripting/nodes/variables-basic/boolean.md) Variables:** Set an Object Scoped [`Boolean` Variable](../../../scripting/nodes/variables-advanced/boolean-variable.md) to true when a player enters the area and false when they exit. The loop can then check this variable before applying movement.

<figure><img src="../../../.gitbook/assets/object-follow-player-script.webp" alt="Object follow player script"><figcaption><p>The script utilizes a continuous loop to detect players within a generic zone and apply movement toward them.</p></figcaption></figure>

## Technical Considerations and Limitations

While effective, this implementation has specific behaviors and potential issues that should be addressed during map design.

### Object Stability and Behavior

The way objects interact with the environment and the player's collision can lead to unexpected results.

{% hint style="warning" %}
Objects like Fusion Coils may explode if they drag against the floor or collide with walls while moving at high velocities toward a player.
{% endhint %}

{% file src="../../../.gitbook/assets/51626-testingresult.mp4" %}
This video demonstrates how high-velocity movement can cause objects like Fusion Coils to explode when hitting surfaces.
{% endfile %}

Additionally, the following behaviors are inherent to this method:

* **Player Origin:** Because player position originates from their feet, objects will appear to follow the player's feet.
* **Airborne Tracking:** Objects will track players even if they are airborne. If you wish to prevent this, you can implement a condition using the [Get Is Airborne](../../../scripting/nodes/units/get-is-airborne.md) node.

{% file src="../../../.gitbook/assets/obj-follow-player-demo.mp4" %}
This video shows an object successfully tracking a player as they move through a zone.
{% endfile %}

### Multi-player Support

The simple implementation provided here only targets the first player detected in the zone's player list. This approach is efficient for single-player scenarios or simple hazards but lacks precision in crowded environments. 

A more advanced system for supporting multiple players would require creating an ordered list of distances between each player in the zone and the object, allowing the script to determine which player is the closest and should be followed.

***

## Source Data

* Discord thread: [Make Object Follow Player While in Zone](https://discord.com/channels/220766496635224065/1505172135445008424/1505172135445008424)

#### <mark style="color:green;">Contributors</mark>

What's The Password?\
Okom\
AddiCt3d 2CHa0s 🎮 💻
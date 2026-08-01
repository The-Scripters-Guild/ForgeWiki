---
description: >-
  An investigation into how player line-of-sight cones affect spawn
  blocking mechanics in Halo Infinite.
---

# Good FX

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Spawn blocking in Halo Infinite is influenced by a specific line of sight boundary originating from the player's head, which utilizes large field-of-view cones to determine if an enemy can enter the map at a given spawn point.

## Line of Sight Boundary Properties

Research into map boundaries reveals that the line of sight check extends sideways until angles meet, with a radius/length of 181.26 units (approximately 55.3 meters).

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-55ra.webp" alt="Good FX source image"><figcaption><p>The image shows the boundary layout used to detect spawn blocking on maps.</p></figcaption></figure>

### Cone Dimensions and Shape

This boundary manifests as a large cone originating from the player's head with a diameter of 10480 units and a length of 181.26 units, resulting in an approximate field of view (FOV) of 176 degrees.

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-SSiU.webp" alt="Good FX source image"><figcaption><p>A visualization shows the extremely large cone originating from a player's head.</p></figcaption></figure>

{% file src="../../../.gitbook/assets/los-cone-10480-units.mp4" %}
This video demonstrates how distance to a spawned player is tracked to determine if their spawn is currently being blocked.
{% endfile %}

## Spawn Blocking Mechanics

A player within the boundary radius will block an enemy's spawn, provided they are facing the target spawner within their own 176-degree field of view. If a player is inside this area but looking away from the spawn point, the spawn remains unblocked. Furthermore, any static or dynamic obstruction located between the spawning player's upper torso and the enemy's head will invalidate the line of sight check and allow the spawn to proceed.

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-Vsty.webp" alt="Good FX source image"><figcaption><p>The diagram illustrates the requirements for performing a line of sight spawn blocking check.</p></figcaption></figure>

{% hint style="info" %}
Third-person perspective can be used to manipulate these checks, as the obstruction logic is specifically calculated from the player's head to the spawning player's upper torso.
{% endhint %}

### Positional and Tactical Applications

The massive diameter of the line of sight cone allows for several tactical positioning options:

* **Vertical Coverage:** By aiming straight up or down, a player can position their 10480-unit diameter cone to cover the altitude above or below them across much of the map. This can block spawns that have an unobstructed view of the player at those higher or lower elevations.
* **Sideways Orientation:** Because of the large width of the cone, a player may be able to block a spawn even while facing nearly 90 degrees away from it if the spawn falls within the outer edges of their FOV coverage.

{% file src="../../../.gitbook/assets/los-cone-exploit.mp4" %}
This video shows how a player's large line of sight cone can block enemies even when the observer is not directly facing them.
{% endfile %}

***

## Source Data

* Discord thread: [Player Line of Sight Cone Research](https://discord.com/channels/220766496635224065/1529131373602799626/1529131373602799626)

#### <mark style="color:green;">Contributors</mark>

Okom
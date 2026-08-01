---
description: >-
  Discovering what the line of sight spawn blocking boundary on maps
  is. This weird shape that extends seemingly forever sideways until
  the angles meet.
---

description: Research into the line of sight spawn blocking geometry used in Halo Infinite maps.

# New Title

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Research into player spawning mechanics has identified a specific, massive geometry used for line of sight (LoS) spawn blocking on both Forge and development maps. While initial observations suggested various spherical boundaries, the mechanic is primarily driven by large cones originating from players' heads.

## LoS Spawn Blocking Geometry
Initial testing indicated that the boundary width was roughly 55 meters (181.26 units). Further research confirmed this as part of a much larger conical shape: an extremely wide cone with a massive diameter and specific length limits.

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-55ra.webp" alt="An early visualization showing the horizontal width of the LoS boundary."><figcaption></figcaption></figure>

The confirmed geometry for this boundary includes:
* **Cone Diameter:** 10480 units (providing massive lateral coverage).
* **Field of View (FOV):** Approximately 176°.
* **Effective Length/Radius:** ~181.26 units (~55 meters).

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-IeiE.webp" alt="Showing the curvature of the boundary on its top and bottom sides."><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-u7JM.webp" alt="Observations of how spherical characteristics affect boundary edges."><figcaption></figcaption></figure>

While these boundaries can appear as spheres in certain visual tests, they are actually large cones. The "spherical" effect is largely an artifact caused by players standing at specific distances and angles where their LoS cones overlap with target spawn points or other players.

{% file src="../../../.gitbook/assets/los-cone-10480-units.mp4" %}
A player's massive line of sight cone can block a spawning enemy even when positioned far to the side.
{% endfile %}

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-SSiU.webp" alt="Demonstrating how the LoS cone covers distant spawns based on orientation."><figcaption></figcaption></figure>

## Mechanics and Obstructions
A player can block an enemy's spawn by having their 176° LoS cone intersect with the target spawner or another spawning player, provided several conditions are met:

* **Orientation:** A player must face the direction of the target within their own field of view. If a player is inside this area but facing away from the spawner, the spawn will not be blocked because the cone does not overlap the target.
* **Obstructions and Exploits:** Spawning is invalidated if any static or dynamic object obstructs the line of sight between the observing player's head and the spawning player's upper torso. 

{% hint style="info" %}
Because the obstruction check occurs from the player's head to the enemy's upper torso, third-person perspective can be used as an exploit to manipulate LoS functionality.
{% endhint %}

This behavior remains consistent across both Forge canvas maps and Halo Infinite development (dev) maps.

<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-Vsty.webp" alt="Visualization of the interaction between a player's cone and spawn points."><figcaption></figcaption></figure>
<figure><img src="../../../.gitbook/assets/2026-07-21_HaloInfinite-KtEs.webp" alt="Visual representation of the interplay between player position and spawn blocking."><figcaption></figcaption></figure>

## Tactical Applications
Understanding these boundaries allows for several maneuvers designed to manipulate spawning:

* **Lateral Blocking:** By tilting sideways, players can extend their massive 10480-unit diameter cone towards spawns located further than the standard 181.26-unit radius.
 {% file src="../../../.gitbook/assets/los-cone-exploit.mp4" %}
Aiming up or down can reposition your LoS cone to cover large vertical areas of a map.
{% endfile %}

* **Vertical Coverage:** Aiming directly upward or downward positions the player's massive cone above or below their current altitude. This creates an effective zone that can block any spawns within that vertical plane if they have an unobstructed line of sight to the player’s position.

* **Optimal Spawning:** To increase the chances of successfully spawning at a specific point, players should look directly at the target. This aligns with the shortest part of the boundary and ensures the most direct LoS check is being made.

***

## Source Data

* Discord thread: [Player Line of Sight Cone Research](https://discord.com/channels/220766496635224065/1529131373602799626/1529131373602799626)

#### <mark style="color:green;">Contributors</mark>

Okom
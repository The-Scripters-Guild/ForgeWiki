---
description: >-
  Blockers are invisible cubical objects that have collision, whose
  main purpose is to serve as a way to limit the player's ability to
  move outside the intended gameplay space, or to smooth collision in
---

# Blockers

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Blockers are invisible, cubical objects that possess collision properties. Their primary purpose is to restrict player movement outside of intended gameplay areas or to smooth out collisions on surfaces with uneven geometry, such as stairs.

## Blocker Varieties

### Universal, Team, and Player Blockers
Universal blockers (white) block all players, projectiles, and vehicles. These are frequently used to fix uneven collision within a map; since they also block projectiles, they can be used to adjust collision for ideal grenade bouncing trajectories without altering visual geometry.

{% hint style="warning" %}
Because universal blockers block projectiles, players may use the Grappleshot to climb these invisible walls. They should not be used for seamless player containment.
{% endhint %}

Team blockers (blue) are an effective way to contain both players and vehicles within a gameplay space. If the Team property is set to Neutral, they will block players and vehicles from all teams. When assigned to a specific team, that designated team can pass through the blocker on foot or in a vehicle.

Player blockers (purple) were previously used to only block players; however, following an update around April 2024, these also began blocking all vehicles and gameplay objects. They are commonly utilized for containment on 4v4 maps where no vehicles are present.

### Vehicle, Projectile, and One-Way Blockers
Vehicle blockers (light blue) only block vehicles from a specific team. If the Team is set to Neutral, they will block all vehicles regardless of team.

{% hint style="info" %}
When driving a vehicle through a vertical blocker, players on the matching team typically pass through cleanly. However, at an angle of approximately 30° or greater, collision may break; this can result in either "soft blocking" or the vehicle being blocked entirely even when moving in the correct direction.
{% endhint %}

Projectile blockers (orange) block only projectiles, such as grenades and bullets. These are useful for creating custom FX barriers that players can walk through but which still interact with projectile physics.

One-Way blockers allow movement in one of six directions while blocking others. An arrow shape inside the blocker points to the X/forward direction toward the side that is blocked. Movement in the direction of this arrow is allowed, whereas movement against the direction of the arrow is blocked. The Team property can also be used to allow a specific team to bypass the blocker entirely.

## Scaling and Interaction

### Scalable vs. Dynamic Blockers
Scalable blockers are a type of blocker that can be scaled in size and were added late into Halo Infinite's development. They have become the primary method for creating large areas because they can cover much larger spaces than individual dynamic blockers, which are restricted to specific sizes such as 16x16x16, 256x2x128, or a maximum of 256x256x256.

Standard (dynamic) blockers have approximately 33 variants for each type and cannot be scaled. However, dynamic blockers retain utility in scripting because they can be manipulated like any other dynamic object, unlike static scalable blockers.

***

## Source Data

* Discord thread: [Blockers](https://discord.com/channels/220766496635224065/1538518983387385907/1538518983387385907)

#### <mark style="color:green;">Contributors</mark>

Okom
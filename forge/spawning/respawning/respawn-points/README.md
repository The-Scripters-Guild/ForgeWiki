---
description: >-
  Nodes used to spawn players after death or as a fallback for initial
  spawning if no other valid spawn points exist.
---

# Respawn Points

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Respawn Points are primarily used to spawn players after they have died during a match. They can also serve as fallback points for initial spawning if the map does not feature valid Team Intro Spawns or Initial Spawn Points.

## Placement and Orientation

Respawn Points should be placed around the outer edges of the map, mostly within each team's safe spawning areas. Some spawn points may also be placed on the edges of a middle divider; these are useful when spawns at the back of a base are unsafe due to enemy presence. Most players will naturally gravitate toward the safest areas rather than those in the middle divider.

When placing nodes, ensure they do not cause players to encounter sudden unexpected actions within two seconds of running forward from the spawn. Players often attempt to continue gameplay immediately upon spawning and may be unable to react to events like falling off a ledge or hitting a wall directly in front of them if the node is positioned poorly. 

Additionally, avoid floating respawn points. While players will spawn in the air and land on the nearest surface if a point is floating, this behavior should be avoided to ensure players spawn directly on the ground.

### Orientation

The Respawn Point should only ever be rotated on the Yaw axis, which determines the direction the player faces upon spawning. The node should not have rotation applied to the Pitch or Roll axes; doing so will rotate the player's camera in those directions immediately upon spawning, which is disorienting.

## Configuration and Quantity

For a standard setup, Respawn Points should utilize the following properties:
* **Team:** Neutral
* **Order:** 0
* **Ignore Danger:** Off
* **Ignore LoS:** Off

These settings allow the Respawn Point to be used by all teams without hardcoded spawn weighting. When configured this way, the game will automatically select the safest Respawn Point based on [Spawn Influence](https://wiki.thescriptersguild.com/forge/spawning/spawn-influence) at the moment of respawn.

### Recommended Amounts

The required number of Respawn Points varies based on map size and intended player count. Providing enough points scattered in safe spaces ensures players have sufficient options to spawn away from enemies:
* 2v2: 30–50
* 4v4: 50–80
* 8v8: 80–120
* 12v12: 120–180

***

## Source Data

* Discord thread: [Respawn Points](https://discord.com/channels/220766496635224065/1535813880364666880/1535813880364666880)

#### <mark style="color:green;">Contributors</mark>

Okom
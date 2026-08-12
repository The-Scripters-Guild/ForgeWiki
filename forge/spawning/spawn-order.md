---
description: >-
  Explains how Spawn Order functions as a spawning priority mechanism
  and an adjustable scripting variable for objects.
---

# Spawn Order

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The Spawn Order property is a versatile attribute that serves different purposes depending on the object and its context, primarily affecting spawning priority or acting as a scriptable variable.

## Spawning Priority
Spawn Order can be used to stagger the priority order of objects during gameplay. A lower Spawn Order value takes precedence over an object with a higher value. This is useful for ensuring specific spawns do not overlap in importance; for example, adjusting [Spawn Order of Initial Spawn Points](initial-spawning/initial-spawn-points.md#node-properties) can ensure they have a different priority than [Team Intro Spawns](initial-spawning/team-intro-spawns.md), allowing Team Intro Spawns to be prioritized if both objects are present on the map.

While this functionality exists for many objects, it's not largely utilized in Halo Infinite, as all of the spawn influence is handled via [Spawn Volumes](spawn-influence/spawn-volumes.md). The Spawn Order of Respawn Points shouldn't be altered in an effort to influence which Respawn Points are utilized.

## Scripting Usage
Most objects feature a default Spawn Order of 0. For many instances, the property can be used as an adjustable variable for scripting purposes or as a value shared by multiple objects by default. A useful scripting procedure is to fetch all objects with a Spawn Order of 0 in order to gather a list of most objects on the level.

***

## Source Data

* Discord thread: [Spawn Order](https://discord.com/channels/220766496635224065/1536624166495723531/1536624166495723531)

#### <mark style="color:green;">Contributors</mark>

Okom

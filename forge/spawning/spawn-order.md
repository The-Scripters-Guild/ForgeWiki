---
description: >-
  Explains how Spawn Order functions as a spawning priority mechanism
  and an adjustable scripting variable for objects in Halo Infinite.
---

# Spawn Order

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The Spawn Order property is a versatile attribute that serves different purposes depending on the object and its context, primarily affecting spawning priority or acting as a scriptable variable.

## Spawning Priority
Spawn Order can be used to stagger the priority order of objects during gameplay. A lower Spawn Order value takes precedence over an object with a higher value. This is useful for ensuring specific spawns do not overlap in importance; for example, adjusting [Spawn Order of Initial Spawn Points](initial-spawning/initial-spawn-points.md#node-properties) can ensure they have a different priority than [Team Intro Spawns](initial-spawning/team-intro-spawns.md), allowing Team Intro Spawns to be prioritized if both objects are present on the map.

### Respawn Points
{% hint style="warning" %}
The Spawn Order should not be changed on Respawn Points. Adjusting spawn priority and influence in Halo Infinite is handled via [Spawn Volumes](spawn-influence/spawn-volumes.md).
{% endhint %}

## Scripting Usage
Most objects feature a default Spawn Order of 0. For many instances, the property's primary utility is as an adjustable variable for scripting purposes or as a value shared by multiple objects by default.

***

## Source Data

* Discord thread: [Spawn Order](https://discord.com/channels/220766496635224065/1536624166495723531/1536624166495723531)

#### <mark style="color:green;">Contributors</mark>

Okom
---
description: >-
  An overview of the Spawn Order property, covering its use as a
  scripting variable and its role in prioritizing objects during
  spawning.
---

# Spawn Order

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While the name suggests a specific spawning function, the Spawn Order property is primarily used as an adjustable variable for scripting purposes or to store shared data across objects by default.

## General Usage and Scripting
Most objects in Halo Infinite are assigned a default Spawn Order of 0. For many creators, this property serves more effectively as an adjustable variable within scripts rather than a tool for direct spawning mechanics.

## Prioritization Logic
The primary application of the Spawn Order property regarding actual spawn logic is to stagger the priority order of objects being used. In these instances, assets with a lower Spawn Order value are prioritized over those with higher values.

### Staggering Spawns
To ensure specific spawns occur without overlapping in priority with others, designers can adjust their Spawn Order. For example, adjusting the [Spawn Order of Initial Spawn Points](initial-spawning/initial-spawn-points.md#node-properties) ensures they do not share the same priority as [Team Intro Spawns](initial-spawning/team-intro-spawns.md); if both exist on a map, the Team Intro Spawns will be prioritized.

#### Respawn Point Configuration
{% hint style="warning" %}
The Spawn Order property should not be modified on Respawn Points to manage spawn priority or influence.
{% endhint %}

Adjusting how spawns are influenced and their relative priority is handled through [Spawn Volumes](spawn-influence/spawn-volumes.md).

***

## Source Data

* Discord thread: [Spawn Order](https://discord.com/channels/220766496635224065/1536624166495723531/1536624166495723531)

#### <mark style="color:green;">Contributors</mark>

Okom
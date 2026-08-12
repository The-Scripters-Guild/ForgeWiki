---
description: >-
  Adjust spawn weighting within a volume's boundary to influence spawn
  probabilities or restrict enemy spawning in specific game modes.
---

# Spawn Volumes

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Spawn Volumes are used to modify the weighting of spawns within the boundary of a volume. They are commonly utilized to adjust spawn probabilities for specific groups or to completely prevent one team from spawning on the enemy side of a map.

## Weighting and Placement

### Adjusting Spawn Probability
Spawn weight is a value applied to each spawn point that influences whether a point is used with higher or lower probability. While the Spawn Volume object allows values ranging from `-128.00` to `128.00`, most applications utilize a range between `-16.00` and `16.00`.

When adjusting spawn weights, it is recommended as a starting point to add a Spawn Volume over the desired points with a weight of `-4.00` or `4.00`. This adjustment should only be applied if map testing reveals that certain spawns are being naturally under-utilized or over-utilized.

#### Placement Requirements
Spawn Volumes must be placed so that the boundary of the volume fully covers the intended spawn points.

## Configuration Profiles

Different properties can be configured within a Spawn Volume depending on its intended use case.

### Basic Spawn Influence
This configuration is used for adjusting the basic weighting of a specific group of spawns.

* **Labels:** None
* **Team:** Neutral
* **Weight:** (User-defined)
* **Disable Spawn Points:** Off
* **Affects Opposing Team:** Off
* **Affects Initial Spawns:** Off

{% hint style="info" %}
Using the "Neutral" team setting ensures that weight applies to any player spawning on those points. This is important in modes like Slayer, where respawn points can flip between teams.
{% endhint %}

### Preventing Enemy Side Spawning
This configuration is used to ensure only one specific team is permitted to spawn within a volume's boundary. This is commonly employed to prevent "spawn flipping" in certain game modes.

* **Label 1:** CTF Include
* **Label 2:** Stockpile Include
* **Label 3:** Total Control Include
* **Team:** (The team allowed to spawn)
* **Weight:** 0.00
* **Disable Spawn Points:** On
* **Affects Opposing Team:** On
* **Affects Initial Spawns:** Off

The inclusion labels allow the Spawn Volume to only appear during specific game modes. If support for a mode like Stockpile or Total Control is not planned for the map, "CTF Include" may be the only label required.

***

## Source Data

* Discord thread: [Spawn Volumes](https://discord.com/channels/220766496635224065/1536608379084996658/1536608379084996658)

#### <mark style="color:green;">Contributors</mark>

Okom
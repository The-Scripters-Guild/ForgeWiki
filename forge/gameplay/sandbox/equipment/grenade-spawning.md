---
description: >-
  Explanations regarding grenade spawning methods and configuration
  using Forge objects.
---

# Grenade Spawning

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article details how to use various Forge objects for grenade spawning in Halo Infinite, including dispenser setups and object properties.

Explanations about the topics related to grenade spawning, and all ways to spawn grenades in Halo Infinite via Forge objects.

## Grenade Dispenser

The Grenade Dispenser is the main spawner for grenades. It's intended to be placed on the ground.

The standard setup for a Grenade Dispenser is as follows:
* **Grenade Quantity:** 2
* **Spawn Cyclically:** Off
* **Grenade:** (user-defined)
* **Static Selection:** Enabled
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** GrenadePadPlacementKey

{% hint style="info" %}
Read about the details about the Static Selection and Spawn Properties [here](../spawn-properties.md).
{% endhint %}

## Grenade Objects

The individual, loose grenade objects aren't used in any standard setup. For usage in custom games, it's still useful to know the object properties:

### Object Properties

* Despawn category: When the weapon should despawn. Abandoned/Disturbed means when the weapon is moved from its initial spawn position.
* Respawn category: Death/Deletion means when the weapon despawns, Disturbance means when the weapon is moved from its initial spawn position.

***

## Source Data

* Discord thread: [Grenade Spawning](https://discord.com/channels/220766496635224065/1535167635258347530/1535167635258347530)

#### <mark style="color:green;">Contributors</mark>

Okom
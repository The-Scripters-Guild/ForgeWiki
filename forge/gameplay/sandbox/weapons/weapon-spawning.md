---
description: >-
  Explanations regarding weapon spawning and the various Forge objects
  used to spawn weapons in Halo Infinite.
---

# Weapon Spawning

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article explores the mechanisms behind weapon spawning within Halo Infinite Forge, detailing how various spawners and item classes influence the availability of weapons during gameplay.

## Class

Classes are a way to have the game randomly select a weapon from a pre-determined pool if the "Static Selection" property is set to Disabled.

Breakdown of the weapons within each class:

### Default variants

* **Anti-Vehicle:** Disruptor, MLRS-2 Hydra, Shock Rifle
* **Any:** All weapons
* **Assault Rifle:** Bandit Evo, M392 Bandit, Pulse Carbine
* **Launcher:** Cindershot, Fuel Rod SPNKr, M41 SPNKr, MLRS-2 Hydra, Ravager
* **Melee:** Energy Sword, Gravity Hammer, Mutilator
* **Pistol:** Disruptor, Mangler, Plasma Pistol
* **SMG:** MA5K Avenger, Needler, Sentinel Beam
* **Shotgun:** CQS48 Bulldog, Heatwave
* **Sniper Rifle:** S7 Sniper Rifle, Shock Rifle, Skewer, Stalker Rifle
* **Tactical Rifle:** BR75, VK78 Commando Rifle, Vestige Carbine

### Legendary variants

The legendary weapons will only appear if the "Legendary Variants" option is set to Included or Preferred.

* **Anti-Vehicle:** Calcine Disruptor, Pursuit Hydra, Purging Shock Rifle
* **Any:** All weapons
* **Assault Rifle:** Bandit Evo, M392 Bandit, Rapidfire Pulse Carbine
* **Launcher:** Backdraft Cindershot, Fuel Rod SPNKr, M41 Tracker, Pursuit Hydra, Rebound Ravager
* **Melee:** Duelist Energy Sword, Elite Bloodblade, Infected Energy Sword, Rushdown Hammer, Mutilator
* **Pistol:** Calcine Disruptor, Riven Mangler, Unbound Plasma Pistol
* **SMG:** MA5K Avenger, Pinpoint Needler, Arcane Sentinel Beam
* **Shotgun:** Convergence Bulldog, Scatterbound Heatwave
* **Sniper Rifle:** S7 Flexfire Sniper, Purging Shock Rifle, Volatile Skewer, Stalker Rifle Ultra
* **Tactical Rifle:** BR75 Breacher, Impact Command, Vestige Carbine

{% hint style="info" %}
The MA40 Assault Rifle, Mk50 Sidekick or Mythic Sandwich don't appear in any of the categories.
{% endhint %}

## Weapon Rack

The Weapon Rack is the main spawner for base weapons. It's intended to be placed on walls in a vertical orientation. Horizontal orientation is accepted, but not standard.

The standard setup for a Weapon Rack is as follows:
* **Weapon:** (user-defined)
* **Static Selection:** Disabled
* **Class:** (user-defined, but usually what the Weapon belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** WeaponRackPlacementKey

{% hint style="info" %}
Read about the details about the Static Selection and Spawn Properties [here](../spawn-properties.md).
{% endhint %}

## Weapon Pad

The Weapon Pad is the main spawner for power weapons. It's intended to be placed on the ground.

The standard setup for a Weapon Pad is as follows:
* **Weapon:** (user-defined)
* **Static Selection:** Disabled
* **Class:** (user-defined, but usually what the Weapon belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Preview As Hologram:** On
* **Rotate Item:** On
* **Navpoint:** On
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** PowerWeaponPadPlacementKey
* **Exclude Gravity Hammer:** Off

## Weapon Trunk

The Weapon Trunk is rarely used in standard setups, but it hasn't been excluded from usage. Properties not listed don't matter.

The standard setup for a Weapon Trunk is as follows:
* **Weapon:** (user-defined)
* **Static Selection:** Disabled
* **Class:** (user-defined, but usually what the Weapon belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** On
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** WeaponTrunkPlacementKey

## Weapon Pod

The Weapon Pod is not used in standard setups, but it still follows the same logic as other spawners. It's only used in Big Team Battle as ordnance drops. Properties not listed don't matter.

The standard setup for a Weapon Pod is as follows:
* **Weapon:** (user-defined)
* **Static Selection:** Disabled
* **Class:** (user-defined, but usually what the Weapon belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** On
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** OrdnancePodPlacementKey

## Classic Weapon Spawn

The Classic Weapon Spawn is not used in standard setups, but it still follows the same logic as other spawners. It's only used in Infection as the main way of spawning weapons. Properties not listed don't matter.

The standard setup for a Classic Weapon Spawn is as follows:
* **Weapon:** (user-defined)
* **Static Selection:** Disabled
* **Class:** (user-defined, but usually what the Weapon belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** WeaponRackPlacementKey

## Weapon Objects

The individual, loose weapon objects aren't used in any standard setup. For usage in custom games, it's still useful to know the object properties:

* Despawn category: When the weapon should despawn. Abandoned/Disturbed means when the weapon is moved from its initial spawn position.
* Respawn category: Death/Deletion means when the weapon despawns, Disturbance means when the weapon is moved from its initial spawn position.
* Spare Clips: How many extra magazines the weapon spawns with. Maximum 16, which on some weapons is more than the normally allowed maximum ammo capacity.

***

## Source Data

* Discord thread: [Weapon Spawning](https://discord.com/channels/220766496635224065/1535159391962136606/1535159391962136606)

#### <mark style="color:green;">Contributors</mark>

Okom

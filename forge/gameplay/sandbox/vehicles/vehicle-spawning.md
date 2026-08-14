---
description: >-
  Explanations regarding various methods and topics for spawning
  vehicles within Halo Infinite via Forge objects.
---

# Vehicle Spawning

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Explanations about the topics related to vehicle spawning, and all ways to spawn vehicles in Halo Infinite via Forge objects.

## Randomization Mechanics

### Class

Classes are a way to have the game randomly select a vehicle from a pre-determined pool if the "Static Selection" property is set to Disabled.

Breakdown of the vehicles within each Class:

* **Any:** All vehicles
* **Cavalry:** Falcon, Rockethog, Warthog
* **Duelist:** Banshee, Chopper, Chieftain Chopper (Legendary), Ghost, Gungoose, Wasp
* **Siege:** Scorpion, Wraith
* **Support:** Mongoose, Razorback

### Terrain Type

The Terrain Type is another filter in combination with the Class to have the game randomly select a vehicle from a pre-determined pool if the "Static Selection" property is set to Disabled.

Breakdown of the vehicles within each Terrain Type:

* **Air:** Banshee, Falcon, Wasp
* **Any:** All vehicles
* **Land:** Chieftain Chopper (Legendary), Chopper, Ghost, Gungoose, Mongoose. Razorback, Rockethog, Scorpion, Warthog, Wraith

### Faction

Factions are a way restrict the random vehicle pool even more to vehicles belonging to a faction if the "Static Selection" property is set to Disabled.

* **Banished:** Banshee, Chopper, Chieftain Chopper (Legendary), Ghost, Wasp, Wraith
* **UNSC:** Falcon, Gungoose, Mongoose, Razorback, Rockethog, Scorpion, Warthog

## Spawning Methods and Objects

### Vehicle Pad

The Vehicle Pad is the main spawner for vehicles. It's intended to be placed on the ground.

The standard setup for a Vehicle Pad is as follows:
* **Vehicle:** (user-defined)
* **Static Selection:** Enabled
* **Class:** (user-defined, but usually what the Vehicle belongs in)
* **Terrain Type:** (user-defined, but usually what the Vehicle belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** VehiclePadPlacementKey

{% hint style="info" %}
Read about the details about the Static Selection and Spawn Properties [here](../spawn-properties.md).
{% endhint %}

### Classic Vehicle Spawn

The Classic Vehicle Spawn is not the standard spawner for vehicles, but it has been used on some Big Team Battle maps.

The standard setup for a Classic Vehicle Spawn is as follows:
* **Vehicle:** (user-defined)
* **Static Selection:** Enabled
* **Class:** (user-defined, but usually what the Vehicle belongs in)
* **Terrain Type:** (user-defined, but usually what the Vehicle belongs in)
* **Legendary Variants:** Exclude
* **Faction:** Any
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** VehiclePadPlacementKey

### Vehicle Objects

The individual, loose vehicle objects aren't used in any standard setup. For usage in custom games, it's still useful to know the object properties:

* Despawn category: When the weapon should despawn. Abandoned/Disturbed means when the weapon is moved from its initial spawn position.
* Respawn category: Death/Deletion means when the weapon despawns, Disturbance means when the weapon is moved from its initial spawn position.
* Camera Distance: How far the third-person camera is placed from the vehicle when operating.

***

## Source Data

* Discord thread: [Vehicle Spawning](https://discord.com/channels/220766496635224065/1535169262774259822/1535169262774259822)

#### <mark style="color:green;">Contributors</mark>

Okom

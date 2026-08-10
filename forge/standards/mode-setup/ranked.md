---
description: >-
  Guidelines regarding unique property adjustments and procedures used
  when setting up maps for Ranked modes.
---

# Ranked

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article outlines the guidelines for object property deviations and specific setup procedures required to accommodate ranked competitive playstyles on a map.

## Ranked sandbox behavior

Any official "Ranked" mode automatically adjusts the sandbox on the map so that all item spawners have the "Static Selection" property forcefully Enabled. This results in the "Class" property being ignored, and the Weapon/Equipment/Grenade/Vehicle set on the spawner only spawning that item instead of picking by random from the item options in the selected Class.

{% hint style="info" %} A Weapon Rack with the following properties will spawn a BR75 in Ranked modes, and a CQS48 Bulldog or Heatwave in non-Ranked modes:
* Weapon: BR75
* Static Selection: Disabled
* Class: Shotgun {% endhint %}

## Standard spawners

Item spawners standard for Ranked modes:
* Weapon Rack
* Weapon Pad
* Equipment Dispenser
* Power Equipment Pad
* Grenade Dispenser
* Vehicle Pad

Item spawners not standard for Ranked modes:
* Weapon Pod
* Weapon Trunk
* Weapon objects
* Classic Equipment Spawn
* Classic Grenade Spawn
* Grenade objects
* Classic Vehicle Spawn
* Vehicle objects

## Weapons

Adjustments to weapons required for the standard Ranked sandbox. These are modifications to the [standard setup for weapon spawners](../../gameplay/sandbox/weapons/weapon-spawning.md).

### M41 SPNKr

* **Spawn Properties:** Custom
* **Ammo Multiplier:** 50%
* **Spawn Logic:** Static (Time)
* **Spawn Time:** 120.00
* **Max Deployed:** 0.00

### Weapon pool

The weapon pool for the standard 4v4 Ranked sandbox. There's no limitation on the weapon pool in 8v8 Ranked.

Standard weapons for Ranked modes:
* BR75
* Bandit Evo
* CQS48 Bulldog
* M41 SPNKr
* Mk50 Sidekick
* Needler
* Plasma Pistol
* S7 Sniper Rifle
* Shock Rifle
* Stalker Rifle
* VK78 Commando Rifle
* Vestige Carbine

{% hint style="info" %} The CQS48 Bulldog and Needler are not used in official tournaments, but are fine for matchmaking. {% endhint %}

Non-standard weapons for Ranked modes:
* Cindershot
* Diminisher of Hope
* Disruptor
* Elite Bloodblade
* Energy Sword
* Fuel Rod SPNKr
* Gravity Hammer
* Heatwave
* Infected Energy Sword
* M392 Bandit
* MA40 Assault Rifle
* MA5K Avenger
* MLRS-2 Hydra
* Mangler
* Mutilator
* Mythic Sandwich
* Pulse Carbine
* Ravager
* Sentinel Beam
* Skewer
* Fusion Coils

{% hint style="info" %} To exclude a weapon spawner from Ranked modes, apply the "Ranked Exclude" label on the object. To make a weapon spawner only appear in Ranked modes, apply the "Ranked Include" label. {% endhint %}

## Equipment

Adjustments to equipment required for the Ranked sandbox. These are modifications to the [standard setup for equipment spawners](../../gameplay/sandbox/equipment/equipment-spawning.md).

### All base equipment

These adjustments apply to all base equipment; power equipment remain unchanged.

* **Spawn Properties:** Custom
* **Spawn Logic:** Dynamic (Pickup)
* **Spawn Time:** 60.00
* **Max Deployed:** 1.00 (creates the "[red-rack](../../forge-basics-and-ui/forge-terminology.md#creator-vocabulary-and-objects)" effect)

### Drop Wall

* **Spawn Properties:** Custom
* **Charge Multiplier:** 50%

### Shroud Screen

* **Spawn Properties:** Custom
* **Charge Multiplier:** 50%

### Threat Seeker

* **Spawn Properties:** Custom
* **Charge Multiplier:** 50%

{% hint style="info" %} These equipment variants require a separate Equipment Dispenser for the Ranked sandbox if you want to support both a standard Arena and Ranked sandbox. {% endhint %}

### Equipment pool

The equipment pool for the standard 4v4 Ranked sandbox. There's no limitation on the equipment pool in 8v8 Ranked.

Standard equipment for Ranked modes:
* Active Camouflage
* Drop Wall
* Grappleshot
* Overshield
* Quantum Translocator
* Repulsor
* Shroud Screen
* Threat Seeker
* Thruster
* Frag Grenade
* Plasma Grenade
* Spike Grenade

Non-standard equipment for Ranked modes:
* Custom Equipment A
* Custom Equipment B
* Custom Equipment C
* Custom Equipment D
* Repair Field
* Threat Sensor
* Dynamo Grenade

{% hint style="info" %} To exclude an equipment spawner from Ranked modes, apply the "Ranked Exclude" label on the object. To make a equipment spawner only appear in Ranked modes, apply the "Ranked Include" label. {% endhint %}

***

## Source Data

* Discord thread: [Ranked](https://discord.com/channels/220766496635224065/1535134742859743312/1535134742859743312)

#### <mark style="color:green;">Contributors</mark>

Okom\
Callous

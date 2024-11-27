---
description: How to set up a level to support 4v4 Stockpile.
---

# 4v4 Stockpile

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

4v4 Stockpile by [WAR FH](https://www.unggoy.xyz/browse?gamertag=WAR+FH\&ownerOnly=true) is a variant of [Stockpile](../../../forge/modes/stockpile.md) that is tailored for competitive 4v4 gameplay. Power Seeds spawn in 5 set locations on the map and need to be delivered to your team's Power Sockets to gain score. 3 delivered Power Seeds results in a score increase for the team. The first team to 3 score wins. Players can also steal Power Seeds from enemy Power Sockets and bring them back to their own.



## Gamemode setup

The objects required on-level to support 4v4 Stockpile.

* [5 Power Seed Spawns](4v4-stockpile.md#power-seed-spawns)
* [3 Power Sockets per Team](4v4-stockpile.md#power-sockets)
* [1 Stockpile Navpoint (Stronghold Capture Zone) per team](4v4-stockpile.md#stockpile-navpoints)
* [Spawn Volumes for preventing spawn-flipping](4v4-stockpile.md#spawn-influence)

{% hint style="info" %}
A prefab with correctly set up objects for this mode can be found here: [ForgeHub 4v4 Stockpile Template](https://www.halowaypoint.com/halo-infinite/ugc/browse?searchTerm=ForgeHub+4v4+Stockpile+Template) by [Okom1](https://www.unggoy.xyz/browse?gamertag=Okom1\&ownerOnly=true).
{% endhint %}

### Power Seed Spawns

Power Seed Spawns determine the locations where Power Seeds should spawn.

#### Object path

* `Gameplay`
  * `Game Modes`
    * Power Seed Spawn

#### Placement

Place 3 Power Seed Spawns in neutral positions around the middle of the map that don't favor either team. Place the remaining 2 near the other Power Seed Spawns, but each slightly favoring one team.

Place each Power Seed Spawn flat on the intended surface. The origin point of the Power Seed Spawn object should be positioned on the surface and not floating above it. Having the origin point float above the surface means that the Power Seed will spawn in the air and drop on the ground.

#### Labels

* None

{% hint style="info" %}
As this object is not visible in gameplay and has no effect in modes that don't use it, it doesn't require a gamemode "Include" label.
{% endhint %}

#### Properties

* **Power Seed Variant**: User choice.

### Power Sockets

Power Sockets are where Power Seeds should be delivered to.

#### Object path

* `Gameplay`
  * `Game Modes`
    * Power Socket Forerunner
    * Power Socket UNSC
    * Power Socket UNSC Engine Blue
    * Power Socket UNSC Engine Red
    * Power Socket UNSC Green Sand
    * Power Socket UNSC Yellow
    * Power Socket UNSC Yellow Sand

#### Placement

Place 3 Power Sockets per team next to one another and in a relatively open and vulnerable area near each team's base. The goal is to promote the stealing of Power Seeds and for them to be delivered back to the other team's Power Sockets in around 4 seconds.

#### Labels

* Stockpile Socket
* Stockpile Include

#### Properties

* **Team:** Team 1 (Eagle) / Team 2 (Cobra)
* **One Time Use**: Off
* **Create With Carriable Attached**: Off
* **Use Device Interaction**: On
* **Removal Hold Time**: 3.00
* **Planting Hold Time**: 2.00

### Stockpile Navpoints

Stockpile Navpoints are used to create a navpoint on the Power Sockets to show players where to deliver the Power Seeds.

#### Object path

* `Gameplay`
  * `Game Modes`
    * Stronghold Capture Zone

{% hint style="info" %}
The Stronghold Capture Zone object is used for this item, but the correct label makes it work as intended.
{% endhint %}

#### Placement

Place 1 Stronghold Capture Zone 6.5 units below where the "Deliver" navpoint should show up. Usually this is placed at the position of the central Power Socket.

{% hint style="info" %}
The zone boundary has no effect on the navpoint.
{% endhint %}

#### Labels

* Stockpile Navpoint

{% hint style="info" %}
As this object is not visible in gameplay and has no effect in modes that don't use it, it doesn't require a gamemode "Include" label.
{% endhint %}

#### Properties

* **Team:** Team 1 (Eagle) / Team 2 (Cobra)

### Spawn Influence

Spawn Volumes are used to prevent teams from swapping sides during 4v4 Stockpile gameplay.

#### Object path

* `Gameplay`
  * `Player Spawning`
    * Spawn Volume \[Respawn]

#### Placement

Place 1 Spawn Volume per team covering half of the map's Respawn Points within the boundary. The Spawn Volumes should intersect in the middle of the map. Avoid overlapping the Spawn Volumes as the overlap area will block players on both teams from spawning in it.

{% hint style="info" %}
Spawn Volumes are used to adjust the spawning influence of Spawn Points within the boundary.
{% endhint %}

#### Labels

* Stockpile Include

#### Properties

Eagle:

* **Team:** Team 1 (Eagle)
* **Weight**: 0.00
* **Disable Spawn Points**: On
* **Affects Opposing Team**: On
* **Affects Initial Spawns**: Off

Cobra:

* **Team:** Team 2 (Cobra)
* **Weight**: 0.00
* **Disable Spawn Points**: On
* **Affects Opposing Team**: On
* **Affects Initial Spawns**: Off



## Sandbox setup

As 4v4 Stockpile is based on a BTB mode, but is intended for Ranked 4v4 play, the sandbox of the map needs to be forced to Ranked 4v4 settings for optimal gameplay, otherwise the properties that default to BTB modes would be used such as faster spawning weapons.

* [Custom Spawn Properties for base Weapon Spawners](4v4-stockpile.md#base-weapon-spawners)
* [Custom Spawn Properties for base Equipment Spawners](4v4-stockpile.md#base-equipment-spawners)
* [Custom Spawn Properties for specific Equipment and Power Weapons for Ranked modes](4v4-stockpile.md#ranked-variant-spawners)

### Base Weapon Spawners

Adjust the Spawn Properties of the [Weapon Spawners](../../../forge/gameplay/sandbox/weapons/weapon-spawning/) on the level to match the following:

{% hint style="info" %}
Power Weapons (Tier 3) don't need to be adjusted.
{% endhint %}

#### Tier 1

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 100%
* **Spawn Logic**: Dynamic (Expired)
* **Spawn Time**: 30.00
* **Max Deployed**: 0.00

For the following weapons:

* `BR75`
* `VK78 Commando`
* `MA40 AR`
* `Pulse Carbine`
* `M392 Bandit`
* `Bandit Evo`
* `Disruptor`
* `Mangler`
* `Plasma Pistol`
* `Mk50 Sidekick`

#### Tier 2, 100%

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 100%
* **Spawn Logic**: Dynamic (Expired)
* **Spawn Time**: 60.00
* **Max Deployed**: 0.00

For the following weapons:

* `MLRS-2 Hydra`
* `Ravager`
* `Sentinel Beam`
* `Needler`
* `MA5K Avenger`

#### Tier 2, 50%

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 50%
* **Spawn Logic**: Dynamic (Expired)
* **Spawn Time**: 60.00
* **Max Deployed**: 0.00

For the following weapons:

* `Shock Rifle`
* `Stalker Rifle`
* `CQS48 Bulldog`
* `Heatwave`

### Base Equipment Spawners

Adjust the Spawn Properties of the [Equipment Spawners](../../../forge/gameplay/sandbox/equipment/equipment-spawning/) on the level to match the following:

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 100%
* **Spawn Logic**: Dynamic (Pickup)
* **Spawn Time**: 60.00
* **Max Deployed**: 0.00

For the following equipment:

* `Drop Wall`
* `Grappleshot`
* `Repair Field`
* `Repulsor`
* `Shroud Screen`
* `Threat Seeker`
* `Threat Sensor`
* `Thruster`

### Ranked variant Spawners

Specific equipment and weapons in have been adjusted by HCS ruling to have less ammo/charge when played in Ranked modes. These changes need to be adjusted on-level, and a Ranked-specific variant of a spawner needs to be duplicated at the same position with specific Spawn Properties.

#### Power Weapons

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 50%
* **Spawn Logic**: Static (Time)
* **Spawn Time**: 120.00–150.00
* **Max Deployed**: 0.00

For the following weapons:

* `Rocket Launcher`

#### Base Equipment

* **Spawn Properties**: Custom
* **Ammo Multiplier**: 50%
* **Spawn Logic**: Dynamic (Pickup)
* **Spawn Time**: 60
* **Max Deployed**: 0.00

For the following equipment:

* `Drop Wall`
* `Shroud Screen`
* `Threat Seeker`

{% hint style="warning" %}
Any Threat Sensor equipment should be replaced with a Threat Seeker for Ranked modes.
{% endhint %}

#### Labels

The two spawner variants should not appear in a mode at the same time. Labels need to be assigned to prevent this.

**Default spawner:**

* Ranked Exclude
* Stockpile Exclude

**Ranked Variant:**

* Ranked Include
* Stockpile Include



***

#### <mark style="color:green;">Contributors</mark>

Okom

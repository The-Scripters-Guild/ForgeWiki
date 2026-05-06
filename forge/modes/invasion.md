---
description: >-
  Guidelines for setting up maps for the official Invasion game mode.
---

# Invasion

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Invasion is an asymmetrical, 8v8 objective mode featuring two rounds of attack and defense. Each round is divided into three distinct phases, where teams compete to complete specific objectives to earn points.

## Gameplay and Objectives

The mode incorporates several objective types inspired by *Halo: Reach*, including Capture the Zone, Assault, Core Delivery, and Deliver the Payload. Matches are scored based on phase completion; successfully progressing through a phase awards a point to the team. It is possible for a match to end in a tie if both teams successfully complete all three phases.

### Phase Progression

Each phase features specific gameplay constraints regarding spawns, vehicle access, and available equipment:

* **Phase 1**
 * **Spawn Orders:** 11, 12, 13.
 * **Objective Spawn Order:** 1.
 * **Loadouts:** 2 per team.
 * **Vehicles:** Tier 1 vehicles only (Spawn Order 1).
 * **Power Weapons:** None available.
* **Phase 2**
 * **Spawn Orders:** 21, 22, 23.
 * **Objective Spawn Order:** 2.
 * **Loadouts:** 3 per team.
 * **Vehicles:** Tier 1 and Tier 2 vehicles (Spawn Order 2).
 * **Power Weapons:** Available.
* **Phase 3**
 * **Spawn Orders:** 31, 32, 33.
 * **Objective Spawn Order:** 3.
 * **Loadouts:** 5 per team.
 * **Vehicles:** Tiers 1 through 4 (Spawn Order 3).
 * **Power Weapons:** Available.

### Spawning Mechanics

In addition to standard Left, Middle, or Right spawns, Invasion utilizes Buddy Spawning. In this system, players are randomly assigned a reciprocal buddy for the duration of the match.

{% hint style="info" %}
To use Buddy Spawning, your buddy must be alive for at least five seconds, possess full health and shields, and be clear of nearby enemies or engagements.
{% endhint %}

If a buddy is in a vehicle, a seat must be available to spawn on them. Note that if a buddy abandons the match, the ability to Buddy Spawn is lost for the remaining players.

## Map Setup

Configuring a map for Invasion requires specific settings for items, vehicles, and module-specific labels.

### Weapons and Vehicles

Weapons can be found on pads, lockers, drop pods, and chests. All normal weapon spawns utilize a "Red Racked" system, meaning a weapon will not respawn until the previously spawned weapon has been despawned. The respawn timer for these weapons is 10 seconds. Grenades and equipment are not spawned on the map; they are part of the player's loadout but can be scavenged from fallen players.

For vehicles, creators should use the vehicle object rather than a classic or vehicle spawner. Vehicles must have their "Respawn" setting set to "Off" and should be assigned the appropriate spawn order for the phase.

| Tier | Vehicles | Respawn Time |
| --- | --- | --- |
| **Tier 1** | Mongoose, Razor Back | 5 seconds |
| **Tier 2** | Brute Chopper, Ghost, Gungoose, Rockethog, Warthog | 10 seconds |
| **Tier 3** | Banshee, Boss Chopper, Wasp, Falcon | 30 seconds |
| **Tier 4** | Scorpion, Wraith | 90 seconds |

### Module Labeling

To ensure the Invasion mode functions correctly, gameplay objects must be assigned specific labels based on the active module.

* **Assault ([Label](../../scripting/nodes/variables-literals/label.md): Bravo)**
 * Items: All Assault Items
 * Bomb: Assault Bomb
 * Zones: Assault Site
 * Plates: Assault Plate
 * Bomb Spawn: Assault Bomb Spawn
* **Zone Capture (`Label`: Alpha)**
 * Items: All Zone Capture Items
 * Hills: King of the Hill Zone
* **Payload (`Label`: Delta)**
 * Items: All Payload Mode Items
 * Zone: Strongholds Zone
 * Crate: Yankee
 * Cart: Xray
 * Totem: Tango
* **Core Delivery (`Label`: Charlie)**
 * Items: All Core Delivery Items
 * Flag: Flag Stand Spawner
 * Plate: Flag Delivery Plate

 <figure><img src="../../.gitbook/assets/image-3fdd.png" alt="Assault Setup"><figcaption><p>The Assault module uses specific object properties to define gameplay zones and items.</p></figcaption></figure>

 <figure><img src="../../.gitbook/assets/image-3b8c.png" alt="Zone Capture Setup"><figcaption><p>Zone Capture items are identified using the Alpha label.</p></figcaption></figure>

 <figure><img src="../../.gitbook/assets/image-1044.png" alt="Payload Setup"><figcaption><p>The Payload module requires specific labels for zones, crates, and carts.</p></figcaption></figure>

## On-Map Events

The mode automatically fires specific on-map events. Map creators can hook into these triggers to execute custom functions unique to their map.

<figure><img src="../../.gitbook/assets/image-cc96.png" alt="On Map Events Brain"><figcaption><p>The On Map Events Brain allows creators to hook into automatic mode triggers for custom map functions.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image-1751.png" alt="Brain 1"><figcaption><p>The first On Map Events Brain represents a configuration for map triggers.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image-458a.png" alt="Brain 2"><figcaption><p>The second On Map Events Brain manages event logic within the map.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image-db29.png" alt="Brain 3"><figcaption><p>The third On Map Events Brain provides additional event handling capabilities.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image-aa55.png" alt="Brain 4"><figcaption><p>The fourth On Map Events Brain allows for further customization of map-specific logic.</p></figcaption></figure>

***

## Source Data

* Discord thread: [Invasion Setup](https://discord.com/channels/220766496635224065/1501455397322756197/1501455397322756197)

#### <mark style="color:green;">Contributors</mark>

Okom
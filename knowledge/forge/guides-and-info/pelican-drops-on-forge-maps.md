---
description: >-
  Guidelines for configuring Pelican Drops on Forge maps using
  Firefight mode settings and specific object properties.
---

# Pelican Drops on Forge maps

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Pelican Drops, which are usually reserved for specific game modes, can be integrated into Forge maps using specific object settings and Firefight mode configurations.

## Implementation

To enable Pelican Drops on a Forge map, several environmental and mode-specific conditions must be met.

<figure><img src="../../../.gitbook/assets/HaloInfinite_ecJMgmvXcj.jpg" alt="Cover image"><figcaption><p>The Pelican Drop object can be placed on a map to initiate a drop sequence.</p></figcaption></figure>

### Setup Requirements

For the drop to trigger successfully, the following setup is required:

* A "Pelican Drop" object must be placed on the map (hidden object). A working Firefight: King of the Hill setup is typically required. An example of a map containing this object can be found [here](https://www.halowaypoint.com/halo-infinite/ugc/maps/47dce9d6-f7bd-4570-9e75-e4a9c0fcab5d).
* The map must be loaded using a Firefight mode (any Firefight variant works).

### Object Properties

The Pelican Drop object requires specific properties to function as intended. The **Cargo Drop Type** must be set to **Exact Drop**. Other relevant properties include:

* **Spawn Properties**: Default
* **Symmetrical Channel**: AirDrop Alpha
* **Selective Channel**: AirDrop Alpha
* **Drop Range**: 3.00

A prefab with a fully set up Pelican Drop object can be found here: [Pelican Drop](https://www.halowaypoint.com/halo-infinite/ugc/prefabs/0c3e683d-e324-4b2a-95c8-71fdf6740c18)

## Mode Configuration

The functionality of the Pelican Drop is tied to internal events triggered by specific mode settings. In the Mode Editor, the **Firefight → Prevent Item Respawns** option must be set to **True**. Although this setting is typically used to prevent the automatic respawn of items, it is required for the Pelican Drop to function. This setting is usually set to **True** by default.

<figure><img src="../../../.gitbook/assets/2026-04-17_HaloInfinite-n5gx.jpg" alt="Cover image"><figcaption><p>The Prevent Item Respawns setting must be enabled in the Mode Editor.</p></figcaption></figure>

## Constraints and AI Behavior

### Pilot AI Characteristics

The Pelican is piloted by an invisible, frictionless AI entity that has no physical size but is still affected by gravity. This pilot cannot be removed from the vehicle through standard methods, such as flipping the vehicle. If the pilot AI is damaged or deleted, the Pelican vehicle will also be deleted.

<figure><img src="../../../.gitbook/assets/HaloInfinite_mJ25QayzqK.jpg" alt="Cover image"><figcaption><p>The pilot of the Pelican is an invisible AI entity.</p></figcaption></figure>

### Flight and Scripting Limitations

The Pelican Drop is designed to trigger at the start of gameplay; delaying or activating the drop via command is not currently possible, though blocking it with ghost objects may work on developer BTB maps. Furthermore, there are specific constraints regarding vehicle usage in different modes:

* **Firefight modes**: Attempting to pilot a Pelican using a vehicle type reference in Firefight modes will result in the pilot being automatically kicked out of the vehicle. Once this happens, the vehicle may become un-enterable via scripts.
* **BTB:Slayer**: Flying the Pelican vehicle is possible in BTB:Slayer on developer-made maps.

{% hint style="warning" %}
Attempting to pilot a Pelican in Firefight modes via a vehicle type reference will result in the pilot being automatically kicked out of the vehicle.
{% endhint %}

#### Scripting: Player Respawns and Entering

When using scripts to facilitate players entering a Pelican, players who have been revived in FFKOTH may encounter issues where they remain on a death screen. This occurs because internal scripting may not automatically unblock respawns after a player is revived. To resolve this, add an `Unblock Respawns For Player` node immediately after teleporting the player to ensure the "enter" sequence proceeds correctly.

Because players cannot use conventional methods to enter a Pelican, "entering" must be simulated by respawning the player into the Pelican vehicle type at the vehicle's location. If the entry sequence is triggered by a switch, add a small delay to the script. Without this delay, the button used to activate the switch (such as "E") may be interpreted as the exit vehicle command immediately after the player is teleported inside.

{% hint style="info" %}
Add a small delay to switch-activated entry scripts to prevent the player from immediately exiting the Pelican.
{% endhint %}

***

## Source Data

* Discord thread: [Pelican Drops on Forge maps](https://discord.com/channels/220766496635224065/1210616741756014632/1210616741756014632)

#### <mark style="color:green;">Contributors</mark>

Okom\
thescriptinator\
Dj_HurstyDNB\
SpawnOfTheDeep\
Josh
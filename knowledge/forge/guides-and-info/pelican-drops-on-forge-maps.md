---
description: >-
  Implementing functional Pelican Drops on Forge maps using specific
  object settings and Firefight mode configurations.
---

# Pelican Drops on Forge maps

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Although Pelican Drops are usually restricted to specific game modes, they can be implemented on Forge maps by combining particular object properties with Firefight mode settings.

## Implementation

To enable Pelican Drops on a Forge map, several environmental and mode-specific conditions must be met.

<figure><img src="../../../.gitbook/assets/HaloInfinite_ecJMgmvXcj.jpg" alt="Cover image"><figcaption><p>The Pelican Drop object can be placed on a map to initiate a drop sequence.</p></figcaption></figure>

### Setup Requirements

For the drop to trigger successfully, the following setup is required:

* A "Pelican Drop" object must be placed on the map (hidden object).
* The map must be loaded using a Firefight mode (all Firefight variants, including Firefight: Custom, are supported).

### Object Properties

The Pelican Drop object requires specific properties to function as intended. The Cargo Drop Type must be set to "Exact Drop." Other relevant properties include:

* **Spawn Properties**: Default
* **Symmetrical Channel**: AirDrop Alpha
* **Selective Channel**: AirDrop Alpha
* **Cargo Drop Type**: Exact Drop
* **Drop Range**: 3.00

A prefab with a fully set up Pelican Drop object can be found here: [Pelican Drop](https://www.halowaypoint.com/halo-infinite/ugc/prefabs/0c3e683d-e324-4b2a-95c8-71fdf6740c18). An alternative version containing additional objects can be found here: [Machinima Flashlights and Pelican](https://www.halowaypoint.com/halo-infinite/ugc/prefabs/0e92b964-f790-4431-adbd-16be43afb2b8) (requires "Enable Weapon Resupply" to be enabled in the Mode Editor).

*Note: Changing the Symmetrical or Selective channels from "AirDrop Alpha" may affect the timing of the Pelican's arrival, though this has not been verified.*

## Mode Configuration

The functionality of the Pelican Drop is tied to internal events triggered by specific mode settings. In the Mode Editor, the **Firefight → Prevent Item Respawns** option must be set to **True**. While this setting is typically used to prevent the automatic respawn of items, it is required for the Pelican Drop to function. This option is set to **True** by default.

<figure><img src="../../../.gitbook/assets/2026-04-17_HaloInfinite-n5gx.jpg" alt="Cover image"><figcaption><p>The Prevent Item Respawns setting must be enabled in the Mode Editor.</p></figcaption></figure>

## Constraints and AI Behavior

### Pilot AI Characteristics

The Pelican is piloted by an invisible, frictionless AI entity that has no physical size but is still affected by gravity. This pilot cannot be removed from the vehicle through standard methods, such as flipping the vehicle. If the pilot AI is damaged or deleted, the Pelican vehicle will also be deleted.

<figure><img src="../../../.gitbook/assets/HaloInfinite_mJ25QayzqK.jpg" alt="Cover image"><figcaption><p>The pilot of the Pelican is an invisible AI entity.</p></figcaption></figure>

### Flight and Scripting Limitations

The Pelican Drop is designed to trigger at the start of gameplay; delaying or activating the drop via command is not currently possible. Furthermore, there are specific constraints regarding vehicle usage in different modes:

* **Firefight modes**: Attempting to pilot a Pelican using a vehicle type reference in Firefight modes will result in the pilot being automatically kicked out of the vehicle. Once this happens, the vehicle may become un-enterable via scripts.
* **BTB:Slayer**: Flying the Pelican vehicle is possible in BTB:Slayer on developer-made maps.

{% hint style="warning" %}
Attempting to pilot a Pelican in Firefight modes via a vehicle type reference will result in the pilot being automatically kicked out of the vehicle.
{% endhint %}

#### Scripting Note: Player Respawns

When using scripts to facilitate players entering a Pelican, players who have been revived in FFKOTH may encounter issues where they remain on a death screen. This occurs because internal scripting may not automatically unblock respawns after a player is revived. To resolve this, add an `Unblock Respawns For Player` node immediately after teleporting the player to ensure the "enter" sequence proceeds correctly.

#### Scripting Note: Entering the Pelican

Because the Pelican has no entering animation, players are teleported inside the vehicle instantly. If the entry script is triggered by a button press (such as "E" to activate a switch), the player may be immediately ejected because the "enter" action and "switch activation" share the same input. To resolve this, add a small delay to the script to ensure the player can release the button before they are entered into the vehicle.

*Note: "Entering" the Pelican in this context means respawning the player as the Pelican vehicle type at the Pelican's location, as standard `Attempt To Enter Vehicle` nodes may not function.*

***

## Source Data

* Discord thread: [Pelican Drops on Forge maps](https://discord.com/channels/220766496635224065/1210616741756014632/1210616741756014632)

#### <mark style="color:green;">Contributors</mark>

Okom\
thescriptinator\
Dj_HurstyDNB\
SpawnOfTheDeep\
Josh
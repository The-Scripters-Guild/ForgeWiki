---
description: >-
  Explains how to implement Pelican Drops on Forge maps using specific
  object settings and Firefight: King of the Hill mode configurations.
---

# Pelican Drops on Forge maps

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The Pelican Drop object allows for the spawning of Pelican vehicles on Forge-created maps. This functionality is currently tied to specific game mode configurations and requires a specialized setup to trigger correctly.

## Implementation Requirements

To utilize Pelican Drops, a map must have a working Firefight: King of the Hill setup. The drops will only spawn when the map is loaded using a Firefight: King of the Hill mode variant.

### Object Settings

The "Pelican Drop" object must be placed on the map with specific properties to ensure functionality. While the object can be found on hidden object maps, its settings must be configured as follows:

* **Cargo Drop Type**: Exact Drop (this setting is mandatory)
* **Spawn Properties**: Default
* **Symmetrical Channel**: AirDrop Alpha
* **Selective Channel**: AirDrop Alpha
* **Drop Range**: 3.00

<figure><img src="../../../.gitbook/assets/HaloInfinite_ecJMgmvXcj.jpg" alt="Cover image"><figcaption><p>The Pelican Drop object must be placed with specific settings to trigger the spawn.</p></figcaption></figure>

### Mode Editor Configuration

In addition to the object settings, the game mode itself must be configured through the Mode Editor. Specifically, the "Firefight → Prevent Item Respawns" option must be set to **TRUE**. Although this may seem counter-intuitive, the Pelican Drop's functionality is tied to the internal events triggered by this specific mode setting.

<figure><img src="../../../.gitbook/assets/2026-04-17_HaloInfinite-n5gx.jpg" alt="Cover image"><figcaption><p>The mode editor requires the Firefight Prevent Item Respawns option to be set to true for the Pelican Drop to function.</p></figcaption></figure>

## Vehicle and Pilot Behavior

The Pelican vehicles produced by these drops possess unique behaviors regarding their pilot AI and how they interact with players in specific game modes.

### Pilot AI Properties

Each Pelican is controlled by an internal pilot AI. This AI has the following characteristics:

* **Physicality**: The AI is an invisible, frictionless entity with no physical size, though it is still affected by gravity.
* **Persistence**: The AI cannot be kicked out of the vehicle through standard gameplay actions, such as flipping the vehicle.
* **Dependency**: The Pelican is dependent on the AI's existence; if the pilot AI is damaged or deleted, the Pelican vehicle will also be deleted.

<figure><img src="../../../.gitbook/assets/HaloInfinite_mJ25QayzqK.jpg" alt="Cover image"><figcaption><p>The Pelican's pilot is an invisible AI that cannot be removed from the vehicle.</p></figcaption></figure>

### Gameplay Constraints

There are several limitations regarding how and when Pelican Drops can be used:

* **Timing**: The Pelican Drop triggers only at the start of gameplay. It cannot be delayed or activated on command via scripting.
* **Pilot Ejection**: In Firefight: King of the Hill mode, attempting to pilot a Pelican will cause the player to be automatically ejected. Once ejected, the vehicle cannot be re-entered using scripts that attempt to place a player into the vehicle. However, flying these vehicles is reportedly possible in other modes, such as Battle Royale: Slayer, on development maps.

{% hint style="info" %}
When scripting players to enter a Pelican, players who have been revived in Firefight: King of the Hill may encounter issues where their respawns remain internally blocked. To resolve this, use the `Unblock Respawns For Player` node immediately after teleporting the player to ensure they can successfully occupy the vehicle.
{% endhint %}

***

## Source Data

* Discord thread: [Pelican Drops on Forge maps](https://discord.com/channels/220766496635224065/1210616741756014632/1210616741756014632)

#### <mark style="color:green;">Contributors</mark>

Okom\
Dj_HurstyDNB\
SpawnOfTheDeep\
thescriptinator\
Josh
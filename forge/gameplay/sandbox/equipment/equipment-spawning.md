---
description: >-
  Explanations regarding various methods and topics for spawning
  equipment within Halo Infinite via Forge objects.
---

# Equipment Spawning

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article provides explanations regarding topics related to equipment spawning, covering the different ways equipment can be spawned in Halo Infinite via Forge objects.

## Standard Spawners

### Equipment Dispenser

The Equipment Dispenser is the main spawner for base equipment. It's intended to be placed on the ground.

The standard setup for an Equipment Dispenser is as follows:
* **Equipment:** (user-defined)
* **Static Selection:** Enabled
* **Legendary Variants:** Exclude
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** EquipmentPadPlacementKey

{% hint style="info" %}
Read about the details about the Static Selection and Spawn Properties [here](../spawn-properties.md).
{% endhint %}

### Power Equipment Pad

The Power Equipment Pad is the main spawner for power equipment. It's intended to be placed on the ground.

The standard setup for a Power Equipment Pad is as follows:
* **Equipment:** (user-defined)
* **Static Selection:** Enabled
* **Tier:** Power
* **Legendary Variants:** Exclude
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** On
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** PowerUpPadPlacementKey

## Specialized Spawners

### Equipment Pod

The Equipment Pod is not used in standard setups, but it still follows the same logic as other spawners. It's only used in Big Team Battle and Last Spartan Standing as ordnance drops. Properties not listed don't matter.

The standard setup for an Equipment Pod is as follows:
* **Equipment:** (user-defined)
* **Static Selection:** Disabled
* **Tier:** Any
* **Legendary Variants:** Exclude
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** On
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** OrdnancePodPlacementKey

### Classic Equipment Spawn

The Classic Equipment Spawn is not used in standard setups, but it still follows the same logic as other spawners. It's only used in Infection as the main way of spawning equipment. Properties not listed don't matter.

The standard setup for a Classic Equipment Spawn is as follows:
* **Equipment:** (user-defined)
* **Static Selection:** Disabled
* **Tier:** Any
* **Legendary Variants:** Exclude
* **Randomize:** Every Game
* **Symmetrical Channel:** (user-defined)
* **Navpoint:** Off
* **Initial Spawn Delay:** (user-defined)
* **Spawn Properties:** 343 Default
* **Selective Channel:** None
* **Seed Sequence Key:** EquipmentPadPlacementKey

***

## Source Data

* Discord thread: [Equipment Spawning](https://discord.com/channels/220766496635224065/1535166833781645413/1535166833781645413)

#### <mark style="color:green;">Contributors</mark>

Okom

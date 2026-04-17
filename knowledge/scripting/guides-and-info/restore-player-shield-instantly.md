---
description: >-
  Use the Set Player Overshield node with a 0.00 Percent Shield value
  to immediately restore a player's shield to maximum.
---

# Restore Player Shield Instantly

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While standard shield regeneration typically occurs over time, it is possible to bypass this process through scripting. By manipulating overshield nodes or recharge traits, developers can trigger immediate shield restoration.

## Implementation via Overshield Node

The most effective way to restore a shield instantly is to use the [Set Player Overshield](https://wiki.thescriptersguild.com/scripting/nodes/players/set-player-overshield) node. Although this node is primarily intended to add extra protection, its underlying logic can be leveraged to reset the standard shield bar.

### Node Configuration

To achieve a full shield restoration without adding additional overshield protection, configure the node with the following setting:

* **Percent Shield**: `0.00`

<figure><img src="assets/2026-03-02_HaloInfinite-bE7M-wt5u.png" alt="Restore Player Shield Instantly source image"><figcaption><p>Source image from the original research thread.</p></figcaption></figure>

## Underlying Mechanics

The ability to use this node for instant regeneration is due to the specific execution order of the overshield logic. When the `Set Player Overshield` node is triggered, the system performs two distinct actions in sequence:

1. The player's current shield is immediately set to its maximum value.
2. The specified overshield amount is then applied on top of that maximum value.

By providing a `Percent Shield` value of `0.00`, the second step adds no additional overshield protection, resulting in only an instant reset to the player's maximum standard shield.

{% hint style="success" %}
This technique is a useful workaround for mechanics that require an immediate "recharge" effect without the player gaining the extra durability associated with overshields.
{% endhint %}

## Alternative Method via Shield Recharge Trait

For a near-instantaneous recharge (approximately 0.2 seconds) without using the overshield node, you can manipulate the `Trait: Shield Recharge` node. This method adjusts the timing and speed of the standard regeneration process.

### Implementation

To use this method, you must declare and apply a trait set:

* Use the `Declare Trait Set` node to create a set containing the shield recharge trait.
* Use the `Apply Trait Set` node (or its variants) to apply the set to a player.

### Configuration

To minimize the delay before regeneration begins and maximize the recharge speed, use the following scalar values:

* **Recharge Delay Scalar**: `-1.00` (results in 0.000 s cooldown)
* **Recharge Rate Scalar**: `10.00` (results in 0.2000 s recharge time)

***

## Source Data

* Discord thread: [Restore Player Shield Instantly](https://discord.com/channels/220766496635224065/1478032097200574626/1478032097200574626)

#### <mark style="color:green;">Contributors</mark>

Okom
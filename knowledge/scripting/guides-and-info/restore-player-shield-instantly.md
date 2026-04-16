---
description: >-
  Use the Set Player Overshield node with a 0.00 Percent Shield value
  to immediately restore a player's shield to maximum.
---

# Restore Player Shield Instantly

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While standard shield regeneration typically occurs over time, it is possible to bypass this process through scripting. By manipulating the overshield node, developers can trigger an immediate restoration of a player's shield capacity.

## Implementation via Overshield Node

The most effective way to restore a shield instantly is to use the [Set Player Overshield](https://wiki.thescriptersguild.com/scripting/nodes/players/set-player-overshield) node. Although this node is primarily intended to add extra protection, its underlying logic can be leveraged to reset the standard shield bar.

### Node Configuration

To achieve a full shield restoration without adding additional overshield protection, configure the node with the following setting:

* **Percent Shield**: `0.00`

<figure><img src="assets/2026-03-02_HaloInfinite-bE7M.png" alt="Restore Player Shield Instantly source image"><figcaption><p>Source image from the original research thread.</p></figcaption></figure>

## Underlying Mechanics

The ability to use this node for instant regeneration is due to the specific execution order of the overshield logic. When the `Set Player Overshield` node is triggered, the system performs two distinct actions in sequence:

1. The player's current shield is immediately set to its maximum value.
2. The specified overshield amount is then applied on top of that maximum value.

By providing a `Percent Shield` value of `0.00`, the second step adds no additional overshield protection, resulting in only an instant reset to the player's maximum standard shield.

{% hint style="success" %}
This technique is a useful workaround for mechanics that require an immediate "recharge" effect without the player gaining the extra durability associated with overshields.
{% endhint %}

***

## Source Data

* Discord thread: [Restore Player Shield Instantly](https://discord.com/channels/220766496635224065/1478032097200574626/1478032097200574626)

#### <mark style="color:green;">Contributors</mark>

Okom
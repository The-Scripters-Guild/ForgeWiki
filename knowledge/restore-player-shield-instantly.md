---
description: >-
  Explains how to use the Set Player Overshield node to achieve
  instantaneous shield restoration.
---

# Restore Player Shield Instantly

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While shield regeneration typically occurs over time, scripting allows for the immediate replenishment of a player's shield capacity.

## Instant Shield Refill Method

The [Set Player Overshield](https://wiki.thescriptersguild.com/scripting/nodes/players/set-player-overshield) node can be leveraged to bypass standard regeneration delays and provide an immediate shield refresh.

<figure><img src="assets/2026-03-02_HaloInfinite-bE7M.png" alt="Restore Player Shield Instantly source image"><figcaption><p>Source image from the original research thread.</p></figcaption></figure>

### Parameter Configuration

To trigger an instant restoration, the node must be configured with the following value:

* **Percent Shield**: `0.00`

#### Internal Logic

The effectiveness of this method relies on the node's internal behavior. The overshield system always sets the player's shield back to its maximum capacity before applying any additional overshield on top of that value. By setting the Percent Shield to `0.00`, the player receives their maximum base shield instantly without an additional overshield layer being applied.

## Node Behavior and Mechanics

Using the node in this manner provides a reliable way to manage player resources during gameplay. Because the shield is reset to maximum before the overshield is applied, this technique ensures a full base shield regardless of the player's current shield level.

{% hint style="success" %}
Setting the Percent Shield value to 0.00 is the specific requirement for bypassing the recharge delay and providing a full, instant shield.
{% endhint %}

***

## Source Data

* Discord thread: [Restore Player Shield Instantly](https://discord.com/channels/220766496635224065/1478032097200574626/1478032097200574626)

#### <mark style="color:green;">Contributors</mark>

Okom
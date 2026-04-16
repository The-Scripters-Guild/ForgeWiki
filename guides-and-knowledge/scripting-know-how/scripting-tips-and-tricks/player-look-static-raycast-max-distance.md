---
description: >-
  Documentation regarding the maximum detection distance and default hit
  position behavior for the Get Player Look Static Raycast Result node.
---

# Player Look Static Raycast Max Distance

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The [Get Player Look Static Raycast Result](https://wiki.thescriptersguild.com/scripting/nodes/math/get-player-look-static-raycast-result) node has specific constraints regarding its detection range and the data it returns when a raycast fails to hit a target.

## Detection Range

The "Hit Detected" pin on the Get Player Look Static Raycast Result node is limited by distance. The node will output `TRUE` from the Hit Detected pin only when the target is within a maximum distance of 1000.00 units.

## Default Hit Position

If the raycast fails to find a valid hit, the node provides a default "hit position."

### Interpreting Distance on Miss

When no hit is detected, the node's default hit position is set to `0,0,0`. Consequently, if you are measuring the distance from the player to the reported hit position during a failed raycast, the resulting value represents the distance between the player and the world origin (`0,0,0`).

<figure><img src="../../../.gitbook/assets/player-look-static-raycast-max-distance-source-1451609883165331609-1451609884306047097-2025-12-19-haloinfinite-vvkl.png" alt="Player Look Static Raycast Max Distance source image"><figcaption><p>Source image from the original research thread.</p></figcaption></figure>

For instance, a reported distance of 511.33 units in a scenario where no hit is detected indicates the distance from the player to the `0,0,0` coordinate.

{% hint style="success" %}
The "Hit Detected" pin will only return `TRUE` for targets within 1000.00 units of the player.
{% endhint %}

***

## Source Data

* Discord thread: [https://discord.com/channels/220766496635224065/1451609883165331609/1451609883165331609](https://discord.com/channels/220766496635224065/1451609883165331609/1451609883165331609)

#### <mark style="color:green;">Contributors</mark>

Okom\\

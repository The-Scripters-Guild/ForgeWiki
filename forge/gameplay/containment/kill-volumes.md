---
description: >-
  Kill Volumes are boundaries that damage the player when entered.
---

# Kill Volumes

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Kill Volumes are boundaries designed to damage the player when they enter their area. They serve as various environmental hazards or containment measures throughout a map.

## Volume Types

### Kill Volumes
These volumes cause instant death upon entry and are most often used in areas where the player's death is expected, such as falling into water or entering a death pit.

{% hint style="warning" %}
Kill Volumes should not be used in areas where the player might be abruptly killed without warning.
{% endhint %}

### Soft Kill Volumes
The Soft Kill Volume (or "Soft Kill") utilizes a 10-second countdown timer; once the timer reaches zero, the player instantly dies. This type of volume is often placed on top of tall structures as a containment measure when using a [Blocker](blockers.md) would be too obvious. While it is not common, soft kills can also be used at map edges to warn players against further traversal.

#### Map Boundary Behavior
At the edges of each 4000x4000x1500-unit [Forge canvas](../../forge-basics-and-ui/loading-into-forge/forge-canvases.md), there is a prebuilt soft kill boundary and a soft barrier that prevents player movement outside the canvas bounds. This soft kill acts identically to a standard Soft Kill Volume.

## Safe Volumes
Safe Volumes can be placed inside death zones to create specific safe spaces where volume effects are ignored. 

* `Safe Volume` ignores the effect of a Kill Volume.
* `Soft Kill Safe Volume` ignores the effect of a Soft Kill Volume.

***

## Source Data

* Discord thread: [Kill Volumes](https://discord.com/channels/220766496635224065/1538532501033713705/1538532501033713705)

#### <mark style="color:green;">Contributors</mark>

Okom
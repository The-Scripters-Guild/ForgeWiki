---
description: >-
  The Killed Unit Position pin in the On AI Unit Killed node outputs a
  Vector3 that is 10x smaller than the actual Forge position.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Users may encounter spatial inaccuracies when attempting to use the position data from the `On AI Unit Killed` node, as the coordinate values do not match standard Forge scaling.

## Coordinate Scaling Discrepancy

The `Killed Unit Position` pin in the `On AI Unit Killed` node outputs a `Vector3` that is 10x smaller than the actual position values used by Forge. This discrepancy means that if the raw output is used directly for spawning effects or moving objects, the coordinates will be incorrect.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Node setup"><figcaption><p>The node graph demonstrates the connection between the On AI Unit Killed node and a Scale Vector node.</p></figcaption></figure>

### Impact on Spatial Logic

Because the vector is scaled down, any logic relying on this position will place objects or effects at a location far from the intended event if the vector is not corrected.

## Correcting the Output

To obtain the correct position used by Forge, the output from the `Killed Unit Position` pin must be adjusted through additional nodes.

### Required Node Configuration

To resolve the scaling issue, the following configuration is required:

* Feed the `Vector3` from the `Killed Unit Position` pin into a `Scale Vector` node.
* Set the `Scalar` input of the `Scale Vector` node to `10.00`.

{% hint style="warning" %}
The `Killed Unit Position` pin must always be fed into a `Scale Vector` node with a `10.00` scalar to ensure the resulting position is accurate.
{% endhint %}

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="Debug output"><figcaption><p>Debug text displays the difference between the original and expected death positions.</p></figcaption></figure>

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
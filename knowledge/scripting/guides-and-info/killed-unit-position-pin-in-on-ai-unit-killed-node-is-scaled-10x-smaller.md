---
description: >-
  The Killed Unit Position pin in the On AI Unit Killed node outputs a
  Vector3 that is 10x smaller than the expected Forge position.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The `On AI Unit Killed` node provides a `Killed Unit Position` pin intended to return the location where a unit died. However, the Vector3 output from this pin is scaled incorrectly relative to standard Forge coordinates.

## Vector3 Scaling Discrepancy

The `Killed Unit Position` pin outputs a [Vector3](../../../scripting/nodes/variables-basic/vector3.md) that is 10x smaller than the actual position used by Forge. This discrepancy means that using the raw output directly for spatial logic will result in coordinates being positioned near the map origin rather than at the unit's death site.

### Correcting the Output

To obtain the correct position, the Vector3 from the `Killed Unit Position` pin must be processed through a `Scale Vector` node. Using a scalar value of `10.00` will scale the vector back to the intended Forge coordinate system.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Node graph demonstration"><figcaption><p>The node graph shows the On AI Unit Killed pin being passed into a Scale Vector node with a 10.00 scalar to correct the position.</p></figcaption></figure>

## Implementation Requirements

When scripting events that rely on the location of a unit's death—such as spawning effects, setting object positions, or triggering proximity logic—this scaling step is required.

{% hint style="info" %}
To ensure accurate positioning, the `Killed Unit Position` pin should be fed into a `Scale Vector` node with a `10.00` scalar.
{% endhint %}

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="In-game debug view"><figcaption><p>Debug text in-game illustrates the difference between the original death position and the scaled value.</p></figcaption></figure>

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
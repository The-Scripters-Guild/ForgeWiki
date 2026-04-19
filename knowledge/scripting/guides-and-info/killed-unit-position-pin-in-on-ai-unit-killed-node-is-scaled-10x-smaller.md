---
description: >-
  The Killed Unit Position pin in the On AI Unit Killed node outputs a
  Vector3 that is 10x smaller than standard Forge positions.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The `On AI Unit Killed` node is a common event trigger in Forge scripting, but the spatial data it provides requires manual adjustment to align with the rest of the engine.

## Coordinate Scaling Issue

The `Killed Unit Position` pin within the `On AI Unit Killed` node does not output coordinates that match the standard scaling used by Forge. Instead, the `Vector3` produced by this pin is 10x smaller than the actual position of the unit at the time of death.

### Discrepancy in Vector3 Values

Because the output is scaled down, using the raw value for positioning objects, spawning effects, or calculating distances will result in significant errors. The values provided by the node are a fraction of the intended world coordinates.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt=""Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller source image"><figcaption><p>In-game debug text displays the discrepancy between the scaled death position and the actual coordinates.</p></figcaption></figure>

## Correcting the Position Output

To use the death position accurately within a script, the output must be scaled back up to its intended value.

### Using the [Scale Vector](../../../scripting/nodes/math/scale-vector.md) Node

The recommended method for correcting this value is to pass the `Vector3` from the `Killed Unit Position` pin into a `Scale Vector` node. By setting the `Scalar` input of the `Scale Vector` node to `10.00`, the coordinate is multiplied by the necessary factor to return it to the standard Forge scale.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt=""Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller source image"><figcaption><p>The node graph shows the implementation of a Scale Vector node to correct the position output from the On AI Unit Killed node.</p></figcaption></figure>

{% hint style="warning" %}
You must always feed the `Killed Unit Position` vector into a `Scale Vector` node with a scalar of `10.00` to ensure the output position is correct.
{% endhint %}

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
---
description: >-
  The "Killed Unit Position" output in the On AI Unit Killed node is
  scaled 10x smaller than standard Forge coordinates.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The `On AI Unit Killed` node provides location data via its "Killed Unit Position" pin, but this data is not returned in the standard coordinate scale used throughout Forge.

## Position Scaling Issue

The `Vector3` output from the "Killed Unit Position" pin is 10x smaller than the actual position used by Forge. Because of this discrepancy, any logic attempting to use this position for spawning objects, moving units, or calculating distances will be inaccurate unless the vector is adjusted.

### Required Mathematical Correction

To obtain the correct position, the output from the "Killed Unit Position" pin must be processed through a [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node.

* **Input Vector:** The "Killed Unit Position" from the `On AI Unit Killed` node.
* **Scalar Value:** 10.00.

{% hint style="warning" %}
The "Killed Unit Position" pin should be fed into a [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node with a 10.00 scalar to ensure the output matches standard Forge positions.
{% endhint %}

## Node Implementation

When setting up a script to react to a unit's death, the scaling correction should be applied before passing the position to other nodes.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Node graph showing the correction workflow"><figcaption><p>A node graph demonstrating the use of a Scale Vector node to correct the killed unit position.</p></figcaption></figure>

A typical workflow involves taking the raw position from the `On AI Unit Killed` node, applying the 10.00 scale, and then using that corrected value for tasks such as updating variables or setting the position of a new object.

### Visualizing the Discrepancy

Without the mathematical correction, the reported death location will be significantly offset from the actual location where the unit died.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="Visual debug information"><figcaption><p>Debug information showing the discrepancy between the scaled position and the actual position.</p></figcaption></figure>

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
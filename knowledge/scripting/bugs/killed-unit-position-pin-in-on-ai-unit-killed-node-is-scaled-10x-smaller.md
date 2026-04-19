---
description: >-
  The Killed Unit Position pin in the On AI Unit Killed node outputs
  coordinates that are 10x smaller than standard Forge coordinates.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

In Halo Infinite Forge scripting, the [On AI Unit Killed](../../../scripting/nodes/events-ai/on-ai-unit-killed.md) node is used to trigger events when an AI unit dies. However, the positional data provided by this node does not align with the standard coordinate system used by other Forge nodes.

## Scaling Behavior of On AI Unit Killed

The `Killed Unit Position` pin within the `On AI Unit Killed` node outputs a [Vector3](../../../scripting/nodes/variables-basic/vector3.md) that is 10x smaller than the actual position used by Forge. If this vector is used directly to place objects, spawn effects, or set variables, the resulting position will be significantly offset from the actual death location.

### Correcting the Position Output

To obtain the correct coordinates, the output from the `Killed Unit Position` pin must be passed through a math node to restore its proper scale.

#### Required Node Setup

The standard workflow to correct this discrepancy involves using the [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node. The `Killed Unit Position` pin should be connected to the `Vector` input of a `Scale Vector` node, with the `Scalar` input set to `10.00`. The `Result` of the `Scale Vector` node can then be used for accurate positioning in subsequent logic.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Scripting graph showing scale correction"><figcaption><p>The scripting graph demonstrates connecting the `On AI Unit Killed` node to a `Scale Vector` node with a scalar of 10.00 to correct the death position.</p></figcaption></figure>

## Visual Representation of the Discrepancy

The difference between the raw output and the corrected position is clearly visible when comparing debug values or observing the physical placement of scripted elements.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="In-game debug view"><figcaption><p>Debug text in the game view displays the difference between a scaled and unscaled death position.</p></figcaption></figure>

{% hint style="warning" %}
Always feed the `Killed Unit Position` pin into a `Scale Vector` node with a `10.00` scalar to ensure your script targets the correct location.
{% endhint %}

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
---
description: >-
  The "Killed Unit Position" pin in the On AI Unit Killed node outputs a Vector3
  that is 10x smaller than standard Forge coordinates.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The [On AI Unit Killed](../../../scripting/nodes/events-ai/on-ai-unit-killed.md) node provides event data when an AI unit is defeated, including the location of the death. However, the position data provided by this node requires a specific correction to be used accurately within Forge.

## Vector3 Coordinate Discrepancy

The "Killed Unit Position" pin in the `On AI Unit Killed` node outputs a Vector3 value that is 10x smaller than the actual position used by Forge. Because of this scaling discrepancy, using the raw output directly for spatial logic—such as spawning effects or moving objects—will result in coordinates that are significantly offset from the actual death location.

### Correcting the Position

To obtain the correct position, the output from the "Killed Unit Position" pin must be passed through a [Scale Vector](../../../scripting/nodes/math/scale-vector.md) node.

* Connect the "Killed Unit Position" pin to the `Vector` input of a `Scale Vector` node.
* Set the `Scalar` value to `10.00`.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Node workflow"><figcaption><p>The node workflow demonstrates scaling the killed unit position by a factor of 10.00 to ensure coordinate accuracy.</p></figcaption></figure>

## Visual Comparison

The difference between the unscaled output and the corrected coordinates can be observed through debug text. The original death position values are a tenth of the magnitude of the actual Forge coordinates.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="Debug output comparison"><figcaption><p>Debug text shows the difference between the unscaled death position and the corrected coordinates.</p></figcaption></figure>

{% hint style="warning" %}
To ensure spatial accuracy in your scripts, always feed the "Killed Unit Position" pin into a Scale Vector node with a 10.00 scalar.
{% endhint %}

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom

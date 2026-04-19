---
description: >-
  The "Killed Unit Position" pin in the On AI Unit Killed node outputs
  a Vector3 that is 10x smaller than the actual Forge position.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The "On AI Unit Killed" node is used to trigger logic when an AI unit is defeated. However, the coordinate data provided by the "Killed Unit Position" pin does not return standard Forge coordinates, which can cause errors in spatial logic if not corrected.

## Coordinate Scaling Issue

The "Killed Unit Position" pin outputs a Vector3 that is 10x smaller than the actual position used within Forge. Because of this discrepancy, using the pin's output directly for positioning tasks—such as spawning objects or determining death locations—will result in coordinates that are significantly offset from the true location.

## Correcting the Output

To ensure accuracy, the output from the "Killed Unit Position" pin must be adjusted to match Forge's standard coordinate scale.

### Using the Scale Vector Node

The most effective way to rectify this is to pass the Vector3 through a [Scale Vector](https://wiki.thescriptersguild.com/scripting/nodes/math/scale-vector) node.

#### Required Scalar Value

The [Scale Vector](https://wiki.thescriptersguild.com/scripting/nodes/math/scale-vector) node must be configured with a scalar of 10.00 to return the Vector3 to its accurate Forge-standard coordinates.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Node workflow"><figcaption><p>The node workflow demonstrates scaling the output of the On AI Unit Killed node by 10.00 to correct the position.</p></figcaption></figure>

## Visual Verification

This scaling behavior can be observed through debug text in-game, where the reported coordinates appear much smaller than the expected Forge values.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="In-game debug text"><figcaption><p>In-game debug text shows that the original death position is scaled 10x smaller than the actual location.</p></figcaption></figure>

{% hint style="warning" %}
Always feed the "Killed Unit Position" Vector3 into a Scale Vector node with a 10.00 scalar to ensure correct spatial placement.
{% endhint %}

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
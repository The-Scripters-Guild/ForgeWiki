---
description: >-
  The "Killed Unit Position" pin in the [On AI Unit
  Killed](https://wiki.thescriptersguild.com/scripting/nodes/events-ai/on-ai-unit-killed)
  node outputs a Vector3 that is 10x smaller than what the.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The `On AI Unit Killed` event node provides a `Killed Unit Position` pin, but this vector does not represent the true coordinates of the death event within the Forge world. Instead, the value is scaled down, requiring an adjustment to match the position data used by other Forge systems.

## Identifying the Scaling Discrepancy

The `Killed Unit Position` pin returns a `Vector3` that is exactly 10 times smaller than the actual position value Forge uses internally. When this pin is used directly for positioning objects or printing values, the results will be incorrect unless corrected.

### Verifying the Output Value

Users can verify this behavior by comparing the output of the pin against known world coordinates or debug prints. The discrepancy is consistently a factor of 10, as shown in the debug output below.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="Debug output showing the position scaling"><figcaption><p>Debug output demonstrating that the original death position from the pin is scaled 10 times smaller than the actual world coordinates.</p></figcaption></figure>

## Correcting the Position with Scale Vector

To obtain the accurate position data, the `Killed Unit Position` pin must be processed through a `Scale Vector` node. The scalar input of this node must be set to 10.00.

* Connect the `Killed Unit Position` pin to the **Vector** input of a `Scale Vector` node.
* Set the **Scalar** input to 10.00.
* Use the **Result** pin of the `Scale Vector` node for the corrected position.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Workflow showing the Scale Vector fix"><figcaption><p>Node layout showing the Scale Vector node connected to the On AI Unit Killed pin with a scalar of 10.00 to correct the position output.</p></figcaption></figure>

{% hint style="success" %}
Always feed the `Killed Unit Position` output into a `Scale Vector` node with a scalar of 10.00 to retrieve the correct world coordinates.
{% endhint %}

Applying this scaling ensures that the position data is compatible with other Forge functions, such as setting object positions or spawning effects at the exact location of the AI unit's death.

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
---
description: >-
  The "Killed Unit Position" pin in the On AI Unit Killed node outputs
  a Vector3 that is 10x smaller than what the actual position is that
  Forge uses.
---

# "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When scripting events around artificial intelligence in Forge, developers frequently rely on the `On AI Unit Killed` node to trigger actions based on enemy deaths. However, the "Killed Unit Position" output pin does not report coordinates directly in the standard Forge spatial system. Instead, it provides a Vector3 value that is compressed by a factor of ten. This discrepancy requires a consistent adjustment step to align positional data with other Forge systems, object placement, or debug displays.

## Understanding the Position Scaling Behavior

The "Killed Unit Position" pin functions as an event data output that passes spatial information from the engine to your script. While the pin successfully transmits the location of the eliminated unit, the vector components are divided by ten relative to how Forge natively calculates world space coordinates. This behavior applies universally to all AI entities and does not vary based on squad type, killing context, or difficulty settings. 

### Correcting the Vector Output

To restore the position to its actual Forge coordinate values, the output vector must be multiplied back into the standard scale. The most reliable method involves routing the pin through a [Scale Vector](../../../scripting/nodes/math/scale-vector) node and configuring the scalar input to `10.00`. This adjustment ensures that downstream nodes, such as object spawners, visual markers, or environmental triggers, receive accurate spatial data.

* [Scale Vector](../../../scripting/nodes/math/scale-vector) node with a `10.00` scalar multiplier restores native Forge coordinates.
* Apply this scaling immediately after capturing the "Killed Unit Position" to prevent coordinate drift in subsequent calculations.

## Practical Application and Debugging

Implementing this correction in your graph requires a straightforward workflow. By connecting the event pin to the scaling node, developers can maintain precise control over where subsequent actions take place. Debug displays and variable assignments also benefit from this normalization, ensuring that logged positions match visual in-game references.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-d8mD.png" alt="Script graph showing the necessary node connections"><figcaption><p>Illustrates a setup or result relevant to "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller and the workflow described in this article.</p></figcaption></figure>

{% hint style="warning" %}
Failing to scale the output vector will cause positional data to appear significantly closer to the origin. Objects spawned at this unadjusted position may cluster near the map center rather than appearing at the actual death site.
{% endhint %}

When verifying the fix in-game, debug text or console outputs will show the transformed coordinates matching the expected range. The scaling operation is computationally inexpensive and should be applied consistently across all scripts that depend on AI death locations.

<figure><img src="../../../.gitbook/assets/2025-12-17_HaloInfinite-lcEr.jpg" alt="In-game debug output comparing original and corrected positions"><figcaption><p>Illustrates a setup or result relevant to "Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller and the workflow described in this article.</p></figcaption></figure>

Integrating this normalization step into your scripting workflow eliminates positional inaccuracies and keeps your logic aligned with Forge's internal coordinate system.

***

## Source Data

* Discord thread: ["Killed Unit Position" Pin in On AI Unit Killed Node is Scaled 10x Smaller](https://discord.com/channels/220766496635224065/1450874812405645402/1450874812405645402)

#### <mark style="color:green;">Contributors</mark>

Okom
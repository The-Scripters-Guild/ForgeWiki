---
description: >-
  Power Sockets can be configured to function as interactive switches
  by detecting when a Power Seed is removed.
---

# Power Sockets as Interactive Switches

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Power Sockets can be repurposed as interactive switches to provide a flexible alternative to standard scriptable switches, particularly when mass-deploying objects via scripting.

## Implementation

To utilize a Power Socket as a switch, enable the `Create With Carriable Attached` option within the object properties. Instead of using [On Object Interacted](../../../scripting/nodes/events-custom/on-object-interacted.md), the switch logic is driven by the [On Socket Removed](../../../scripting/nodes/events-generic-objectives/on-socket-removed.md) node, which triggers when the associated Power Seed is taken.

<figure><img src="../../../.gitbook/assets/image-o3qj.png" alt="Power Socket settings"><figcaption><p>An example of a Power Socket configured as a switch with a 3-second interaction timer.</p></figcaption></figure>

### Setup and Resetting

{% hint style="warning" %}
Due to a known bug, newly placed Power Sockets must be primed to ensure they function correctly with scripting nodes. Toggle the `Use Device Interaction` setting Off and then back On to ensure the socket respects `Removal Hold Time` and `Planting Hold Time` settings.
{% endhint %}

Once the `On Socket Removed` event is detected, the Power Seed can be deleted. To reset the switch for future use, the [Spawn Mode Object](../../../scripting/nodes/game-mode/spawn-mode-object.md) node can be used to replace the current socket with a fresh copy.

#### Scripting Workflow

A typical workflow for a resetting switch involves:
* Detecting the removal via `On Socket Removed`.
* Deleting the Power Seed.
* Creating a weapon at the original location.
* Using `Spawn Mode Object` to replace the socket after a set duration.

<figure><img src="../../../.gitbook/assets/image-d5rp.png" alt="Scripting nodes"><figcaption><p>A script that detects interaction, deletes the seed, and uses `Spawn Mode Object` to reset the socket.</p></figcaption></figure>

## Comparison and Limitations

Compared to a dedicated `Scriptable Switch` object, Power Sockets bypass the direct reference requirement of the `On Object Interacted` node. This allows them to be mass-deployed using `Spawn Mode Object` while still functioning as unique, individual switches. Additionally, Power Sockets allow for customizable activation durations.

### Operational Constraints

While versatile, this method has several limitations:

* **Pickup Requirements:** Power Sockets rely on the ability to pick up weapons; they may not function properly if the `Weapon Pickup` trait is disabled or if `Object Filters` are in use. This makes them unsuitable for scenarios where specific players or teams must be restricted from using the switch.
* **Interaction Reliability:** Depending on the orientation of the socket, the "Take Power Seed" prompt may occasionally be inconsistent.
* **Spawn Behavior:** There are reports that objects created via `Spawn Mode Object` may occasionally fail to appear in the [Object List](../../../scripting/nodes/variables-basic/object-list.md), which can impact the reliability of the reset mechanic.

***

## Source Data

* Discord thread: [Power Sockets as Interactive Switches](https://discord.com/channels/220766496635224065/1474550605103104063/1474550605103104063)

#### <mark style="color:green;">Contributors</mark>

Toast\
Okom
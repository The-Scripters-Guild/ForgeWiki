---
description: >-
  Using Power Sockets and the On Socket Removed node to create
  interactive switches that can be mass-deployed.
---

# Power Sockets as Interactive Switches

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Power Sockets can be repurposed as interactive switches by detecting when a Power Seed is removed from the socket. This method provides an alternative to the dedicated Scriptable Switch object, offering specific advantages for mass-produced interactive elements.

## Implementation

To use a Power Socket as a switch, enable the `Create With Carriable Attached` option in the object properties. The activation is triggered using the [On Socket Removed](../../../scripting/nodes/events-generic-objectives/on-socket-removed.md) node, which detects when a player takes the Power Seed.

### Configuration and Priming

For the socket to function correctly with scripting nodes and respect settings like `Removal Hold Time` and `Planting Hold Time`, it must be primed.

{% hint style="warning" %}
Newly placed Power Sockets require the `Use Device Interaction` setting to be toggled Off and then back On to ensure they work correctly with scripting nodes.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image-y4hk.png" alt="Power Socket properties"><figcaption><p>The object properties for a Power Socket configured to act as a switch.</p></figcaption></figure>

### Resetting the Switch

Once the `On Socket Removed` event triggers, the Power Seed can be deleted. To reset the switch for future use, the [Spawn Mode Object](../../../scripting/nodes/game-mode/spawn-mode-object.md) node can be used to replace the existing socket with a fresh copy.

## Comparison and Limitations

Using Power Sockets offers several differences compared to the standard Scriptable Switch.

### Advantages over Scriptable Switches

* **Mass Deployment:** Unlike [On Object Interacted](../../../scripting/nodes/events-custom/on-object-interacted.md), which requires a direct reference to a specific object, Power Sockets bypass this requirement. This allows them to be deployed in large quantities using `Spawn Mode Object` while still functioning as individual, independent switches.
* **Customizable Behavior:** Power Sockets allow users to set how long it takes to activate the switch and whether or not the object resets.

### Known Constraints

* **Weapon Pickup Requirement:** This method relies on the ability to pick up weapons. It may not function properly if the `Weapon Pickup` trait is disabled or if `Object Filters` are applied.
* **Interaction Prompts:** Depending on the orientation of the socket, players may experience inconsistent "Take Power Seed" prompts.
* **Cloning Reliability:** There have been reports of issues when using `Spawn Mode Object` to clone sockets, where cloned objects may not consistently trigger events or appear correctly in the [Object List](../../../scripting/nodes/variables-basic/object-list.md).

<figure><img src="../../../.gitbook/assets/image-i2hc.png" alt="Scripting logic"><figcaption><p>A script that handles the removal of the Power Seed and resets the Power Socket.</p></figcaption></figure>

***

## Source Data

* Discord thread: [Power Sockets as Interactive Switches](https://discord.com/channels/220766496635224065/1474550605103104063/1474550605103104063)

#### <mark style="color:green;">Contributors</mark>

Toast\
Okom
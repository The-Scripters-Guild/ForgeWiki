---
description: >-
  Leveraging Power Sockets to create mass-deployable interactive
  switches by detecting Power Seed removal.
---

# Power Sockets as Interactive Switches

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Power Sockets can be repurposed to function as a type of interactive switch. By using the removal of an attached Power Seed as a trigger, developers can create switches that are easy to mass-deploy without the direct referencing requirements typical of standard scriptable objects.

## Implementation Method

To configure a Power Socket to act as a switch, the `Create With Carriable Attached` option must be enabled within the object's properties. The logic is then driven by the removal of the Power Seed rather than a direct interaction with the socket itself.

### Triggering and Resetting

The interaction is detected using the [On Socket Removed](../../../scripting/nodes/events-generic-objectives/on-socket-removed.md) node. Once this node triggers, the following workflow is typically implemented:
* Delete the Power Seed.
* Use a [Spawn Mode Object](../../../scripting/nodes/game-mode/spawn-mode-object.md) node to replace the existing socket with a fresh copy of the object to reset the switch.

<figure><img src="../../../.gitbook/assets/image-q4lx.png" alt="Power Socket properties"><figcaption><p>A Power Socket is configured as a switch with an interaction timer set to 3 seconds.</p></figcaption></figure>

{% hint style="warning" %}
Newly placed Power Sockets must be "primed" to function correctly with scripting nodes. To ensure they respect `Removal Hold Time` and `Planting Hold Time` settings, toggle the `Use Device Interaction` setting `Off` and then back `On`.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image-ps4l.png" alt="Scripting node layout"><figcaption><p>A script detects the interaction, deletes the seed, and spawns a replacement socket to reset the switch.</p></figcaption></figure>

## Comparison and Constraints

While using Power Sockets offers several advantages for large-scale map design, it also introduces specific gameplay dependencies and potential limitations.

### Advantages over Scriptable Switches

* **Mass Deployment**: Unlike the dedicated `Scriptable Switch` object, Power Sockets bypass the direct reference requirement of `On Object Interacted`. This allows them to be mass-deployed via `Spawn Mode Object` while still functioning as individual, unique switches.
* **Customization**: Power Sockets allow developers to set specific activation durations and determine whether the object should automatically reset.

### Limitations and Known Issues

* **Weapon Pickup Dependency**: This method relies on the player's ability to pick up weapons. It may not function as intended if `Object Filters` are active or if the `Weapon Pickup` trait has been disabled, which can make it difficult to restrict switch access to specific players or teams.
* **Interaction Reliability**: Depending on the orientation of the socket, the "Take Power Seed" prompt may occasionally be inconsistent.
* **Spawning Issues**: There are reports that objects spawned via `Spawn Mode Object` may sometimes fail to trigger events if the clones are not correctly recognized in the [Object List](../../../scripting/nodes/variables-basic/object-list.md).

***

## Source Data

* Discord thread: [Power Sockets as Interactive Switches](https://discord.com/channels/220766496635224065/1474550605103104063/1474550605103104063)

#### <mark style="color:green;">Contributors</mark>

Toast\
Okom
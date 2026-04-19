---
description: >-
  Using Power Sockets and the On Socket Removed node to create
  mass-deployable interactive switches.
---

# Power Sockets as Interactive Switches

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Power Sockets can be repurposed as a type of interactive switch. This method allows for mass deployment and custom activation timing, offering an alternative to the dedicated Scriptable Switch object.

## Configuration and Interaction

To use a Power Socket as a switch, the "Create With Carriable Attached" option must be enabled in the object's properties. This setup allows the system to detect when the attached Power Seed is removed.

### Object Properties

When configuring the socket, developers can utilize the following settings to control how the switch behaves:

* **Removal Hold Time**: Determines how long a player must interact with the socket to remove the seed.
* **Planting Hold Time**: Determines the duration required to return a seed to the socket.

<figure><img src="../../../.gitbook/assets/image-llj4.png" alt="Power Socket settings"><figcaption><p>An example of a Power Socket configured with a 3-second interaction timer.</p></figcaption></figure>

{% hint style="warning" %}
Due to a known bug, newly placed Power Sockets must be "primed" to function correctly. This is done by toggling the **Use Device Interaction** setting Off and then back On. Failing to do this may prevent the socket from respecting the Removal Hold Time and Planting Hold Time settings.
{% endhint %}

## Implementation and Scripting

The logic for the switch is triggered using the `On Socket Removed` node, which fires once the Power Seed is taken.

### Resetting via Spawn Mode Object

To allow the switch to be used multiple times, the socket can be reset after the interaction occurs. A common workflow involves:

1. Detecting the interaction via `On Socket Removed`.
2. Deleting the Power Seed.
3. Using the `Spawn Mode Object` node to replace the original socket with a fresh copy.

<figure><img src="../../../.gitbook/assets/image-42u5.png" alt="Scripting nodes"><figcaption><p>A script that detects interaction, deletes the seed, and uses Spawn Mode Object to reset the socket.</p></figcaption></figure>

## Advantages and Limitations

Using Power Sockets provides distinct advantages over the standard Scriptable Switch, but it also introduces specific constraints.

### Advantages

* **Mass Deployment**: Unlike the Scriptable Switch, which requires a direct reference for the `On Object Interacted` node, Power Sockets bypass this requirement. This allows them to be mass-deployed using `Spawn Mode Object` while still functioning as individual switches.
* **Custom Timers**: The built-in hold time settings allow for variable interaction speeds.

### Limitations

* **Weapon Pickup Dependency**: This method relies on the ability to pick up weapons. It may not function properly if the **Weapon Pickup** trait is disabled or if **Object Filters** prevent the interaction.
* **Interaction Prompts**: Depending on the orientation of the socket, the "Take Power Seed" prompt can occasionally be inconsistent.
* **Cloning Issues**: There are reports that clones created via `Spawn Mode Object` may sometimes fail to trigger events or may not appear correctly in the [Object List](../../../scripting/nodes/variables-basic/object-list.md).

***

## Source Data

* Discord thread: [Power Sockets as Interactive Switches](https://discord.com/channels/220766496635224065/1474550605103104063/1474550605103104063)

#### <mark style="color:green;">Contributors</mark>

Toast\
Okom
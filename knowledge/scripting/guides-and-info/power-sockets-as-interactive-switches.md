---
description: >-
  Power Sockets can be used as a type of interactive switch.
---

# Power Sockets as Interactive Switches

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

By utilizing the mechanics of Power Seeds and sockets, developers can repurpose Power Sockets to act as interactive switches. This technique provides more flexibility for mass-produced interactive elements than standard switch objects.

## Implementation and Configuration

### Object Settings

To use a Power Socket as a switch, the `Create With Carriable Attached` option must be enabled in the object properties. Interaction is then detected using the [On Socket Removed](../../../scripting/nodes/events-generic-objectives/on-socket-removed.md) node, which triggers when the associated Power Seed is removed from the socket.

<figure><img src="../../../.gitbook/assets/image-q09m.png" alt="Power Socket properties"><figcaption><p>The object properties show the settings required to enable the Power Socket as a switch.</p></figcaption></figure>

{% hint style="warning" %}
Newly placed Power Sockets may require priming to function correctly with scripting nodes and to respect `Removal Hold Time` and `Planting Hold Time` settings. To prime a socket, switch the `Use Device Interaction` setting `Off` and then back `On`.
{% endhint %}

## Comparison and Limitations

### Benefits of the Power Socket Method

Compared to the dedicated Scriptable Switch object, the Power Socket method offers several advantages for level design:

* **Mass Deployment:** It bypasses the direct reference requirement of `On Object Interacted`, allowing switches to be mass deployed via `Spawn Mode Object` while still functioning as individual, independent switches.
* **Customizable Timing:** Power Sockets allow developers to define how long it takes to activate them via hold time settings.
* **Reset Logic:** The method allows for custom control over whether or not the switch resets after use.

### Resetting the Switch

To reset a switch after it has been activated, the `On Socket Removed` trigger can be used to delete the Power Seed and then use `Spawn Mode Object` to replace the socket with a fresh copy.

<figure><img src="../../../.gitbook/assets/image-mb0q.png" alt="Scripting graph for Power Socket switch"><figcaption><p>A script graph demonstrates how to detect the removal of a Power Seed and replace the socket to reset it.</p></figcaption></figure>

### Constraints and Known Issues

While versatile, this method has specific requirements and observed limitations:

* **Weapon Pickup Reliance:** The functionality relies on the ability to pick up weapons. It may not work properly if `Object Filters` are being used or if the `Weapon Pickup` trait is disabled.
* **Orientation and Prompts:** Depending on the orientation of the socket, players may find the "Take Power Seed" interaction prompt to be inconsistent or difficult to trigger.
* **Spawn Mode Reliability:** There are reports that clones generated via `Spawn Mode Object` may occasionally fail to appear correctly in the Object List, which can prevent the expected reset events from running.

***

## Source Data

* Discord thread: [Power Sockets as Interactive Switches](https://discord.com/channels/220766496635224065/1474550605103104063/1474550605103104063)

#### <mark style="color:green;">Contributors</mark>

Toast\
Okom
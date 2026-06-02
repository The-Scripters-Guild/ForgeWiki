---
description: >-
  Describes a behavior where object transform nodes only affect the
  parent object when using Get Objects In Prefab in Custom Games.
---

# Get Objects In Prefab Node Returns Only Parent Object

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When running in Custom Games, using the [Get Objects In Prefab](../../../scripting/nodes/objects/get-objects-in-prefab.md) node with object transformation commands may result in only the parent object being moved, even though the node successfully returns all child objects in the list.

## Transform Behavior Discrepancy

There is a documented discrepancy between how object transformations behave in Forge mode versus Custom Games when utilizing the `Get Objects In Prefab` node. While the node functions as intended by returning a list of all objects within the specified prefab, the subsequent transformation nodes may fail to apply to the individual children.

### Forge vs. Custom Games

In Forge mode, object transform commands (such as "Move Object to Point") applied to the results of `Get Objects In Prefab` function as expected, moving all objects in the prefab simultaneously.

However, in Custom Games, these same transformation nodes appear to only affect the parent object. This behavior has been observed following the May update. It is important to note that the node is still correctly identifying and returning the child objects; for instance, commands like "Set Spawn Order" may still work on the entire list, but transformations and translations do not.

## Recommended Workarounds

Because the transformation system in Custom Games may not properly subscribe child objects to movement commands when they are accessed via a prefab, developers can use alternative methods to target these objects.

### Using User Labels

The most efficient workaround involves the use of User Labels. Applying a User Label to a prefab automatically applies that label to every object contained within that prefab.

{% hint style="info" %}
Applying a User Label to a prefab is a highly effective way to ensure all constituent objects are correctly registered for transformations in Custom Games.
{% endhint %}

By assigning a label to the prefab, you can then use label-based logic to target the objects, which allows the transformation nodes to function correctly on all parts of the prefab in a Custom Game environment.

### Alternative Implementation Methods

If User Labels are not suitable for a specific script, other methods can be used, though they may increase the complexity of the logic:

* **Object Lists:** Declaring and maintaining an explicit object list. While functional, this can add significant bulk to a script.
* **Direct Object References:** Ensuring every object within the prefab has a direct object reference in the script brain. This is noted to be a more "clunky" implementation compared to labeling.

***

## Source Data

* Discord thread: [Get Objects In Prefab Node Returns Only Parent Object](https://discord.com/channels/220766496635224065/1404355060909080606/1404355060909080606)

#### <mark style="color:green;">Contributors</mark>

Riveringston\
Artifice\
green\
Okom\
AddiCt3d 2CHa0s 🎮 💻\
Guild Archivist
---
description: >-
  In Custom Games, object transform nodes may only affect the parent
  object when using the Get Objects In Prefab node.
---

# Get Objects In Prefab Node Returns Only Parent Object

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When using the [Get Objects In Prefab](../../../scripting/nodes/objects/get-objects-in-prefab.md) node in Custom Games, object transformation commands may fail to affect child objects, only applying to the parent object. While the node successfully retrieves the entire list of objects within the prefab, subsequent transform nodes—such as those used for movement—may only execute on the root object.

## Observed Behavior

The issue is specifically noted when running maps in Custom Games. In Forge mode, scripts utilizing `Get Objects In Prefab` followed by transform commands function as expected, with all constituent objects moving simultaneously.

### Transformation Failures in Custom Games

Although the `Get Objects In Prefab` node correctly identifies and returns all objects within a prefab (allowing for successful debug prints or setting spawn orders), transformational logic like `Move Object to Point` often fails to translate the child objects in a live game environment. 

This behavior suggests that while the objects are being retrieved by the script, they may not be properly subscribed to the game systems responsible for handling transformations and translations when running in Custom Games.

## Workarounds

Several methods exist to ensure all objects within a prefab are correctly manipulated during gameplay.

### Applying User Labels

A primary workaround involves applying a [User [Label](../../../scripting/nodes/variables-literals/label.md)](../../../scripting/nodes/variables-basic/user-label.md) to the prefab. Because applying a label to a prefab automatically applies that label to every individual object within that prefab, it appears to ensure the objects are properly subscribed to the necessary transformation systems.

{% hint style="success" %}
Applying a `User `Label`` to a prefab allows the objects to be correctly manipulated by transform nodes in Custom Games, even when using the `Get Objects In Prefab` node.
{% endhint %}

### Alternative Implementation Methods

If User Labels are not suitable for a specific script, other methods can be used, though they may increase script complexity:

* **Manual Object Lists:** Declaring an explicit object list can resolve the issue, though this increases the "bulk" and complexity of the script.
* **Direct Object References:** Ensuring every object within a prefab has its own individual object reference in the script brain is possible, though this is considered a more cumbersome implementation.

***

## Source Data

* Discord thread: [Get Objects In Prefab Node Returns Only Parent Object](https://discord.com/channels/220766496635224065/1404355060909080606/1404355060909080606)

#### <mark style="color:green;">Contributors</mark>

Riveringston\
Artifice\
green\
Okom\
Guild Archivist
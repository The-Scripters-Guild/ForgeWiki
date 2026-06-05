---
description: >-
  I have only noticed this problem when using object transform
  commands so far however I haven't tested it more extensively yet. I
  don't have related footage ATM so I'll write it down. Example
  script:
---

# Get Objects In Prefab Node Returns Only Parent Object

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When using the [Get Objects In Prefab](../../../scripting/nodes/objects/get-objects-in-prefab.md) node in Custom Games, object transformation nodes may only successfully move or rotate the parent object of the prefab. While the node correctly identifies and returns all constituent objects within the prefab, subsequent transformation commands often fail to apply to the child objects.

## Observed Behavior

The issue appears to be a discrepancy in how object transformations are handled between Forge mode and Custom Games. In Forge mode, transformations applied to objects retrieved via a prefab function as expected, affecting all objects in the list. However, in Custom Games, these same transformations may only affect the parent object.

### Discrepancy Between Forge and Custom Games

It is important to note that the `Get Objects In Prefab` node itself continues to return the correct list of objects. This has been observed in instances where other properties, such as spawn order, are set on the retrieved objects; the system correctly identifies and applies these changes to the full list of children.

Testing has revealed several nuances regarding this behavior in Custom Games:

* **List Integrity:** The returned list size is accurate (verifiable via [Get List Size](../../../scripting/nodes/objects/get-list-size.md)), and objects can be successfully cast to the object type.
* **Validity Discrepancies:** Some objects within the returned list may return `FALSE` when checked with the [Get Is Valid Object](../../../scripting/nodes/objects/get-is-valid-object.md) node, even if they are present in the list and can be cast to objects.
* **Direct Access Failure:** Attempting to move a specific child object directly using the [Get Object At Index](../../../scripting/nodes/objects/get-object-at-index.md) node also fails to move the child in Custom Games, mirroring the failure of the loop-based approach.

The failure is specific to the interaction between the retrieved child objects and object transformation nodes (such as `Move Object to Point`) when running in a Custom Game environment. This behavior has been reported as occurring following the May update.

{% hint style="warning" %}
This behavior may not be present when testing in Forge mode. Always verify script behavior in a Custom Game environment to ensure transformations are applying to all intended objects.
{% endhint %}

## Workarounds

Several methods can be used to ensure that all objects within a prefab are correctly transformed in Custom Games.

### Using User Labels

A highly effective workaround involves applying a User Label to the prefab itself. When a User Label is applied to a prefab, that label is automatically applied to every object contained within the prefab.

Applying these labels appears to ensure that the child objects are properly subscribed to the systems responsible for transformations and translations. Once the objects are labeled, transformation nodes should function correctly on all constituent parts of the prefab in Custom Games.

### Manual Reference Methods

If User Labels are not suitable for a specific implementation, other more manual methods can be used to ensure children are transformed:

* **Explicit Object Lists:** Manually declaring an object list to hold the specific objects intended for transformation. While this ensures the transformations work, it can increase the complexity and "bulk" of the script.
* **Script Brain References:** Assigning an object reference within the script brain to every individual object inside the prefab. This ensures the script has a direct connection to each child, though it is considered a more cumbersome implementation.

***

## Source Data

* Discord thread: [Get Objects In Prefab Node Returns Only Parent Object](https://discord.com/channels/220766496635224065/1404355060909080606/1404355060909080606)

#### <mark style="color:green;">Contributors</mark>

Riveringston\
Artifice\
green\
Okom\
AddiCt3d 2CHa0s\
Cookies

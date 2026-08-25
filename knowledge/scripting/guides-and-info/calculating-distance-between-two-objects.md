---
description: >-
  Learn how to use Vector3 positions and math nodes to calculate the
  distance between two objects.
---

# Calculating Distance Between Two Objects

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Finding the distance between two entities requires calculating the difference between their positions and then determining the magnitude of that vector.

## Mathematical Logic

To determine the distance between two objects, you must find the difference between their spatial coordinates and then find the magnitude of that difference.

### Required Nodes

* [Get Object Position](../../../scripting/nodes/math/get-object-position.md): This node is used for both objects to retrieve their current `Vector3` coordinates.
* [Subtract Vectors](../../../scripting/nodes/math/subtract-vectors.md): Plug the position of Object A into **Operand A** and the position of Object B into **Operand B**. This generates a new `Vector3` representing the direction and distance between them.
* [Get Vector Length](../../../scripting/nodes/math/get-vector-length.md): Plug the output of the `Subtract Vectors` node into this node. The resulting `Number` is the distance.

***

## Source Data

* Discord thread: [Calculating Distance Between Two Objects](https://discord.com/channels/220766496635224065/1541699500727468032/1541699500727468032)

#### <mark style="color:green;">Contributors</mark>

Guild Archivist

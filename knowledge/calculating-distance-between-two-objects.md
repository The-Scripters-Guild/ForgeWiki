---
description: >-
  @Guild Archivist what nodes would I need to use to get the distance
  between two objects?
---

# Calculating Distance Between Two Objects

<figure><img src="../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

To determine the distance between two objects, you must calculate the difference between their positions and then find the magnitude of that difference.

## Standard Implementation Workflow

The standard setup for calculating distance involves three primary steps using specific scripting nodes.

### Distance Calculation Steps

1. **Get Position**: Utilize this node for both objects to retrieve their current `Vector3` coordinates.
2. **[Subtract Vectors](../scripting/nodes/math/subtract-vectors.md)**: Plug the position of Object A into **Operand A** and the position of Object B into **Operand B**. This produces a new `Vector3` that represents both the direction and the distance between the two objects.
3. **[Get Vector Length](../scripting/nodes/math/get-vector-length.md)**: Plug the output of the **`Subtract Vectors`** node into this node. The resulting `Number` is your distance.

#### Node Summary

* `Get Position` (required for each object)
* `Subtract Vectors`
* `Get Vector Length`

***

## Source Data

* Discord thread: [Calculating Distance Between Two Objects](https://discord.com/channels/220766496635224065/1541699500727468032/1541699500727468032)

#### <mark style="color:green;">Contributors</mark>

Mr Multibit (Sometimes)
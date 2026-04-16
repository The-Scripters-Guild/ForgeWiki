---
description: >-
  A technique for executing multiple conditional branches and a final
  action without duplicating nodes or event triggers.
---

# N Iterations Skip

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The `N Iterations Skip` pattern is a method used to execute various conditional logic paths and then perform a single, centralized action upon their completion. This is achieved by using a `For N Iterations` node set to a single iteration, allowing the developer to avoid attaching duplicate nodes to every individual branch or creating multiple separate event triggers.

## Centralizing Logic with Single Iterations

When a workflow requires one of several different actions to occur followed by a common final step—such as setting a player message and then teleporting the player—standard branching often requires duplicating the final step onto every possible branch. This can lead to cluttered circuits and redundant logic.

By setting a `For N Iterations` node to 1 iteration, the `Execute Iteration` pin can drive multiple branches. Once those branches have processed, the `On Completion` pin triggers the final sequence.

### Managing Data Flow

A known limitation of this pattern is that data cannot be passed automatically from the triggered iteration chain to the completion chain. To move information from the branch logic to the final action, developers should use local or object scope variables to store the necessary data during the iteration and retrieve it once the completion chain begins.

{% hint style="success" %}
This pattern is particularly useful for centralizing complex logic, such as assault mechanics or UI updates, by reducing the total node count.
{% endhint %}

## Execution Order and Comparisons

This method can be further optimized by passing numbers through custom events to act as stand-ins for booleans. Using numbers allows for more than two potential outcomes while maintaining a low node count.

While this approach is highly efficient for reducing clutter, it differs from `For N Iterations Stacks` in terms of control:

* **Execution Order**: This method does not provide direct control over the execution order. While the order remains deterministic, it is not as easily influenced as it is in a stack-based configuration.
* **Complexity**: `For N Iterations Stacks` are considered superior when specific control over the sequence of branch execution is required.

***

## Source Data

* Discord thread: [https://discord.com/channels/220766496635224065/1045952137953284106/1045952137953284106](https://discord.com/channels/220766496635224065/1045952137953284106/1045952137953284106)

#### <mark style="color:green;">Contributors</mark>

Agent Zero85\
Kwatzy\
TheProgrammer163\
Captain Punch\
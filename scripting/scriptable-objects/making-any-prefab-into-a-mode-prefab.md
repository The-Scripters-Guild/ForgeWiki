---
description: >-
  Learn how to convert standard prefabs, including those with static
  objects, into Mode Prefabs using two different methods.
---

# Making any Prefab into a Mode Prefab

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While some prefabs may contain static objects that prevent them from being classified as modes, there are specific workflows available to convert any prefab into a Mode Prefab.

## Conversion Methods

There are two primary ways to convert an existing prefab into a Mode Prefab.

### Adding a Mode Brain

The most direct way to convert an existing prefab is to modify its components:

* Add a `Mode Brain` to the existing prefab.
* Save the prefab.

Once these steps are completed, the prefab will be converted and classified as a Mode.

### Group Selection

A second method involves the specific order in which objects are selected before being prefabbled. When selecting a group of objects to turn into a prefab:

* Ensure a static object is the first object selected.
* Include a Mode Prefab within the selection.
* Do not select the Mode Prefab as the first object.

## Benefits of Mode Prefabs

Converting a standard prefab into a Mode Prefab provides a significant advantage regarding content updates. When a Mode Prefab is updated, any new placement of that prefab will automatically receive the updates for every user. This eliminates the need for users to manually re-bookmark the prefab to see changes.

{% hint style="success" %}
Using Mode Prefabs allows you to push updates to all new placements of that prefab automatically.
{% endhint %}

***

## Source Data

* Discord thread: [Making any Prefab into a Mode Prefab](https://discord.com/channels/220766496635224065/1417228240526905447/1417228240526905447)

#### <mark style="color:green;">Contributors</mark>

Okom
---
description: >-
  Learn how to convert standard prefabs, including those with static
  objects, into Mode Prefabs using two different methods.
---

# Making any Prefab into a Mode Prefab

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While prefabs containing static objects are typically prevented from being classified as modes, specific workflows allow these to be converted into Mode Prefabs.

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

## Script Brain vs. Mode Brain

Mode Brains offer several advantages over regular Script Brains:

* They can be colored.
* They can be converted into Mode Prefabs.
* They allow for updates while maintaining the asset link.

Regular Script Brains are primarily useful for creating prefabs that contain only dynamic objects and should be classified as standard prefabs rather than modes.

## Benefits of Mode Prefabs

Converting a standard prefab into a Mode Prefab provides a significant advantage regarding content updates. When a Mode Prefab is updated, any new placement of that prefab will automatically receive the updates for every user. This eliminates the need for users to manually re-bookmark the prefab to see changes.

{% hint style="success" %}
Using Mode Prefabs allows you to push updates to all new placements of that prefab automatically.
{% endhint %}

{% hint style="info" %}
An update arriving on 2026-05-01 is expected to fix the exploit that allows players to create Mode Prefabs from any normal Prefab. This will not break existing Mode Prefabs.
{% endhint %}

***

## Source Data

* Discord thread: [Making any Prefab into a Mode Prefab](https://discord.com/channels/220766496635224065/1417228240526905447/1417228240526905447)

#### <mark style="color:green;">Contributors</mark>

Okom\
swagonflyyyy
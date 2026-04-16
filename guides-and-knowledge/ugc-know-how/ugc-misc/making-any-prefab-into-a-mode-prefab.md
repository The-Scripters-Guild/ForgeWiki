---
description: Learn how to convert standard Prefabs, including those containing static objects, into Mode Prefabs using two different methods.
---

# Making any Prefab into a Mode Prefab

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Standard Prefabs can be converted into Mode Prefabs, even if they contain static objects. This conversion allows for more dynamic behavior and easier updates across user sessions.

## Conversion Methods

There are two primary ways to convert a Prefab into a Mode Prefab.

### Modifying an Existing Prefab

If you have an existing Prefab that you wish to convert, you can add a **Mode Brain** to it. Once the Mode Brain is added, saving the Prefab will transform it into a Mode Prefab, and it will then be classified as a Mode.

### Group Selection Method

A Mode Prefab can also be created during the initial selection and grouping process by following a specific selection order:

1. Select a group of objects.
2. Ensure the **first** object selected is a static object.
3. Include a Mode Prefab within the selection, provided it is **not** the first object selected.

{% hint style="success" %}
Converting Prefabs to Mode Prefabs enables seamless updates; when you update a prefab, any new placements of that prefab will reflect those changes for all users without requiring them to re-bookmark the asset.
{% endhint %}

## Benefits and Use Cases

The primary advantage of using Mode Prefabs over standard Prefabs is the ease of maintenance. When a creator updates a Mode Prefab, the changes are automatically applied to any new instances placed by users. This functionality removes the need for users to manually re-bookmark a prefab to receive the latest version.

***

## Source Data

- Discord thread: <https://discord.com/channels/220766496635224065/1417228240526905447/1417228240526905447>

#### <mark style="color:green;">Contributors</mark>

Okom\
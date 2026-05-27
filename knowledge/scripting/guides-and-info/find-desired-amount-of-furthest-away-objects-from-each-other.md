---
description: >-
  Explains how to select a specific number of objects from a group by
  maximizing the distance between them.
---

# Find Desired Amount of Furthest Away Objects From Each Other

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This logic allows for the selection of a specific quantity of objects from a larger pool, such as spawn points, by ensuring they are positioned as far from one another as possible. Instead of merely selecting the most distant individual objects, the method evaluates the spacing between the entire set of chosen candidates.

## Spreading Object Distribution

To achieve a balanced distribution, the selection process relies on the concept of "Max Min Distance." This approach prevents objects from clustering in specific areas, such as appearing in two distant groups, by ensuring that new objects added to the list maintain a significant distance from all existing members.

### The Max Min Distance Concept

The logic differentiates between the proximity of a single candidate and the overall quality of the set through two key variables:

* **Min Distance**: The distance from a potential candidate to its nearest neighbor among the objects already selected for the group.
* **Max Min Distance**: The highest "Min Distance" value found during the search process.

<figure><img src="../../../.gitbook/assets/furthest-objects-from-each.webp" alt="Furthest objects workflow"><figcaption><p>The script uses a logic loop to determine which objects are furthest from the current selection.</p></figcaption></figure>

## Implementation Strategy

#### Candidate Selection

The process begins by selecting an initial anchor object. Because this first object can be chosen randomly, the specific set of objects selected can change with each execution, providing variety in the distribution.

The script iterates through the available objects and compares their positions to the objects already in the "desired objects" list. A candidate is considered for inclusion when its "Min Distance" is greater than the current "Max Min Distance."

{% hint style="info" %}
Comparing the distance of a new object against the entire existing list is necessary to prevent objects from appearing close to members already selected.
{% endhint %}

## Distribution Results

When implemented correctly, the objects are spread across the available area rather than being concentrated in one or two distant groups.

<figure><img src="../../../.gitbook/assets/desired-object-distribution1.webp" alt="Object distribution 1"><figcaption><p>The selected objects are distributed across the area to maintain maximum distance.</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/desired-object-distribution2.webp" alt="Object distribution 2"><figcaption><p>The final distribution shows objects spread out across the terrain.</p></figcaption></figure>

***

## Source Data

* Discord thread: [Find Desired Amount of Furthest Away Objects From Each Other](https://discord.com/channels/220766496635224065/1508892619319545966/1508892619319545966)

#### <mark style="color:green;">Contributors</mark>

Okom\
swagonflyyyy (Mr. Blackwell)
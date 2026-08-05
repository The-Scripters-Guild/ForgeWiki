---
description: >-
  Standardized measurements for player movement, geometry, and map
  dimensions in level design.
---

# Metrics

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

In the context of level design, metrics refer to the proportions and distances within gameplay spaces. Maintaining a baseline knowledge of these standard values is important so that environment scaling and character movement feel correct during play.

## Level Geometry Metrics

The following measurements are key dimensions for designing geometry in Halo Infinite:

### Character and Jump Heights
* Player height: 11.25 units
* Crouch height: 9 units
* Jump height: 9.5 units
* Crouch jump height: 11.5 units
* Clamber height: 16 units
* Jump distance: 34 units
* Sprint jump distance: 40 units

### Navigation and Pathways
Because Halo features more "floaty" movement than other arena shooters, pathways on maps are usually a bit wider than usual, and doorways tend to be taller.

* Normal player pathway: 16 units
* Narrow player pathway: 8 units
* Vehicle pathway: 32 units

## Map Scaling Guidelines

Scaling is used as a guideline to determine the size of space required based on intended player counts. As maps that are too small or too large can be easily noticed during gameplay, the following dimensions have been universally tested as ideal sizes:

* **4v4:** `450 x 340 x 100`
* **8v8:** `900 x 600 x 160`
* **12v12:** `1100 x 750 x 200`

{% hint style="info" %}
While these guidelines assume rectangular boundaries, if the ratio of a map is changed (such as making it shorter), the width should be increased to maintain equivalent volume.
{% endhint %}

***

## Source Data

* Discord thread: [Metrics](https://discord.com/channels/220766496635224065/1534418014441570456/1534418014441570456)

#### <mark style="color:green;">Contributors</mark>

Okom

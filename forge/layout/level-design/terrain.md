---
description: >-
  The way to create terrain in Forge is with individual, preset
  terrain objects. These terrain objects come in various shapes that
  can be combined to create various shapes of terrain.
---

# Terrain

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Landscaping in Forge is achieved by combining individual, preset terrain objects of various shapes. Creating complex landforms often requires a careful visual assessment to determine which pieces can be effectively used together to form specific shapes and features.

## Composition and Placement

Because landscapes are built from many distinct, shaped pieces rather than as a single mesh, the process can be tedious. Achieving natural-looking terrain requires significant effort in selecting and placing objects so that their silhouettes transition smoothly into one another.

## Object Variants

Terrain objects fall into two categories: normal objects and TI (Terrain Inherited) objects. These variants serve different aesthetic purposes and have distinct technical behaviors.

### Normal Objects

Normal terrain objects allow for customization of both material and color, similar to many other Forge objects. A key feature of these objects is the inclusion of three material slots (swatches). Creative use of these swatches can create well-blended pathways, as some swatches are designed with smooth transitions between them.

### TI (Terrain Inherited) Objects

TI terrain objects inherit their material and texture directly from the canvas terrain's current texture at that location. Unlike normal objects, they cannot be manually adjusted for color or material. When a TI object is moved to a different position on the map, its appearance changes because it displays whatever part of the underlying canvas texture exists at those new coordinates.

{% hint style="warning" %}
Using TI terrain presents specific challenges: 
* Blending them into non-TI environments can be difficult since finding an exact material match for the inherited texture is complex.
* Map design must account for the fixed nature of the canvas terrain, as its texture patterns are locked in position and cannot be moved or changed.
{% endhint %}

***

## Source Data

* Discord thread: [Terrain](https://discord.com/channels/220766496635224065/1534326125277347932/1534326125277347932)

#### <mark style="color:green;">Contributors</mark>

Okom

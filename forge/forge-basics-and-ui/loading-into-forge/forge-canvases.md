---
description: >-
  Forge canvases are empty maps with varying themes that players can
  use to begin their map projects on. Most forge maps are built on a
  forge canvas map.
---

# Forge Canvases

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Forge canvases are empty maps provided in different themes that players can use to begin their map projects. While most "forge maps" are built upon a forge canvas, it is important to distinguish them from "dev maps," which are constructed using developer tools; even if dev maps contain Forge objects, they remain classified as dev maps.

## Canvas variants and themes

The following list represents the available forge canvases:

* Arid
* Barrage
* Ecliptic
* Institute
* Mires
* Permafrost
* Seafloor
* Void

Each canvas features a specific theme, such as snow (Permafrost), grass, or space. All canvases except for **Void** and **Ecliptic** feature built-in terrain. These terrains include unique texture patterns that can be matched by using "TI" or "Terrain Inherited" objects, allowing creators to replicate the canvas's terrain pattern without manually adjusting material colors and textures.

## Starting platforms

Every forge canvas includes a starting platform containing basic gameplay setup elements, such as spawn points, item spawns, and gamemode configurations. These can serve as references for ideal item spawner placement or for testing specific gamemodes.

{% hint style="warning" %}
The default starting platform configuration provided by Halo Studios contains incorrect object properties; it appears to be an inaccurate copy of the setup found on the [tsg Void](https://www.unggoy.xyz/maps/eb6ef4dd-3fe0-4265-a5db-40bfb90a851b) map.
{% endhint %}

## Forgeable areas

### Gameplay area

The primary gameplay area for a forge canvas is an XYZ: 4000x4000x1500 unit space, with the canvas floor located at Z: 500. Moving beyond these defined limits triggers an undeletable soft-kill boundary accompanied by a soft barrier that prevents player movement past it.

### Object placement limits

There are two distinct boundaries regarding object placement and persistence on forge canvases:

1. **The Hard Barrier:** A cubical boundary exists at approximately XYZ: 40000x40000x30000 (roughly 20,000 units in each direction from the 0,0,0 point, with different vertical limits). While objects can be placed near the corners of this cube, they will be deleted upon a session restart.
2. **The Deletion Boundary:** A separate, invisible sphere exists with a radius of 20,250 units from the 0,0,0 point. Any object placed beyond this boundary will be deleted when the Forge session is restarted.

{% hint style="info" %}
When placing large-scale skybox objects—such as moons or distant mountains—ensure the object's origin point remains within the 20,250-unit radius sphere to prevent them from being deleted after a session restart. The [tsg objectPlacementBounds](https://www.unggoy.xyz/prefabs/25603843-8140-4a1a-82d6-7a1634564efa) prefab can be used to visualize this boundary.
{% endhint %}

### Subsurface space

Below the canvas floor (Z: 500), there is a large area extending from Z: -250 down to Z: -9462.15. This subsurface region has an XYZ dimension of 4635x4542x9212. Players can freely place static or dynamic objects and perform standard gameplay actions within this space without being instantly killed; however, moving outside the boundaries of this specific area results in an instant respawn.

***

## Source Data

* Discord thread: [Forge Canvases](https://discord.com/channels/220766496635224065/1533995379237060678/1533995379237060678)

#### <mark style="color:green;">Contributors</mark>

Okom
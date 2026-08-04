---
description: >-
  Empty maps with various themes used as starting points for Forge map
  projects.
---

# Forge Canvases

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Forge canvases are empty template maps that serve as the foundation for most player-made Forge maps. While these templates provide various themes to begin a project, they should not be confused with "dev maps," which are built using developer tools and retain their classification even if they contain forge objects.

## Canvas Variants and Themes

There are eight specific variants of forge canvases available:

* Arid
* Barrage
* Ecliptic
* Institute
* Mires
* Permafrost
* Seafloor
* Void

Each variant features a distinct theme, such as snow, desert, grass, or space. All canvas variants except for Void and Ecliptic feature built-in terrain. These canvases possess unique terrain texture patterns that can be utilized by "TI" (Terrain Inherited) objects to match the existing landscape without manually adjusting materials or colors.

## Map Layout and Boundaries

Forgeable area dimensions vary depending on whether a player is interacting with the gameplay volume, placing static objects, or utilizing the subsurface space.

### Gameplay Area
The designated gameplay area has XYZ dimensions of 4000x4000x1500 units. The canvas floor is positioned at Z: 500. Moving beyond these specific limits triggers an undeletable soft-kill boundary and a soft barrier that prevents player movement.

### Object Placement Limits
While players can place objects within a large cubical area of approximately XYZ: 40000x40000x30000 units, there is a critical distinction between the hard placement limit and object persistence. A separate sphere boundary exists with a radius of 20250 units from the 0,0,0 origin point; any objects placed beyond this spherical boundary will be deleted when the Forge session is restarted.

{% hint style="warning" %}
Objects located in the corners of the cubical placement boundary that fall outside the 20250-unit radius sphere will not persist after a session restart. To visualize this invisible deletion volume, players can use the [tsg objectPlacementBounds](https://www.unggoy.xyz/prefabs/25603843-8140-4a1a-82d6-7a1634564efa) prefab.
{% endhint %}

### Space Under the Canvas
A large volume exists beneath the canvas floor (Z: 500). This subsurface area begins at Z: -250 and ends at Z: -9462.15, with total dimensions of XYZ: 4635x4542x9212. Players can freely place dynamic or static objects in this zone without being instantly killed; however, moving outside the boundaries of this subsurface area will result in an instant respawn.

## Starting Platforms

Every forge canvas includes a starting platform containing basic gameplay elements such as item spawns, spawn points, and gamemodes. These platforms serve to demonstrate ideal item spawner placement or provide examples for setting up specific gamemode configurations. 

It is noted that the default starting platform setups provided by Halo Studios contain incorrect object properties. For an example of a correctly configured starting platform using these same objects, players can refer to the map [tsg Void](https://www.unggoy.xyz/maps/eb6ef4dd-3fe0-4265-a5db-40bfb90a851b).

***

## Source Data

* Discord thread: [Forge Canvases](https://discord.com/channels/220766496635224065/1533995379237060678/1533995379237060678)

#### <mark style="color:green;">Contributors</mark>

Okom
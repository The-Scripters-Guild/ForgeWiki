---
description: >-
  Taking some time to visualize what you intend your level to look
  like when it's finished, and planning the position and orientation
  of your map before even beginning building it can save a lot of time
---

# Planning The Location And Orientation of Your Map

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Visualizing a level's final appearance before construction begins can prevent significant time and frustration during the building process. Understanding how fixed canvas elements interact with your objects allows for more efficient map design.

## Benefits of Pre-Build Planning

Forge canvases contain static elements that cannot be adjusted, necessitating careful planning to avoid undesired outcomes. Not accounting for these features early on can make it difficult to resolve issues once hundreds of objects have been placed across the map. Knowing these limitations helps in positioning and orienting a map to take maximum advantage of existing canvas assets.

## Environmental and Visual Composition

### Skybox Framing
If a map is built on any forge canvas other than Void or Ecliptic, it will feature an expansive skybox vista. Forgers can utilize this free visual content by positioning the map to frame the skybox within their intended art theme. A common technique used on the Arid canvas involves orienting the map so that the large Halo Ring in the skybox acts as a "hero piece" for the composition of views from the gameplay area.

### Global Reflection
All forge canvases include a "global reflection," which serves as the default reflection for the entire map. This reflection is an image taken from the XYZ: 0,0,1000 coordinate and is applied to all reflective surfaces that have not been overridden by a custom reflection.

Because this point is fixed at XYZ: 0,0,1000, its position relative to your gameplay area is crucial for visual accuracy—especially on maps featuring large water planes extending into the skybox. Placing the 0,0,1000 coordinate near the ideal viewing point of a water vista will ensure the reflections appear accurate from that perspective. Conversely, if the global reflection point ends up inside a building because the map was not designed with it in mind, any reflective surface (such as an outdoor waterbed) would display the interior of that building.

#### Modifying Default Reflections
By placing custom textures around the XYZ: 0,0,1000 coordinate, forgers can change the default reflection used across the entire map. Manipulating this texture can save significant time by reducing the need for manual Reflection Volume placement throughout a level.

### Canvas Terrain Texture
All forge canvases except Void and Ecliptic feature custom terrain textures that are utilized by TI terrain objects. Finding a suitable section of the canvas terrain texture during the planning phase allows forgers to build their map around it, making it much easier to create realistic paths and blending with minimal effort.

## Boundaries and Flow

### Soft Kill Zones
Each forge canvas is sized XYZ: 4000x4000x1500, with the floor located at XYZ: 0,0,500. The immediate area beyond these bounds contains a soft kill boundary and a soft barrier that pushes players back into the gameplay area. These barriers act as cushions rather than solid walls; planning map boundaries—particularly upper ceilings—around these zones can make the limits of the map feel less jarring to the player.

### Water Flow Direction
The direction of water flow is fixed toward the South cardinal direction on all forge canvases and cannot be changed by wind settings.

{% hint style="info" %}
To determine which way is South, enter Test Mode in Forge and observe your motion tracker or Assault Rifle ammo counter. The arrow indicates North; therefore, South is the opposite of that direction.
{% endhint}

{% endhint %}

To determine which way is South, enter Test Mode in Forge and observe your motion tracker or Assault Rifle ammo counter. The arrow indicates North; therefore, South is the opposite of that direction.
{% endhint}

***

## Source Data

* Discord thread: [Planning Map Position and Orientation](https://discord.com/channels/220766496635224065/1534368079704883230/1534368079704883230)

#### <mark style="color:green;">Contributors</mark>

Okom
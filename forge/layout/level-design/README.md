---
description: >-
  Learn the fundamentals of designing functional, readable,
  and engaging levels in Halo Infinite's Forge.
---

# Level Design

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While Halo Infinite is an arena shooter, players can build a wide variety of experiences beyond standard competitive maps using the Forge suite. From campaign scenarios to minigames, the tools allow for immense creativity in layout and mechanics.

## Prototyping with Blockouts

A blockout—also known as a greybox, whitebox, or prototype map—is the first playable version of a level, constructed using simple geometric shapes rather than finished art. The primary goal of a blockout is to test gameplay functionality instead of focusing on final visual aesthetics.

For building a simplified palette during the prototyping phase, it's recommended to use objects from the Halo Design Set and Primitives categories within the Object Browser:
* Cube: `Floors → Floor Half B`
* Triangle: `Floors → Floor Angled Standard A`
* Cylinder: `Primitives → Cylinders → Primitive Cylinder`
* Sphere: `Primitives → Spheres → Primitive Sphere`

## Iterative Design Workflow

### Build Fast and Refine Later

To realize layout ideas quickly, it is best to create rough geometry that can be easily discarded without significant wasted effort. This initial phase is sometimes called a "slopout," as the focus is on testing whether an idea works rather than achieving refinement.

Once a rough layout has been tested and found functional, the map should be rebuilt using aligned objects and standard metrics. While this rebuilding process takes more time, it ensures a strong foundation for the level; failing to observe standard spacing and metrics during the prototyping stage can make subsequent refining much more difficult.

## Designing for Halo

### Geometry and Scale
* **Shape Language:** When designing routes and rough geometry shapes in your blockout or slopout, keep the shape language of your intended theme in mind.
* **Inclines:** For developer-standard maps, inclines should be no steeper than 26.5 degrees whenever possible.
* **Pivot Points:** When building at non-90 degree angles, changing the pivot point for position and rotation allows you to continue building as if you were on a "standard" angle.
* **Rotating Large Objects:** If an object or prefab is not situated at 0,0,0 rotation, spawn in a primitive cube to use as an anchor while rotating the target object.
* **Halo Design Set objects:** These objects are designed with proper scale and angles for developer-made maps. While items like doorways or ramps can be used out of the box without scaling, all objects can and should be scaled if your map requires it.
* **Scale Markers:** Use the Player Scale Object from the HDS category as a marker for the correct scale and shape of your map. Making this object a bright color ensures it remains visible across various light levels and environments.
* **Engagement Testing:** To test the Red Reticle Range (RRR) of your map's scale, place fusion coils in various areas to ensure players can engage targets at appropriate distances with their reticles lighting up correctly.

### Asset Placement and Visual Clarity
* **Weapon Racks:** Ensure weapon racks are set at a proper height above the ground using official weapon rack mounts.
* **Pad Placement:** Unless specific to a gamemode, keep all grenade, equipment, and weapon pads firmly on the ground (players should be able to obtain them simply by walking over them) rather than placing them on walls; use racks for wall-mounted items instead.
* **Color Differentiation:** Use different colors during the blockout stage—such as unique colors for floors, walls, and cover/doorways—to help players visually distinguish geometry without thinking about it. Assign specific colors to certain wall areas to establish easy callouts (e.g., "red room" or "yellow hall").

## Technical Guidance

### Efficiency Tips
* **Material Swatches:** If an object has multiple material swatches but you only need one, set the desired material and then change the others to "Blank" to save time.
* **TSG Prefabs:** To reduce development time, make use of official [tsg sandbox](https://www.unggoy.xyz/prefabs/ad30a5dd-6fd7-44fb-ad21-f2295834cbca) and [tsg gamemodes](https://www.unggoy.xyz/prefabs/ad30a5dd-6fd7-44fb-ad21-f2295834cbca) prefabs which provide correctly configured objects for sandbox and gamemode setup.

### Volume Management
* **Named Location Volumes:** Use a volume with a generic name, such as "Outside," to cover entire playable spaces and fill awkward vertical areas or gaps. 
* **Volume Boundaries:** In Named Location Volumes, set the boundaries to `Show = On` so you can physically see any gaps in your work and ensure all required areas are covered and named correctly.

***

## Source Data

* Discord thread: [Level Design](https://discord.com/channels/220766496635224065/1534355827551637636/1534355827551637636)

#### <mark style="color:green;">Contributors</mark>

Okom\
Igrizhar

---
description: What Nav mesh generation Root Points are and how they behave.
---

# Nav Mesh Generation Root Points

This article explains what Nav mesh generation Root Points are and how they behave.

### What is a Root Point?

A Nav mesh generation Root Point is an object that has the property to generate Nav mesh data from it as long as the object's origin point is close enough to geometry that you can generate Nav mesh on.

### List of known Nav mesh generation Root Point objects

* Nav Seed Point
* Spawn Point [Respawn]
* Spawn Point [Initial]
* Spawn Point [Backup] (including the <a href="/main/halo-infinite/forge/player-spawning/backup-spawn-points" target="_Blank">invisible Backup Spawn Points</a>)
* Team Intro Arrow Front
* Team Intro Line Left
* Team Intro Line Right

<figure><img src="/.gitbook/assets/nav-root-points-spawns.jpg" alt="Image showing different Spawn Point objects generating Nav mesh data"><figcaption><p>Visualization showing Nav mesh data generated from different Spawn Points.</p></figcaption></figure>

{% hint style="info" %}
The Nav hints in the image are placed just so the Nav mesh can connect to each platform and the generated Nav mesh data can be shown in one image.
{% endhint %}

### Effective radius

The effective radius from the origin point of a Nav mesh generation Root Point object is 4.98 units. Meaning that as as long as the geometry you want the Root Point to effect on is within a 4.98 unit spherical radius from the Root Point object's origin point, it will connect to and try generating Nav mesh on that surface.

<figure><img src="/.gitbook/assets/nav-root-point-height.jpg" alt="Image showing different Spawn Point objects generating Nav mesh data"><figcaption><p>Visualization showing Nav mesh data generated from different Spawn Points.</p></figcaption></figure>

{% hint style="info" %}
Intersecting a Root Point like a Nav Seed Point with the geometry is not necessary, and only still results in the same outcome due to there being said ~5 unit effective radius where the Root Point object can still have its Nav mesh generating effect on the surface.
{% endhint %}

### Blocking Root Points

The Nav mesh generation effect of a root point can be blocked by covering the effective radius of the Root Point within a Nav Cutter with its Type set to `Ground`. 

Keep in mind that you need to cover the effective radius of the Root Point and not just the object's origin point within the boundary of the Nav Cutter. Setting the size of a Nav Cutter's boundary to `12, 12, 12` and having it's origin point position be the same as the Root Point will be enough to overcome the effective range reliably.

<hr>

**Contributors**\
Okom

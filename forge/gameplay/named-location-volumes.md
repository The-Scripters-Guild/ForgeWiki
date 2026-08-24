---
description: >-
  Named Location Volumes allow players to assign specific names to
  different areas of a map.
---

# Named Location Volumes

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Named Location Volumes allow players to assign specific names to designated areas of a map. It is standard practice for all sections of the gameplay area to have an assigned callout name, as no gameplay areas should be left without one.

Additionally, it can be beneficial to extend Named Location Volume coverage outside the physical boundaries of the map in areas where players might look or mark a spot. Marking a location reveals its associated name, so extending these volumes ensures that such markings are informative. It is not necessary to assign names to areas strictly outside the gameplay space.

## Selectable Location Names

The following list contains all the location names available for selection within the Named Location Volume object in Halo Infinite Forge:

{% file src="../../.gitbook/assets/Named Location Volume strings.txt" %}

## Appearance Order

If two Named Location Volumes overlap, the one that takes up less volume will take priority. This feature can be used cleverly to cover oddly shaped areas using a volume that is artificially extended multiple units underground in order to make its volume larger, and then using smaller boundaries in areas where the larger boundary overlaps to, but shouldn't cover.

For example, you could cover two callouts of an L-shaped hallway and the area outside it by having one large box volume for the entire hallway and a smaller one for the area outside the hallway. As the smaller volume takes priority over the larger, the two areas can be distinguished with different names using just two volumes, where conventionally it would've taken three: two for the L-shaped hallway and one for the outside area.

## Area Coverage and Boundary Limits

The Named Location Volume adheres to standard boundary limits for Forge objects. Users can choose between Box or Cylinder shapes to define these boundaries.

### Shape-Specific Dimensions

* **Box Boundaries:** 1,250 (Width) x 1,250 (Length) with a limit of 1,250 for both Top and Bottom dimensions.
* **Cylinder Boundaries:** The Top and Bottom limits remain at 1,250. However, the Width and Length parameters are replaced by Radius, which has its own limit of 1,250.

{% hint style="info" %}
A cylinder with a radius of 1,250 covers more area than a box with width and length limits of 1,250. Changing the volume type to a cylinder is an effective way to cover a larger area.
{% endhint %}

***

## Source Data

* Discord thread: [Named Location Volumes](https://discord.com/channels/220766496635224065/1538508315003330560/1538508315003330560)

#### <mark style="color:green;">Contributors</mark>

Okom

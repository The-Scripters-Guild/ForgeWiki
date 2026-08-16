---
description: >-
  Named Location Volumes allow players to assign specific names to
  different areas of a map.
---

# Named Location Volumes

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Named Location Volumes are used in Forge to provide callout names for specific sections of map geometry, allowing players to identify locations by name during gameplay. 

## Map Naming and Best Practices

It is standard practice to ensure every section of a gameplay area has an assigned callout name so that no areas remain unnamed. A complete list of all selectable location strings available within the Named Location Volume object can be found in the attached `Named_Location_Volume_strings.txt` resource.

{% hint style="info" %}
It is recommended to extend Named Location Volume coverage outside of map boundaries in areas where players may look or attempt to mark a spot, as marking reveals the area's name. However, it is not necessary to assign names to areas located entirely outside the gameplay space.
{% endhint %}

## Boundary Dimensions and Shapes

The dimensions available for a Named Location Volume depend on whether the boundary is configured as a box or a cylinder. 

### Shape Properties

#### Box Boundaries
When using a standard box boundary, the volume follows these specific limits:
* **Width:** 1,250
* **Length:** 1,250
* **Top:** 1,250
* **Bottom:** 1,250

#### Cylinder Boundaries
The cylinder shape uses the same Top and Bottom limits as a box. However, instead of Width and Length settings, it utilizes a Radius setting. This radius also has a maximum limit of 1,250.

{% hint style="success" %}
Because a cylinder with a radius of 1,250 covers more surface area than a box with a width and length of 1,250, the boundary can be made to cover a larger total area by changing its type to a cylinder.
{% endhint}

{% endhint %}

Because a cylinder with a radius of 1,250 covers more surface area than a box with a width and length of 1,250, the boundary can be made to cover a larger total area by changing its type to a cylinder.
{% endhint}

***

## Source Data

* Discord thread: [Named Location Volumes](https://discord.com/channels/220766496635224065/1538508315003330560/1538508315003330560)

#### <mark style="color:green;">Contributors</mark>

Okom
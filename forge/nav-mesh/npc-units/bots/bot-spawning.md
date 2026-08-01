---
description: >-
  Discovering what the line of sight spawn blocking boundary on maps
  is. This weird shape that extends seemingly forever sideways until
  the angles meet.
---

---

# Bot Spawning

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Spawning in certain environments is influenced by a player's line of sight (LoS) through specific spatial boundaries and geometric shapes, including large cones originating from the player's head. These mechanics determine whether a spawn point remains blocked or becomes accessible to players based on their orientation and position relative to others.

## Line of Sight Blocking Mechanics

The primary mechanism for blocking spawns via line of sight is an extremely large cone that originates from a player's head. This cone has approximately 176° field-of-view (FOV) and features a diameter of about 10480 units, extending to a length/radius of 181.26 units.

<figure><img src="../../../../.gitbook/assets/2026-07-21_HaloInfinite-55ra.webp" alt="Discovery image"><figcaption></figcaption></figure>

When a player is within this area, they may block spawns depending on their orientation toward the spawning entity or location. In specific configurations, a player can be significantly far from a target (for instance, several thousand units away) and still successfully block its spawn by being positioned within that massive cone's reach. 

{% file src="../../../../.gitbook/assets/los-cone-10480-units.mp4" %}
This video demonstrates how a player can block spawns from significant distances using their LoS cone position.
{% endfile %}

<figure><img src="../../../../.gitbook/assets/2026-07-21_HaloInfinite-SSiU.webp" alt="Cone visualization"><figcaption></figcaption></figure>

### Obstruction Requirements

The success of this spawn blocking depends on an unobstructed line of sight between the spawning player's upper torso and the target player's head. If any static or dynamic obstruction is present along this specific path, the spawn-blocking effect may be invalidated.

{% hint style="warning" %}
Third-person perspective can be used to manipulate LoS functionality by exploiting how the game performs the obstruction check between the player's head and the target's upper torso.
{% endhint %}

## Boundary Geometry and Perceptions

There is significant discussion regarding a "spherical boundary" associated with spawn blocking, often described as having a 181.26 unit radius (approximately 55 meters) originating from the spawn point. However, evidence suggests this sphere may be an artifact caused by overlapping LoS cones rather than a standalone physical entity in the game engine. The interaction is primarily driven by how one player's cone intersects with another player's position or their own personal boundary.

<figure><img src="../../../../.gitbook/assets/2026-07-21_HaloInfinite-Vsty.webp" alt="Boundary diagram"><figcaption></figcaption></figure>

Because these boundaries are based on individual player LoS, every player possesses an identical line of sight cone and a personal boundary that affects how they can be spawned upon by opponents. This functionality is consistent across both Forge maps and developer canvas maps.

### Utilizing Spatial Boundaries

Understanding the behavior of the LoS cone allows for specific tactical adjustments to either block or facilitate spawns:

* **Vertical Coverage:** Aiming straight up or down positions the 10480-unit diameter cone above or below the player's current altitude, potentially covering large portions of a map vertically.
* **Sideways Tilting:** Players can tilt themselves sideways toward spawns that are within their LoS but situated further than 181.26 units away to maintain blocking effectiveness.
* **Direct Sight:** To maximize spawn-blocking efficacy or prepare for an encounter, looking directly at the target is most effective as it represents the shortest distance of the cone's front section.

{% file src="../../../../.gitbook/assets/los-cone-exploit.mp4" %}
The footage demonstrates how aiming vertically or facing away can impact the effectiveness of spawn blocking.
{% endfile %}

***

## Source Data

* Discord thread: [Player Line of Sight Cone Research](https://discord.com/channels/220766496635224065/1529131373602799626/1529131373602799626)

#### <mark style="color:green;">Contributors</mark>

Okom
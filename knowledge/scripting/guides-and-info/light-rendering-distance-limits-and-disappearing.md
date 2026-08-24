---
description: >-
  Storing lights too far away from players, and moving them to the position of the player can cause the lights to not render.
---

# Light Rendering Distance Limits and Disappearing

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Light objects in the engine are subject to rendering distance limits that can cause light emitters to stop functioning or appear to be in the wrong position if the player moves too far away. Most of the time this limitation works in favor of optimizing performance, but in a script like adjusting a light's position to be next to a player as a flashlight, this render limitation behavior can become a detriment.

## Rendering Distance Thresholds

### The 650-Unit Limit

Light objects will stop working if they are more than 650 units away from the player. This distance limit specifically affects the light-emitting portion of the object. 

When a script adjusts the position of a light object—such as a flashlight loop designed to keep a light at the player's position—the following behavior may occur:
* The physical object part of the light will follow the player via the script.
* If the light-emitting portion is currently outside the 650-unit radius, it will not render.
* Consequently, even if the light object is moved directly to the player's position by a script, the light will remain at its previous location until the player re-enters the 650-unit radius of the original emission point.

{% file src="../../../.gitbook/assets/light-650-unit-render.mp4" %}
The video demonstrates a light object failing to render its light-emitting portion despite the object's position being adjusted.
{% endfile %}

{% hint style="warning" %}
If a light's position is moved to a location more than 650 units from the player, the light will not render again until the player moves back within that 650-unit radius.
{% endhint %}

## Maintaining Light Visibility

### Mitigation Strategies

To prevent lights used in scripts like player-based flashlights from disappearing or becoming non-functional, developers can implement several positioning strategies:

* **Centralized Placement:** Position light objects in a centralized location where they remain within a 650-unit radius of any player at all times.
* **Player-Following Offsets:** Assign a light to follow each player at a specific offset (e.g., 645 units underneath the player). While this ensures the light stays rendered, it may cause the light to be visible to other players in areas with extreme verticality.

***

## Source Data

* Discord thread: [Light Rendering Distance Limits and Disappearing](https://discord.com/channels/220766496635224065/1541501331460587661/1541501331460587661)

#### <mark style="color:green;">Contributors</mark>

Okom\
Mr Multibit

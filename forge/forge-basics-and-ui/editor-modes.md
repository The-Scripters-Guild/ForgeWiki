---
description: >-
  An overview of the Monitor, Test, and Play modes available within
  the Forge editor for map design and testing.
---

# Editor Modes

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The Forge editor provides several operational modes that allow creators to transition between building, testing scale, and full gameplay simulation.

## Monitor Mode
Monitor Mode, also called "**Forge Mode**", is most frequently used to place and adjust objects, alter their properties, create scripts, or modify map settings such as lighting and navigation meshes. This is the mode that you spawn in by default when loading into Forge on a map. While in this mode, the player functions as a floating Forge Monitor capable of flying through geometry. This mode can be entered from Play Mode using **F6**/**View** or **F5**.

## Test Mode
Test Mode transforms the floating Forge Monitor into a bipedal character that can walk on map geometry. It is primarily used to quickly assess map scale and sightlines without initiating full physics simulation. From this mode, users have the ability to transform back into Monitor Mode to continue editing. This mode is entered from Monitor Mode using **F5**/**View**.

### Simulation Limitations
In Test Mode, dynamic gameplay elements and physics are not simulated. It is intended for quickly testing out changes made in Monitor Mode before beginning a full physics simulation.

## Play Mode
Play Mode allows users to test maps in an environment where simulation, physics, and scripting are active. This mode essentially functions as a simulated Arena:Slayer match within Forge. 

{% hint style="warning" %}
While the logic for simulated Arena:Slayer gameplay is accurate, it is not a perfect representation of Custom Games; some objects exist in Forge that are absent in Custom Games, and Forge does not check line-of-sight for player respawning. It is recommended to test all experiences in a real custom game before finalization.
{% endhint %}

This mode can be entered from Monitor Mode by holding **F6**/**View**.

***

## Source Data

* Discord thread: [Editor Modes](https://discord.com/channels/220766496635224065/1534016741733175297/1534016741733175297)

#### <mark style="color:green;">Contributors</mark>

Okom
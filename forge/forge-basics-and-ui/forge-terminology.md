---
description: >-
  A guide to common, scripting, and specialized terminology used by
  the Forge community.
---

# Forge Terminology

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article provides definitions for various terms encountered within Halo's Forge editor, ranging from general gameplay concepts to specialized scripting logic and obscure object usage.

## General Concepts

* **Forge**: The level editor used in Halo games to create maps, prefabs, and scripted modes.
* **Forger**: A person who creates content using the Forge tools.
* **Map**: A playable level.
* **Mode/Game Mode**: A predefined ruleset loaded alongside a map that defines objectives and gameplay mechanics for a match.
* **Prefab**: A group of two or more objects saved as a single unit to be shared with other creators; these are often used to build complex structures like entire buildings.

### Scripting and Logic

All Forge scripting is performed within the Node Graph, which serves as a visual building block interface similar in nature to Unreal Engine 5's Blueprint system.

* **Node**: A visual building block within the Node Graph that represents data or performs specific operations. Nodes are connected to define logic, behavior, or data flow.
* **Script Brain/Mode Brain**: An object containing the Node Graph.

{% hint style="info" %}
A single Script Brain can hold a maximum of 128 nodes and 512 connections between those nodes.
{% endhint %}

## Creator Vocabulary

Creators use specific terminology to describe map elements, visual states, and technical properties.

* **HDS (Halo Design Set)**: A category of simple objects used during the blockout stage or for general primitive shapes like cubes and spheres. These objects utilize a corner origin point.
* **Primitives**: Objects in the "Primitives" category that serve similar purposes to HDS but use a central origin point instead of a corner one.
* **Blockers**: Invisible cube objects used for map containment. Variants include one-way, projectile-blocking, universal, team-based, vehicle-only, and player-only versions.
* **TI-terrain**: Terrain objects that inherit the texture and material from the Forge Canvas terrain.
* **The Browser**: The User Generated Content (UGC) browser used to find published content within the game.
* **Red-racked**: A state in which an item spawner (such as a Weapon Rack) displays a red timer immediately upon an item being picked up. This occurs when Spawn Logic is set to "Dynamic (Expired)" or the Max Deployed setting is 1.00; once the item has despawned, the blue progress timer for the next spawn begins.
* **Callout**: A specific named location on a map created via a Named Location Volume.
* **Intro/Outro Cameras**: The camera views displayed at the beginning or end of a match.

### Specialized and Obscure Objects

Certain objects are frequently used by creators in non-standard ways due to their unique properties:

* **Leaks B**: A colorable decal found in `Decals → Editable → Leaks B` that resembles a liquid leak.
* **Forerunner Inquisitor Door/Window**: Located at `Accents → Forerunner MP → Forerunner Door Inquisitor MP`, this object features forerunner lines within the frame and is used by creators to create more detailed windows than standard glass objects allow.
* **Forerunner Platform**: A nearly rectangular object (`Accents → Forerunner → Forerunner Platform 12 x 04 x 56`) with a large-scale, tiling texture that allows for budget-efficient construction of large forerunner surfaces.
* **Argyle Lift**: A hidden Banished Gravity Lift effect first identified on the developer map "Argyle" which features an unusually tall animation.

***

## Source Data

* Discord thread: [Forge Terminology](https://discord.com/channels/220766496635224065/1534038657269371060/1534038657269371060)

#### <mark style="color:green;">Contributors</mark>

Okom
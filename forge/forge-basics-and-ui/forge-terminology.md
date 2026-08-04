---
description: >-
  A comprehensive guide to the terminology used by creators and
  players within the Halo Forge ecosystem.
---

# Forge Terminology

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This article provides a glossary of terms relevant to working in Halo's level editor, covering foundational concepts, scripting logic, community vocabulary, and specialized objects used by creators.

## Essential Forge Concepts

* Forge: The level editor used in Halo games to create maps, prefabs, and scripted modes
* Forger: A person who creates content using Forge
* Map: A level that players can play on.
* Mode/Game Mode: A mode that is loaded alongside a map. A predefined ruleset that defines the objectives and gameplay mechanics of match.
* Prefab: A group of two or more objects that can be saved and shared with other creators. Players have created entire buildings, and saved them as prefabs.

### Scripting Terminology

* Node Graph: The node-based visual scripting interface of Halo Infinite's Forge. Very similar to UE5's Blueprint visual scripting graph. All forge scripting is done within the Node Graph.
* Node: A visual building block in the Node Graph that performs a specific operation or represents a piece of data. Nodes are connected together to define logic, data flow, or behavior.
* Script Brain/Mode Brain: A Forge object that contains the Node Graph. One Script Brain can hold 128 nodes and 512 connections between nodes.

## Creator Vocabulary and Objects

The following terms represent common vocabulary used by players and creators during map construction and within community discussions.

* HDS: Halo Design Set. A category of simple objects used in the blockout stage of a map, or for primitive shapes in general like cubes or spheres. These objects have a corner origin point.
* Primitives: Objects in the "Primitives" category in Forge, which are similar to the Halo Design Set objects in their purpose, but have a central origin point.
* Blockers: Invisible cube objects that are used for map containment. One-way, projectile-blocking, universal, team-based, vehicle-only, and player-only variants are available.
* TI-terrain: Terrain objects that inherit the terrain material and texture from the Forge Canvas terrain.
* The Browser: The UGC browser where players can browse published forge content from within the game.
* Red-racked: In reference to an item spawner—often a Weapon Rack—having the Spawn Logic set to "Dynamic (Expired)", or the Max Deployed-setting as "1.00", resulting in the item spawner's incoming timer display turning red the instant the item is picked up, and only beginning the blue timer progress towards the next spawn once the picked up item has been despawned.
* Callout: A named location on a map created by a Named Location Volume.
* Intro/Outro Cameras: The map-specific camera views that display at the start or end of a game.

### Specialized and Obscure Objects

The following entries refer to specific objects used within Forge for unique visual effects or structural purposes.

* Leaks B: A colorable decal found in `Decals → Editable → Leaks B` that looks like a liquid leak. The object was the first of its kind, and thus gained high popularity among forgers. [Read more](forge-interface/object-browser/hidden-forge-objects.md#leaks-b).
* Forerunner Inquisitor Door/Forerunner Window: A forerunner door object that looks like a window frame with some forerunner lines in the window, found in `Accents → Forerunner MP → Forerunner Door Inquisitor MP`. Forgers have used this object to make better looking windows than what the regular glass objects can illustrate.
* Forerunner Platform: A nearly rectangular forerunner object found in `Accents → Forerunner → Forerunner Platform 12 x 04 x 56` that has a uniquely largely scaled, tiling forerunner texture, which forgers have used to make large forerunner textures that aren't normally possible in a budget-efficient way.
* Argyle Lift: A hidden Banished Gravity Lift object that was first found on the developer-made Forge map "Argyle". The lift features a unusually tall gravity lift effect. [Read more](forge-interface/object-browser/hidden-forge-objects.md#argyle-lift).

***

## Source Data

* Discord thread: [Forge Terminology](https://discord.com/channels/220766496635224065/1534038657269371060/1534038657269371060)

#### <mark style="color:green;">Contributors</mark>

Okom
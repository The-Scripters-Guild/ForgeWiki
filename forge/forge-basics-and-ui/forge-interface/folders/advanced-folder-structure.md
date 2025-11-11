---
description: Examples of an advanced folder structure to use on Halo Infinite Forge maps.
---

# Advanced Folder Structure

<figure><img src="../../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

The folder structure doesn't have to be overly complicated to work efficiently. Below are some examples of advanced folder structures that experienced forgers have come up with, and are tuned to work for all object groups in a Forge map. An advanced folder structure is useful for categorizing every object type efficiently and semantically. Takes a bit longer to set up and takes up more budget, but is much more useful on larger projects or feature-rich maps.

## Advantages

The advantages to having an advanced folder structure are:

* All object types have a descriptive folder allocated for them
* Selecting or hiding specific groups of objects is easy and streamlined
* You are more willing to folderize objects correctly, when a good folder structure is set up

## Disadvantages

The disadvantages to having an advanced folder structure are:

* More budget usage as every folder takes up Forge Simulation memory. This only becomes an issue on maps with the Forge Simulation memory almost at 100% when attempting to re-do the folder structure
* Some forgers may find it too intimidating to use

## Examples

Examples of advanced folder structures used by experienced forgers:

### Okom1

<details>

<summary>General purpose</summary>

* .Non-Folderized Objects `root folder`
* 00.Layout
  * 0.Blockout
  * 1.Main Layout
  * 2.Skybox
  * 3.Detail (Collision)
  * 3.Detail (No Collision)
  * Terrain
* 01.Spawning
  * Initial Spawns
  * Respawn Points
  * Spawn Influence
* 02.Gameplay
  * Audio
  * Cameras
  * Equipment
  * Lifts and Teleporters
  * Named Locations
  * Ordnance, Cobra
  * Ordnance, Eagle
  * Ordnance, LSS
  * Ordnance, Middle
  * Vehicles
  * Weapons
* 03.Modes
  * Assault
  * Attrition
  * CTF
  * Elimination
  * Extraction
  * FFKOTH-1
  * FFKOTH-2
  * FFKOTH-3
  * FFKOTH-4
  * FFKOTH-5
  * Headhunter
  * Infection
  * King of the Hill
  * Land Grab
  * Oddball
  * Stockpile
  * Strongholds
  * Total Control
* 04.Nav Mesh
  * Cutters
  * Helpers
  * Markers
  * Seed Points
  * Temp. Geo
* 05\. Lighting
  * FX
  * Hide For Lighting Build
  * Lighting Modifiers
  * Lights
* 06.Containment
  * Inside Map
  * Kill Volumes
  * Outside Map
* 07.Scripting
  * Script1
  * Script2
  * Script3
* 08.Misc
  * Easter Eggs
  * Palette1
  * Palette2
  * Palette3

</details>

## MikRips

<details>

<summary>General purpose</summary>

* 00 Blockout
* 01 Gamemodes
* 02 Sandbox
  * Weapons Equipment
  * Initial Spawns
  * Respawns
  * Volumes
* 03 Blockers
  * Containment
  * Collision
* 04 Nav Mesh
  * Markers
  * Hints
  * Cutters
  * Nav Mesh Geo
* 05 Scripting
* 06 Foliage (Hide for Nav)
* 07 Terrain
  * Rocks misc
  * Trees
* 08 Lighting
  * Lights
  * Reflection volumes
* 09 Skybox
* 10 Map Art `root folder`

</details>

## nkdape

<details>

<summary>For the map <a href="https://www.halowaypoint.com/halo-infinite/ugc/maps/54cb69c3-9f60-4061-85c4-0ab3da4d234a">Hacksaw Canyon</a>:</summary>

* 01.Gameplay
  * Audio
  * Cameras
  * FX
  * Lifts
  * Script Brains
  * Spawn Influence
  * Spawns, Initial, FFA
  * Spawns, Initial, FFKOTH
  * Spawns, Initial, Infection
  * Spawns, Initial, Team
  * Spawns, Respawn - COBRA
  * Spawns, Respawn - EAGLE
  * Spawns, Respawn - MID
* 02.Modes
  * m01.Weapons, Equipment
  * m02.Vehicles - 0
  * m03.Coils
  * m04.Pods, EAGLE
  * m05.Pods, MID
  * m06.Pods, COBRA
  * m07.Pods, LSS
  * m10.BTB - 0
  * m11.CTF
  * m12.Total Control
  * m13.KOTH
  * m14.Strongholds
  * m15.Land Grab
  * m16.Stockpile
  * m17.Oddball
  * m18.Attrition, Elimination
  * m19.Extraction
  * m20.Infection
  * m21.FFKOTH.1
  * m21.FFKOTH.2
  * m21.FFKOTH.3
  * m21.FFKOTH.4
  * m21.FFKOTH.5
  * m21.FFKOTH.Weapons, Equipment
  * m22.Headhunter
* 03.Volumes
  * Kill, Hard
  * Kill, Soft
  * Named Locations
* 04.Nav Mesh, Objects
  * Nav Cutters
  * Nav Helpers
  * Nav Markers
  * Nav Seeds
* 05.Lighting
  * Lights
  * Probe, Reflections
* 06.Player Containment
  * Bounds Blockers
  * Exploit Blockers
  * FFKOTH Exclude Blockers
  * Smooth Blockers
* 10.Base.COBRA
  * C.BaseBottom
  * C.BaseTop01
  * C.BaseTop02
  * C.Spire\_Platform
  * C.Tower1
  * C.Tower2
* 10.Base.EAGLE
  * E.BaseBottom
  * E.BaseTop01
  * E.BaseTop02
  * E.Spire\_Platform
  * E.Tower1
  * E.Tower2 10.MID
  * M.Bunker1
  * M.Bunker2
  * M.BunkerGround
  * M.BunkerSpires
  * M.Cave
  * M.Circle
  * M.Fins
  * M.Ground
  * M.Monument
  * M.Spires
* 10.Misc
* 10.StageSpires
  * S.Spire1
  * S.Spire2
  * S.Spire3
* 11.Geology
  * G.Cave
  * G.Ground
  * G.Rocks
  * G.Rocks, Bounds
  * G.Rubble, Snow
  * G.Terrain
* 12.Foliage
* 13.Decals
* 99.TEMP

</details>

If you're confused what the `root folder` means, see [Set as Root Folder](./#set-as-root-folder).

***

#### <mark style="color:green;">Contributors</mark>

Okom\
MikRips\
nkdape

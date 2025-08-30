---
description: >-
  A prefab used to block all 27 invisible Backup Spawn Points on any Forge
  canvas so they can't spread Nav Mesh.
---

# tsg navCutters

## Bookmark

Bookmark the prefab via this [filter link](https://www.halowaypoint.com/halo-infinite/ugc/browse?searchTerm=tsg+navcutters\&assetKind=Prefab\&page=1\&tags=tsg) to find the most up-to date version.

## Purpose

This prefab is designed to block the spread of Nav Mesh from all 27 [invisible Backup Spawn Points](../../../halo-infinite/forge/player-spawning/backup-spawn-points/) on all Forge canvases by having a large enough Nav Cutter boundary around each Backup Spawn Point.

## Usage

### Placing the prefab

1. Position your Forge monitor at 0, 0, 500 and aim straight down
2. Spawn in the prefab
3.
   1. If after placing the prefab it is unselectable, go into Play Mode and then back into Test Mode and the prefab should become selectable.
4. Set the location of the prefab to 0, 0, 505
5. Set the rotation of th prefab to 0, 0, 0
6. Optional: Ungroup the prefab and delete any unnecessary Nav Cutters

## Good to note

Once this prefab is in place, you must have at least one non-blocked [Nav Mesh generation Root Point](../../../halo-infinite/forge/nav-mesh/nav-mesh-generation-root-points/) object present on the map for the Nav Mesh to be able to build. Otherwise you will get a [build error](../../../halo-infinite/guides-and-tutorials/forge/nav-mesh/fixing-nav-mesh-build-issues/#navigation-data-generation-failed).

***

**Contributors**\
Okom

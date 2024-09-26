---
description: A prefab used to block all 27 invisible Backup Spawn Points on any Forge canvas so they can't spread Nav Mesh.
---

# tsg navCutters

## Bookmark

Bookmark the prefab via this <a href="https://www.halowaypoint.com/halo-infinite/ugc/browse?searchTerm=tsg+navcutters&assetKind=Prefab&page=1&tags=tsg" target="_blank">filter link</a> to find the most up-to date version.

## Purpose

This prefab is designed to block the spread of Nav Mesh from all 27 <a href="/halo-infinite/forge/player-spawning/backup-spawn-points" target="_blank">invisible Backup Spawn Points</a> on all Forge canvases by having a large enough Nav Cutter boundary around each Backup Spawn Point.

## Usage

### Placing the prefab

<ol>
  <li>Position your Forge monitor at 0, 0, 500 and aim straight down</li>
  <li>Spawn in the prefab</li>
    <ol>
      <li>If after placing the prefab it is unselectable, go into Play Mode and then back into Test Mode and the prefab should become selectable.</li>
    </ol>
    <li>Set the location of the prefab to 0, 0, 505</li>
    <li>Set the rotation of th prefab to 0, 0, 0</li>
    <li>Optional: Ungroup the prefab and delete any unnecessary Nav Cutters</li>
</ol>

## Good to note

Once this prefab is in place, you must have at least one non-blocked <a href ="/halo-infinite/forge/nav-mesh/nav-mesh-generation-root-points" target="_blank">Nav Mesh generation Root Point</a> object present on the map for the Nav Mesh to be able to build. Otherwise you will get a <a href ="/halo-infinite/guides-and-tutorials/forge/nav-mesh/fixing-nav-mesh-build-issues#navigation-data-generation-failed" target="_blank">build error</a>.

<hr>

**Contributors**\
Okom

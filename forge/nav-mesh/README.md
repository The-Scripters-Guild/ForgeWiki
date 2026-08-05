---
description: >-
  Topics about Nav Mesh and NPC Units in Halo Infinite, and how to implement
  them with the Forge tool.
---

# Nav Mesh

The Nav Mesh section focuses on the objects, technical details and applications for the navigation mesh in Halo Infinite.

A nav mesh is the platform for [NPC Units](npc-units/) to navigate around a level, and while it has been used in previous Halo titles with internal tools for campaign AI, Halo Infinite is the first installment where editing the nav mesh on a Forge map is available to the Forgers.

Having a well designed and thorough nav mesh setup on your level is essential for experiences that rely on pathfinding such as [Firefight:King of The Hill](../modes/firefight/firefight-koth.md), but also a good habit to make sure that the level can be played with bots, if enough players can't be gathered for an experience. A working nav mesh setup is also mandatory for matchmaking experiences that may utilize [bot backfill](/broken/pages/XMhSNwCgFl1gbfB32Hcm).

Nav mesh is used by bots and AI to navigate around a level just like how players can. Nav mesh can only be built and inspected on Forge canvas-based levels, and is generally not an option on dev-made levels. While the nav mesh can't be inspected on dev-made levels, it is still present on them, otherwise bots couldn't pathfind on the level.



Nav Objects are objects used to alter the generation of nav mesh in Halo Infinite's Forge, which will impact how [bots](npc-units/bots.md) and [AI](npc-units/ai.md) navigate around the level. Usually nav mesh should be built once and then the nav mesh coverage inspected to see what is missing and can be fixed with the help of the nav objects.

* Nav Seed Points
* Nav Helpers
* Nav Cutters
* Bot Nav Markers

## Learn more about

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Nav Objects</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="/broken/pages/MPKxydqLWKXy9BcW3yOk">Broken link</a></td></tr><tr><td>Nav Mesh Generation</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="/broken/pages/BpmLL7s9nGdHlJ1yKH7E">Broken link</a></td></tr><tr><td>Game AI</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="npc-units/">npc-units</a></td></tr></tbody></table>

***

#### <mark style="color:green;">Contributors</mark>

Okom

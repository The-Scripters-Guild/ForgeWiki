---
description: >-
  Each map in Halo Infinite download files attached to the map each
  time the map is loaded. In addition to the map .mvar file itself,
  these include the Nav Mesh, Audio, and Lighting data files.
---

# Baked-In Map Data

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When a player loads into a Halo Infinite map, the client downloads several specific data files to ensure consistent environmental behavior across all players. These include auxiliary files that work alongside the primary `.mvar` file.

## Downloaded Environmental Files

In addition to the main map `.mvar` file, various specialized blobs are downloaded during the loading process. These "baked-in" files provide essential information for navigation, sound propagation, and lighting.

### Shared Data Types
The following data types are included in the map's download package:

* Nav Mesh ([navmesh.blob](https://blobs-infiniteugc.svc.halowaypoint.com/ugcstorage/map/ee5e295f-c298-4f2f-a64f-dbf0a1087ad8/d8dab2e7-3f98-4914-8382-faa5b9587b45/navmesh.blob))
* Audio occlusion ([audioocclusion.blob](https://blobs-infiniteugc.svc.halowaypoint.com/ugcstorage/map/ee5e295f-c298-4f2f-a64f-dbf0a1087ad8/d8dab2e7-3f98-4914-8382-faa5b9587b45/audioocclusion.blob))
* Lighting ([lightprobes.blob](https://blobs-infiniteugc.svc.halowaypoint.com/ugcstorage/map/ee5e295f-c298-4f2f-a64f-dbf0a1087ad8/d8dab2e7-3f98-4914-8382-faa5b9587b45/lightprobes.blob))

## Local Reflection Generation

While the files listed above are shared globally and baked into the map, reflection data functions differently. 

Reflection data is generated locally for each player when they load into a map. Because this process happens on the individual client side during loading, it is not considered part of the baked-in data shared by all players.

{% hint style="info" %}
The distinction between shared environmental data and local reflection generation ensures that core gameplay elements like navigation and audio remain synchronized for everyone in a session.
{% endhint %}

***

## Source Data

* Discord thread: [Baked-In Map Data](https://discord.com/channels/220766496635224065/1534001681073967227/1534001681073967227)

#### <mark style="color:green;">Contributors</mark>

Okom
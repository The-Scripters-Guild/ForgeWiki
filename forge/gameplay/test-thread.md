---
description: >-
  Guidance on using the spawn properties node to manage object
  spawning, limits, and team assignments in Forge maps.
---

# Test Thread

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Managing how objects appear and reappear in a Forge map is essential for maintaining gameplay balance. By utilizing specific node settings, creators can control the frequency and availability of spawned items.

## Object Spawning Configuration

The spawn properties node is used to configure how objects are instantiated and managed within a Forge map. This node provides control over spawning rates, population limits, and team-specific assignments.

### The Spawn Properties Node

The node functions by applying specific parameters to objects, ensuring that the map environment remains stable and follows the intended gameplay loop. Creators can use this to prevent object overpopulation or to ensure that certain items are only accessible to specific teams.

## Key Configuration Parameters

To effectively manage object behavior, three primary settings within the node should be configured:

#### Spawning Limits and Timing

* `max_count`: This setting defines the maximum number of objects allowed to exist at one time.
* `respawn_delay`: This parameter controls the rate of spawning by determining the time elapsed before an object respawns.

#### Team Management

* `team_filter`: This setting allows creators to manage team assignments, determining which teams are eligible to interact with or be associated with the spawned objects.

{% hint style="info" %}
Using these settings in conjunction can help prevent performance issues caused by excessive object counts while ensuring players have consistent access to necessary items.
{% endhint %}

***

## Source Data

* Discord thread id: `12345`

#### <mark style="color:green;">Contributors</mark>

TestUser
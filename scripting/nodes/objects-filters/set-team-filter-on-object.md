---
description: >-
  Restricts object interaction to a specific team or prevents a
  specific team from interacting.
---

# Set Team Filter On Object

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This node applies a team-based restriction to a specific object, determining which teams are permitted to interact with it. If the `Invert` input is enabled, the specified team is blocked from interacting instead.

## Description
Adds a filter to the Object that only allows the specified [Team](../variables-basic/team.md) to interact with the object. If Inverted, the object cannot be interacted with by this `Team`; filters must be reapplied to objects that are respawned.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------|
| Object | Object | Yes | Object to set filter on for team. |
| Team | Team | Yes | Team to set filter for. |
| Invert | Boolean | Yes | If TRUE, team cannot access object. If FALSE, team can access object. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------|
| (none) | | |

{% warning %}
Certain objects and interactions may bypass or exhibit unexpected behavior when team filters are applied.
{% endwarning %}

### Bypassed Objects
The following objects do not appear to respect the team filter:
* Ammo Crates
* Scriptable Switches (including Invisible, Banished Terminal, Banished Touchpanel, Banished Touchpanel Wall, Forerunner Terminal, Forerunner Terminal Worn, and UNSC Console)
* Power Sockets (including UNSC, UNSC Green Sand, UNSC Engine Blue, UNSC Engine Red, and UNSC Engine Yellow variants)

### Other Behaviors
* **Weapons:** Players can still perform refill pickups on weapons even if a filter is applied.
* **Hacking Terminals:** The filter functions, but there is no interact button when no filter is on.
## Source Data

* Discord thread: [Object Filters have limitations](https://discord.com/channels/220766496635224065/1321416792643604551/1321416792643604551)

#### <mark style="color:green;">Contributors</mark>

AddiCt3d 2CHa0s\
Artifice
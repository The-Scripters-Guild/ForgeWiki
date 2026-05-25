---
description: >-
  Restricts object interaction to specific players or prevents
  interaction through inversion.
---

# Set Player Filter On Object

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

This node provides a method to control which players can interact with a given object. It is commonly used to manage object availability during scripted sequences or to limit access to specific players.

![](../../../.gitbook/assets/set-player-filter-on-object.png)

## Description
Adds a filter to the Object that only allows the specified Player to interact with the object. If Inverted, the object cannot be interacted with by the Player; filters must be reapplied to objects that are respawned.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------|
| Player | Player | Yes | Player to set filter for. |
| Object | Object | Yes | Object to set filter on for player. |
| Invert | Boolean | Yes | If TRUE, player cannot access object. If FALSE, player can access object. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| (none) | | |

## Usage Notes
* **Preventing Double Activation**: To prevent a switch or object from being triggered multiple times while a process is already in progress, use this node with the `Invert` input set to `TRUE`. This effectively "locks" the object from interaction until the filter is updated or removed.

{% info %}
This node has been noted to work on generic objectives.
{% endinfo %}
## Source Data

* Discord thread: [How to Disable a Switch?](https://discord.com/channels/220766496635224065/1508158587116064898/1508158587116064898)

#### <mark style="color:green;">Contributors</mark>

AddiCt3d 2CHa0s\
Halloween\
rocksk8r2k9\
swagonflyyyy (Mr. Blackwell)\
AddiCt3d 2CHa0s 🎮 💻
# On Generic Skull Pickup
![alt text](../../../.gitbook/assets/on-generic-skull-pickup.png)
## Description
Event called when a player explicitly picks up the given *Generic Skull*

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Skull | Object | Yes | Which object to listen for being picked up. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Acquiring Player | Object | Which player picked it up.|
| Pickup Position | Vector3 | Location the object was at before it was picked up. |

\
\
**Contributors**

AddiCt3d 2CHa0s
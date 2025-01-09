# On Generic Zone State Changed
![alt text](../../../.gitbook/assets/on-generic-zone-state-changed.png)
## Description
Event called whenever the *Generic Zone* enters a new *Control State*

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Zone | Generic Zone | Yes | Which zone to listen to this event for. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Previous Control State | Control State | The zone's Control State before the change.|
| Current Control State | Control State | The zone's current Control State |

\
\
**Contributors**

AddiCt3d 2CHa0s
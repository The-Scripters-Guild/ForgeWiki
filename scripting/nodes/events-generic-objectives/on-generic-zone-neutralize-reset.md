# On Generic Zone Neutralize Reset
![alt text](../../../.gitbook/assets/on-generic-zone-neutralize-reset.png)
## Description
Event called when the *Controlling Team* that owns the *Generic Zone* resets their Control Decay to 0, affectively securing the zone.

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Zone | Generic Zone | Yes | Which zone to listen to this event for. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Controlling Team | Team | The team that has reset their zone back to their control.|

\
\
**Contributors**

AddiCt3d 2CHa0s
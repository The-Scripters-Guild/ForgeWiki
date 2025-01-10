# Was With Specific Vehicle
![](../../../.gitbook/assets/was-with-specific-vehicle.png)
## Description
Queries a *DeathContext* from the **On Player Killed** or **On AI Unit Killed** event. Returns true if the killing blow came from the Vehicle instance. Unreliable if the player has left the vehicle since the kill.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| Death Context | Death Context | True | Which Death Context to check if kill was using specific vehicle. |
| Vehicle | Object | True | Which vehicle to check against, whether it was the one that made the kill. |

## Outputs
| Output           | Type             | Description												     |
|------------------|------------------|--------------------------------------------------------------|
| Was With Specific Vehicle | Boolean | TRUE if kill was made using specified vehicle. |

\
\
**Contributors**

AddiCt3d 2CHa0s


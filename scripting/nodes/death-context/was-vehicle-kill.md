# Was Vehicle Kill
![](../../../.gitbook/assets/was-vehicle-kill.png)
## Description
Queries a *DeathContext* from the **On Player Killed** or **On AI Unit Killed** event. Returns true if the killing blow came from a vehicle damage source.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| Death Context | Death Context | True | Which Death Context to check if kill was vehicle damage. |

## Outputs
| Output           | Type             | Description												     |
|------------------|------------------|--------------------------------------------------------------|
| Was Vehicle Kill| Boolean | TRUE if kill was caused by a vehicle. |
| Was Splatter | Boolean | TRUE if killed player was ran over by a vehicle. |

\
\
**Contributors**

AddiCt3d 2CHa0s

# Was Weapon Kill
![alt text](../../../.gitbook/assets/was-weapon-kill.png)
## Description
Queries a *DeathContext* from the **On Player Killed** or **On AI Unit Killed** event. Returns true if the killing blow came froma weapon damage source.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| Death Context | Death Context | True | Which Death Context to check if kill was from a weapon. |

## Outputs
| Output           | Type             | Description												     |
|------------------|------------------|--------------------------------------------------------------|
| Was Weapon Kill| Boolean | TRUE unit was killed by a weapon. |
| Was Headshot | Boolean | True if kill was a headshot. |

\
\
**Contributors**

AddiCt3d 2CHa0s

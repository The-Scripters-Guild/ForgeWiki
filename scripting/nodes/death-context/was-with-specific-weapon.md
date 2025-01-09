# Was With Specific Weapon
![alt text](../../../.gitbook/assets/was-with-specific-weapon.png)
## Description
Queries a *DeathContext* from the **On Player Killed** or **On AI Unit Killed** event. Returns true if the killing blow came from the Weapon instance..

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| Death Context | Death Context | True | Which Death Context to check if kill was with specific weapon. |
| Weapon | Object | True | Which weapon to check if kill was made from it. |

## Outputs
| Output           | Type             | Description												     |
|------------------|------------------|--------------------------------------------------------------|
| Was With Specific Weapon | Boolean | TRUE if weapon that made the kill is the same weapon given. |

\
\
**Contributors**

AddiCt3d 2CHa0s

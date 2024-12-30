# Was With Weapon Type
![alt text](../../../.gitbook/assets/was-with-weapon-type.png)
## Description
Queries a *DeathContext* from the **On Player Killed** or **On AI Unit Killed** event. Returns true if the killing blow came from a matching Weapon Type.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input            | Type             | Required | Description												    |
|------------------|------------------|----------|--------------------------------------------------------------|
| Death Context | Death Context | True | Which Death Context to check if kill was with given Weapon Type. |
| Weapon Type | Weapon Type | True | Which Weapon Type to check against, if kill was made by it. |

## Outputs
| Output           | Type             | Description												     |
|------------------|------------------|--------------------------------------------------------------|
| Was With Weapon Type | Boolean | TRUE if unit was killed with same Weapon Type as given. |

\
\
**Contributors**

AddiCt3d 2CHa0s

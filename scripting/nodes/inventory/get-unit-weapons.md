# Get Unit Weapons
![](../../../.gitbook/assets/get-unit-weapons.png)
## Description
Returns object references to the weapons in the Unit's inventory. Pins return an invalid reference if the Unit does not have a weapon.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Unit | Object | Yes | Which unit to get weapons for. |
| Weapon Type | Weapon Type | Yes | The weapon type to check if player is holding. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Equipped Weapon | Object | Unit's equipped weapon if it exists. |
| Unquipped Weapon | Object |  Unit's unequipped weapon if it exists. |

\
\
**Contributors**

AddiCt3d 2CHa0s
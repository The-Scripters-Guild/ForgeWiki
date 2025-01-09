# On Weapon Pickup
![alt text](../../../.gitbook/assets/on-weapon-pickup.png)
## Description
Event called when a player explicitly picks up a weapon. Ammo refills for a weapon a player is already holding will NOT trigger this event.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node listens for an Event, then triggers it's node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| N/A | N/A | N/A | |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Acquiring Player | Object | Which player picked up the weapon.|
| Weapon | Object | The weapon that is picked up.|
| Weapon Position | Vector3 | Location weapon was at when it was picked up.|

\
\
**Contributors**

AddiCt3d 2CHa0s
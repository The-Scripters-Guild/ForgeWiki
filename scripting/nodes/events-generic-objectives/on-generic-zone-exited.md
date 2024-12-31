# On Generic Zone Exited
![alt text](../../../.gitbook/assets/on-generic-zone-exited.png)
## Description
Event called whenever a player exits the *Generic Zone*'s boundary. Behaves like an Area Monitor, but only tracks players and players in vehicles.

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Zone | Generic Zone | Yes | Which zone to listen to this event for. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Player | Object | Player who has exited the generic zone.|

\
\
**Contributors**

AddiCt3d 2CHa0s
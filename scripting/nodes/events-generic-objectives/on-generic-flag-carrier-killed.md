# On Generic Flag Carrier Killed
![alt text](../../../.gitbook/assets/on-generic-flag-carrier-killed.png)
## Description
Event called whenever a player carrying the *Generic Flag* has been killed

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Flag Spawn | Generic Flag Spawn | Yes | Which object to listen when it's flag carrier is killed. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Killed Player | Object | Which player was the flag carrier that was killed.|
| Killing Unit | Object | Who killed the carrier.|
| Flag | Object | That flag that was being carried.|

\
\
**Contributors**

AddiCt3d 2CHa0s
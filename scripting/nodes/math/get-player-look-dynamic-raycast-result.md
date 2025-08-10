# Get Player Look Dynamic Raycast Result
![](../../../.gitbook/assets/get-player-look-dynamic-raycast-result.png)
## Description
Executes a physics raycast command that collides with dynamic objects from the look direction of a player.  

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Player | Player | Yes | Player to use for look to get dynamic raycast result. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Hit Position | Vector3 | Position, if any, where raycast collides with dynamic object. |
| Normal | Vector3 | Normalized vector based on Hit Position. |
| Hit Object | Object | Dynamic object, if any, that raycast collides with. |
| Hit Detected | Boolean | TRUE if raycast has collided with a dynamic object. |


\
\
**Contributors**

AddiCt3d 2CHa0s \
Okom \
Jordan9232
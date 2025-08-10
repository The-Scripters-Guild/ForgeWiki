# Get Static Bullet Raycast Result
![](../../../.gitbook/assets/get-static-bullet-raycast-result.png)
## Description
Executes a physics raycast command that collides with the static bullet environment.  

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Start Position | Vector3 | Yes | Position at which to start raycast. |
| End Position | Vector3 | Yes | Position at which to end raycast. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Hit Position | Vector3 | Position, if any, where raycast collides. |
| Normal | Vector3 | Normalized vector based on Hit Position. |
| Hit Detected | Boolean | TRUE if raycast has collided. |

\
\
**Contributors**

AddiCt3d 2CHa0s \
Okom \
Jordan9232
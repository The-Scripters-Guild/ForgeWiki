# Get Generic List Variable
![](../../../.gitbook/assets/get-generic-list-variable.png)
## Description
Get the Generic List variable stored with the matching identifier in the matching Scope. The Object pin is only used when accessing the Object scope.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Identifier | String | Yes | The string id for this variable. |
| Scope | Scope | Yes | Determines if this list can be accessed by other brains, and what the list is associated with. |
| Object | Object | No | If Scope is Object, which object this variable is associated to.

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Value | List | The list held in this variable. |

\
\
**Contributors**

AddiCt3d 2CHa0s
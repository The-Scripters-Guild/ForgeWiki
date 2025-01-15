# Get Generic Item Variable
![](../../../.gitbook/assets/get-generic-item-variable.png)
## Description
Get the Generic Item variable stored with the matching identifier in the matching Scope. The Object pin is only used when accessing the Object scope.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data for an Execution node.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Identifier | String | Yes | The string id for this variable. |
| Scope | Scope | Yes | Determines if this item can be accessed by other brains, and what the item is associated with. |
| Object | Object | No | If Scope is Object, which object this variable is associated to.

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Value | item | The item held in this variable. |

\
\
**Contributors**

AddiCt3d 2CHa0s
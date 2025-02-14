# For Each Object
![](../../../.gitbook/assets/for-each-object.png)
## Description
Execute connected functions for each object in the Objects list

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Objects | Object List | Yes | Any list of objects. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| On Completion | Event | Continues node string after this node runs it's loop through the list. |
| Execute Per Object | Function | Runs attached nodes for each object in the list. |
| Current Object | Object | Outputs current object in the list. |
| Current Iteration | Number | Outputs the how many times the loop has run so far before completion. Will be object's index in the list. |

\
\
**Contributors**

AddiCt3d 2CHa0s
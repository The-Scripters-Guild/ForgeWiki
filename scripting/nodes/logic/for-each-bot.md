# For Each Bot
![](../../../.gitbook/assets/for-each-bot.png)
## Description
Execute connected functions for each bot in the Objects list. Identical to For Each Object except it ignores non-bot objects in the list.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Objects | Object List | Yes | Any list of objects. Non bots will be ignored. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| On Completion | Event | Continues node string after this node runs it's loop through the list. |
| Execute Per Bot | Function | Runs attached nodes for each bot in the list. |
| Current Bot | Object | Outputs current bot in the list. |
| Current Iteration | Number | Outputs the how many times the loop has run so far before completion. |

\
\
**Contributors**

AddiCt3d 2CHa0s
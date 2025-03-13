# Scope
![](../../../.gitbook/assets/scope.JPG)

## Description
The variable scope at which a variable is stored. Local is stored in the script brain in which is was declared, whereas Global can be accessed from any script brain. Object is stored on each object in the game and must be accessed by providing an object to the variable node.

## Node Type
Nodes fall into two basic categories: Data and Execution. This node supplies Data.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| (none) |  |  |  |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Scope | Boolean | Local scope can only be accessed by the brain it is declared in. Global and Object scope can be accessed by any brain. |
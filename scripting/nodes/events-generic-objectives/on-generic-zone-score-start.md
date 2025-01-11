# On Generic Zone Score Start
![](../../../.gitbook/assets/on-generic-zone-score-start.png)
## Description
Event called whenever the *Controlling Team* gains scoring control (i.e. uncontested, no delay, etc.) of the *Generic Zone* and the zone begins emitting **On Generic Zone Score Tick** events.

## Node Type
Nodes fall into two basic categories: Data and Execution. This Execution node fires when something happens in the game that triggers it, and starts off the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Generic Zone | Generic Zone | Yes | Which zone to listen to this event for. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Controlling Team | Team | The team that has started scoring control of the zone.|

\
\
**Contributors**

AddiCt3d 2CHa0s


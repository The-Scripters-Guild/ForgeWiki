# Register On Weapon Pickup

{% hint style="important" %}
This node was originally created to cover instances where weapons created using **Spawn Mode Object** might not trigger the **On Weapon Pickup** Event, but they do, so it's currently not needed.
{% endhint %}

![](../../../.gitbook/assets/register-on-weapon-pickup.png)
## Description
(Registers a weapon so an) Event executes when a player explicitly picks up the given _Weapon_.  

## Node Type
Nodes fall into two basic categories: Data and Execution. This node Executes a function directly in the node string.

## Inputs
| Input | Type | Required | Description |
|------------------|------------------|----------|--------------------------------------------------------------|
| Weapon | Weapon | Yes | Which weapon to listen for it being picked up. |

## Outputs
| Output | Type | Description |
|------------------|------------------|--------------------------------------------------------------|
| Acquiring Player | Player | Deprecated. |
| Pickup Position | Vector3 | Deprecated. |


\
\
**Contributors**

AddiCt3d 2CHa0s \
Okom \
Jordan9232
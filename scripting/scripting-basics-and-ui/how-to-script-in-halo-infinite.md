# How To Script In Halo Infinite?

{% hint style="warning" %}
This article is a stub. You can help TSG Forge Wiki by expanding it.
{% endhint %}

{% content-ref url="../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md" %}
[submitting-content-to-the-wiki.md](../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md)
{% endcontent-ref %}



### How do I script in Halo Infinite?

Aside from the obvious first step of creating a Forge lobby and loading a level in a Forge session, one must place a Script Brain ( Gameplay > Scripting ) and use the radial menu to open that Script Brain's node graph. At that point you will be able to place and connect nodes to create circuits, which is the equivalent of 'writing code' in visual programming.

### What is a node graph?

Visual programming systems function similarly to flow charts. A node graph is the place, interface, and document where circuits are defined via placing and connecting nodes. Each Script Brain you place in Forge will have its own node graph that will allow you to place up to 128 nodes and make up to 512 connections. Additional brains can be placed to allow for placing more nodes, but each brain will have that same limit. When opening the node graph interface, the graph connected to the last selected Script Brain will be the one that opens.

### What is a node?

Nodes are the building blocks of visual programming. Acting similar to the shapes that one would connect with arrows to create a flow chart, each node performs a specific task and then either passes along data or triggers the next node in the circuit via its output. Nodes all have some combination of input and output pins that can be connected to each other, if the two that are being connected are both compatible and not being prevented from connecting because of some exclusionary rule.

### How do I test my code?

In Forge, there are multiple 'modes' that can be accessed. By default, the user is in Edit Mode and the player model is a Forge Monitor. Users can take control of a spartan biped at their current location in Edit Mode by transitioning to Test Mode, but this will not build the node graph for the level nor execute code from it. To test scripting in Forge, the user must enter Play Mode, which spawns the player in at a proper spawn point and simulates a play session. Some code, notably anything to do with FFA Affiliations, must be tested in Customs.

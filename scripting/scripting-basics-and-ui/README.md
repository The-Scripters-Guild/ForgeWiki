---
description: >-
  Topics about the basics of what Scripting and the Node Graph is in Halo
  Infinite, and how to use its features.
---

# Scripting Basics and UI

This section will teach you what Scripting means in Halo Infinite, and how to use the Node Graph interface to create scripts.

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt=""><figcaption></figcaption></figure>

## How to Script in Halo Infinite?

Scripting in Halo Infinite is done in the form of visual programming via a node graph interface within a Script Brain or a Mode Brain object. To spawn in a Script Brain, go into Test Mode in Forge and follow these steps based on your input type:

{% tabs %}
{% tab title="Keyboard and Mouse" %}
Option 1:

1. Press `N` to spawn a Script Brain and open it automatically

Option 2:

1. Spawn the Script Brain from the [Object Browser](../../forge/forge-basics-and-ui/forge-controls-and-menus/object-browser.md) from `Gameplay` -> `Scripting` -> Script Brain
2. With the Script Brain selected, Hold `Q` to open the Tools Menu and select the top option: "Node Graph"
{% endtab %}

{% tab title="Controller" %}
1. Spawn the Script Brain from the [Object Browser](../../forge/forge-basics-and-ui/forge-controls-and-menus/object-browser.md) from `Gameplay` -> `Scripting` -> Script Brain
2. With the Script Brain selected, Hold <mark style="color:yellow;">`Y`</mark> to open the Tools Menu and select the top option: "Node Graph"
{% endtab %}
{% endtabs %}

Now you should have the node graph open, which is the interface where scripts can be built in with the help of [Nodes](../nodes/). Connecting these nodes together creates circuits, which is the equivalent of writing code in visual programming.

### What is a node graph?

Visual programming systems function similarly to flow charts. A node graph is the place, interface, and document where circuits are defined via placing and connecting nodes. Each Script Brain you place in Forge will have its own node graph that will allow you to place up to 128 nodes and make up to 512 connections.

Additional brains can be placed to allow for placing more nodes, but each brain will have that same limit. When opening the node graph interface, the graph connected to the last selected Script Brain will be the one that opens.

{% content-ref url="../nodes/" %}
[nodes](../nodes/)
{% endcontent-ref %}

{% content-ref url="../node-data/connection-pins/" %}
[connection-pins](../node-data/connection-pins/)
{% endcontent-ref %}

### How do I test my code?

In Forge, there are multiple 'modes' that can be accessed. By default, the user is in Edit Mode and the player model is a Forge Monitor. Users can take control of a spartan biped at their current location in Edit Mode by transitioning to Test Mode, but this will not build the node graph for the level nor execute code from it.

To test scripting in Forge, the user must enter Play Mode, which spawns the player in at a proper spawn point and simulates a play session. Some code, notably anything to do with FFA Affiliations, must be tested in Customs.

{% content-ref url="../../forge/forge-basics-and-ui/play-mode-and-test-mode.md" %}
[play-mode-and-test-mode.md](../../forge/forge-basics-and-ui/play-mode-and-test-mode.md)
{% endcontent-ref %}



## Learn more about

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Node Graph Controls and Menus</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="node-graph-controls-and-menus/">node-graph-controls-and-menus</a></td></tr><tr><td>Node Graph Properties</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="node-graph-properties.md">node-graph-properties.md</a></td></tr></tbody></table>



#### <mark style="color:green;">Contributors</mark>

Okom\
Captain Punch

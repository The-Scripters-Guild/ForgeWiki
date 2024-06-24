---
description: >-
  Nodes are function blocks in visual programming that can be connected to other
  nodes to create a script in Halo Infinite.
---

# Nodes

Nodes are the building blocks of visual programming. Acting similar to the shapes that one would connect with arrows to create a flow chart, each node performs a specific task and then either passes along data or triggers the next node in the circuit via its output. Nodes all have some combination of input and output pins that can be connected to each other, if the two that are being connected are both compatible and not being prevented from connecting because of some exclusionary rule.

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt=""><figcaption></figcaption></figure>

## Node types

Node types are a way to organize nodes based on what they do. While there are nodes of various categories within Halo Infinite, _Node Types_, specifically designates nodes based on their characteristics.

### Event Nodes (Event Listeners)

* Triggered by a game event, or custom event.
* Can temporarily store and provide data via its output connection pins.
* May accept data inputs which arm or configure the event.
* Notably missing a input (left-side) execution (diamond) pin.

### Execution Nodes

* Triggered by an execution connection via it's input execution pin.
* May also temporarily store and provide date via its output connection pins, as well as require or receive optional input data to successfully execute.
* All Execution Nodes will have an input execution pin on the left that must be connected to either an Event Node, or a string of Execution Nodes that begins with an Event Node, or the graph will fail to build.

### Data Nodes

* Has no execution pins.
* Performs an operation when an execution node it is related to is triggered. Data nodes send information forward and can be combined to create complex operations to prepare data for an execution node.
* May feed into one or many execution nodes within the same event.
* Some Data Nodes have their output restricted to only working within a single chain of execution/circuit.



## Learn more about node categories

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>AI</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ai/">ai</a></td></tr><tr><td>AI ADVANCED</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ai-advanced/">ai-advanced</a></td></tr><tr><td>AI MODIFIERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ai-modifiers/">ai-modifiers</a></td></tr><tr><td>AI WAVES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ai-waves/">ai-waves</a></td></tr><tr><td>AUDIO</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="audio/">audio</a></td></tr><tr><td>BOTS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="bots/">bots</a></td></tr><tr><td>DEATH CONTEXT</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="death-context/">death-context</a></td></tr><tr><td>DEBUG</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="debug/">debug</a></td></tr><tr><td>EVENTS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events/">events</a></td></tr><tr><td>EVENTS AI</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-ai/">events-ai</a></td></tr><tr><td>EVENTS CUSTOM</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-custom/">events-custom</a></td></tr><tr><td>EVENTS GENERIC OBJECTIVES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-generic-objectives/">events-generic-objectives</a></td></tr><tr><td>EVENTS INVENTORY</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-inventory/">events-inventory</a></td></tr><tr><td>EVENTS MODES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-modes/">events-modes</a></td></tr><tr><td>EVENTS PLAYERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="events-players/">events-players</a></td></tr><tr><td>GAME MODE</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="game-mode/">game-mode</a></td></tr><tr><td>GAME MODE FIREFIGHT</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="game-mode-firefight/">game-mode-firefight</a></td></tr><tr><td>GENERIC OBJECTIVES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="generic-objectives/">generic-objectives</a></td></tr><tr><td>INVENTORY</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="inventory/">inventory</a></td></tr><tr><td>INVENTORY EQUIPMENT</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="inventory-equipment/">inventory-equipment</a></td></tr><tr><td>LISTS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="lists/">lists</a></td></tr><tr><td>LISTS CASTS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="lists-casts/">lists-casts</a></td></tr><tr><td>LOGIC</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="logic/">logic</a></td></tr><tr><td>LOGIC COMPARE</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="logic-compare/">logic-compare</a></td></tr><tr><td>MATH</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="math/">math</a></td></tr><tr><td>OBJECTS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="objects/">objects</a></td></tr><tr><td>OBJECTS FILTERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="objects-filters/">objects-filters</a></td></tr><tr><td>OBJECTS TRANSFORM</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="objects-transform/">objects-transform</a></td></tr><tr><td>PLAYERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="players/">players</a></td></tr><tr><td>SKULLS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="skulls/">skulls</a></td></tr><tr><td>STOPWATCHES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="stopwatches/">stopwatches</a></td></tr><tr><td>TRAITS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="traits/">traits</a></td></tr><tr><td>TRAITS AI</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="traits-ai/">traits-ai</a></td></tr><tr><td>TRAITS PLAYERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="traits-player/">traits-player</a></td></tr><tr><td>UI</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ui/">ui</a></td></tr><tr><td>UI NAV MARKERS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="ui-nav-markers/">ui-nav-markers</a></td></tr><tr><td>UNITS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="units/">units</a></td></tr><tr><td>VARIABLES ADVANCED</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="variables-advanced/">variables-advanced</a></td></tr><tr><td>VARIABLES BASIC</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="variables-basic/">variables-basic</a></td></tr><tr><td>VARIABLES LITERALS</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="variables-literals/">variables-literals</a></td></tr><tr><td>VEHICLES</td><td><a href="../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="vehicles/">vehicles</a></td></tr></tbody></table>

***

#### <mark style="color:green;">Contributors</mark>

Captain Punch\
AgentZero\
Okom

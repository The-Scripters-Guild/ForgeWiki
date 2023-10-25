# Nodes

Node types are a way to organize nodes based on what they do. While there are nodes of various categories within Halo Infinite, _Node Types_, specifically designates nodes based on their characteristics.

Event Nodes (Event Listeners)

* Triggered by a game event, or custom event.
* Can temporarily store and provide data via its output connection pins.
* May accept data inputs which arm or configure the event.
* Notably missing a input (left-side) execution (diamond) pin.

Execution Nodes

* Triggered by an execution connection via it's input execution pin.
* May also temporarily store and provide date via its output connection pins, as well as require or receive optional input data to successfully execute.
* All Execution Nodes will have an input execution pin on the left that must be connected to either an Event Node, or a string of Execution Nodes that begins with an Event Node, or the graph will fail to build.

Data Nodes

* Has no execution pins.
* Performs an operation when an execution node it is related to is triggered. Data nodes send information forward and can be combined to create complex operations to prepare data for an execution node.
* May feed into one or many execution nodes within the same event.
* Some Data Nodes have their output restricted to only working within a single chain of execution/circuit.

{% embed url="https://docs.google.com/spreadsheets/d/1nWTARlv1CZKfNVOramvxRC6u56VvK4GrqpLJZP4IPbQ/edit#gid=1000878361" %}
This document contains more than just node information, but it seemed silly to make a second document. This is also viewable in the Reference Documents folder in the Halo Infinite section.
{% endembed %}

Contributors

Captain Punch\
AgentZero

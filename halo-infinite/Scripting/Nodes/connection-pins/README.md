---
description: Connection pins connect nodes together to supply data or initiate triggers.
---

# Connection Pins

There are two types of connection pins, Execution, and Data.&#x20;

* These are represented on either side of each node by diamonds and circles.&#x20;
  * Pins on the left side are ALWAYS input.&#x20;
  * Pins on the right side are ALWAYS output.
* Execution and data ALWAYS flow left to right by virtue of pin connections.
  * The placement of the nodes relative to each other does not matter, only the connected pins.
* Diamonds will always be execution pins, and all data pins are circles.
  * Nodes that have more than one execution output, like Loops, the Branch node, etc., use circles for their execution outputs.

## Execution Pins

Execution Pins define the flow of logic within a node graph. Each node within the chain is connected sequentially using the execution pins.

* Nodes with no input Execution Pin are Event Nodes, which are the same as event listeners in other programming paradigms.
  * Event nodes can be placed and not connected to anything without causing node graph build issues in Play Mode.
* Nodes with an input Execution Pin require it to be connected for them to execute, they cannot do anything on their own.
  * Any Execution node with an input Execution pin not connected will trigger a failed node graph build in Play Mode, though other code that is not affected can still potentially run just fine.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/image (3).png" alt="" data-size="original"></td><td>Above, an event's output execution pin is connected to a node input execution pin.</td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (5).png" alt="" data-size="original"></td><td>Not all execution pins may be represented by diamonds. Due to engine limitations, some execution pins are circles instead.</td><td></td></tr></tbody></table>

## Data Pins

Data Pins allow nodes to receive and provide data of one of the Data Types available to us in Forge.

* Some Data Nodes, like Get All Players, do not have input Data Pins.
* Many Data Nodes that have input pins can have the values of those inputs set manually in the Node Properties _or_ programmatically, meaning you can set the value of the pin directly without plugging anything in to it, or you can connect a data source that could potentially give different information each time the connection is checked for data.
* Some Data Nodes, like the Identifier and Number nodes in the Variables - Basic section, only have outputs, but the value of the output must be manually set in the Node Properties.
* Data Nodes will provide fresh data each time connections to them are accessed.&#x20;
  * This means that you can use a node like Random, which provides a random number based on parameters, in each iteration of a loop and it will provide a new value each time.
  * This can be problematic in some instances, so it is important to make sure to lock data in place where necessary.&#x20;
    * This can be as simple as saving it in a variable that only updates when you want it to instead of reading it dynamically from the current game state, or passing an object or number into a custom event and using the output pins on the custom event, as they will not 'reach back' through their triggering node to get new data and will only work with what they were provided when called.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/image (3).png" alt="" data-size="original"></td><td>Above, the player is being received by the Print Player to Killfeed node from the On Player Mark Event.</td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (5).png" alt="" data-size="original"></td><td>Get All Players provides an Object List of all players currently in the game.</td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

**Contributors**\
AgentZero\
Captain Punch

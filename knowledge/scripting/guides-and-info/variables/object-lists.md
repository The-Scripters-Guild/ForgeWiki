# Object Lists

Object Lists are a powerful tool for storing and manipulating sets of object references in a node graph script. Here are some key points to keep in mind when working with Object Lists:

* Object List variables are declared using "Declare Object List Variable" with a custom Identifier. Variable declarations are automatically performed when the node graph script is run.
* Object List variables can be created for every level of scope, but are normally used at the Global and Local Scope level.
* The Initial Objects input pin accepts an Object List type variable, which can be initialized by a set of Objects. Initial Objects are not required to successfully create the variable. The Object List variable will be an empty list until a "Set Object List" node is executed.

There are two types of Object Lists:

1. **Variables Advanced (Persistent Object List):** Stores a list of Object References. Objects in list are ordered and unique, meaning adding an object a second time will have no effect.
2. **Variables Basic (Temporary Object List):** A basic Object List can be created similar to declaring an Object List Variable. A basic object list can be used to store a small amount of objects that you would like to reference in your node path. Due to the list being definitive, there is no way to alter this type of list directly in following executions.

Adding to, or removing from, an Object List Variable is easy but it is not always immediately understood by new scripters. Here's how to do it:

1. Get the current Object List by using "Get Object List Variable" with the correct Identifier and Scope.
2. Add an "Add Object to List" node, or a "Remove Object From List" node if desired. Connect the Object List output pin on the "Get Object List Variable" to the Object List input pin on the Add/Remove node.
3. After making a new list with the desired object added/removed - we will set the Object List Variable using "Set Object List Variable" with the correct Identifier and Scope.

The list stored under that variable will immediately reflect the change if retrieved later in the execution chain. The variable will continue to be stored with the values set until another Set Object List Variable node is triggered with the same Identifier and Scope.

When using Get/Set Object List variable, it gets or sets that variable at the time of execution of the node that is receiving/setting the data. If you use the same "Get Object List Variable" node for multiple execution nodes, each execution node will get the most current value for that variable, even if it was just set previously.

**Contributors**

Captain Punch\
AgentZero

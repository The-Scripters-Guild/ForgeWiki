# Variables

{% embed url="https://www.youtube.com/watch?v=vl20UefeoSc" %}
A breakdown of the Variable Nodes as of Season 2. Still a good quick start to the variable system in Halo Infinite.
{% endembed %}

## Data Types

Number: used for storing numbers.&#x20;

Boolean: used for storing true/false values.&#x20;

Object: used for storing references to specific objects.&#x20;

Object List: used for storing lists of objects in an array starting at 1.\
(this is a product of underlying LUA code)&#x20;

Weapon Type: used for storing references to weapon types.&#x20;

Grenade Type: used for storing references to grenade types.&#x20;

Equipment Type: used for storing references to equipment types.&#x20;

Vehicle Type: used for storing references to vehicles types.&#x20;

Note: non-static outputs (which includes the values from variables) cannot be used as the initial value of a variable, as all variables are declared at the same time at game start. This behavior is consistent for all variable types, including ones not described here, like Traits, which also have a Declare node (but notably lack a Set or Get node as they cannot be updated during play).

## Scopes

Local Scope: you can use this variable only in the script brain where you created it.&#x20;

Global Scope: you can use this variable in any script.&#x20;

Object Scope: your variable will be affiliated with a specific object and each dynamic object on the level will have it's own copy of the variable that can have differing variables. Object scoped variables require an Object Reference from some source to know which object's copy you are trying to interact with.

## How to declare a variable

1. Spawn a script brain and open the node browser.
2. Navigate to "Variables Advanced" and select "Declare \[type] Variable" for the type of variable you want to use.
3. Once you've created your variable declaration, you'll need to give it a unique identifier and a scope.

* Some data types will also require a default value to be set\*.
* Object scoped variable declarations create a copy of that variable per dynamic object on the level and define the default value for that variable for all objects.

## How to get the value of a variable

1. Navigate to "Variables Advanced" and select "Get \[type] Variable" for the type of variable you want to use.
2. Give it the relevant identifier and scope.
3. If it's an object scoped variable, make sure to connect the relevant object reference to the Object input pin, otherwise do not use that pin.

## How to set (change) the value of a variable

1. Navigate to "Variables Advanced" and select "Set \[type] Variable" for the type of variable you want to use.
2. Give it the relevant identifier and scope.
3. If it's an object scoped variable, make sure to connect the relevant object reference to the Object input pin, otherwise do not use that pin.
4. Set the value that the variable should be updated to either directly on the node or by connecting a relevant input to the Value pin.

\*Vector3 Variable Declarations require default values to be set and cannot be left null

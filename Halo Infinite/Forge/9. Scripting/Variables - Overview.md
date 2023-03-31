# Variables

## Datatypes
Number: used for storing numbers.
Boolean: used for storing true/false values.
Object: used for storing references to specific objects.
Object List: used for storing lists of objects in an array starting at 1 (LUA).
Weapon Type: used for storing references to weapon types.
Grenade Type: used for storing references to grenade types.
Equipment Type: used for storing references to equipment types.
Vehicle Type: used for storing references to  vehicles types.
Note that you can't use the value of another variable as the initial value, as all variables are declared at the same time at game start.

## Scopes
Local Scope: you can use this variable only in the script brain where you created it.
Global Scope: you can use this variable in any script.
Object Scope: your variable will be affiliated with a specific object, with each object having a different copy of, and possibly/likely a different value for, the variable that can be accessed in relation to that object's reference.

## How to declare a variable
1. Spawn a script brain and open the node browser.
2. Navigate to "Variables Advanced" and select "Declare [type] Variable" for the type of variable you want to use.
3. Once you've created your variable declaration, you'll need to give it a unique identifier and a scope. 
 - Some data types will also require a default value to be set*.
 - Object scoped variable declarations create a copy of that variable per dynamic object on the level and define the default value for that variable for all objects.

## How to get the value of a variable
1. Navigate to "Variables Advanced" and select "Get [type] Variable" for the type of variable you want to use.
2. Give it the relevant identifier and scope. 
3. If it's an object scoped variable, make sure to connect the relevant object reference to the Object input pin, otherwise do not use that pin.

## How to set (change) the value of a variable
1. Navigate to "Variables Advanced" and select "Set [type] Variable" for the type of variable you want to use.
2. Give it the relevant identifier and scope. 
3. If it's an object scoped variable, make sure to connect the relevant object reference to the Object input pin, otherwise do not use that pin.
4. Set the value that the variable should be updated to either directly on the node or by connecting a relevant input to the Value pin.

*Vector3 Variable Declarations require default values to be set and cannot be left null
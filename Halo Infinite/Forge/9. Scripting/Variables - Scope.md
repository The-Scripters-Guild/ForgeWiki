# Understanding Scopes in Scripting
In any programming environement, it is important to undestand the concept of scope and what scopes that variables can have. Scopes determine the level at which a variable of a specific identifier and type is stored. In Infinite, those scopes are Global, Local, and Object.

## Global Scope
A Global scope variable exists at the map level and is accessible via its identifier by any Script Brain on the level via Get Type Variable. They can be modified by any brain in the level via Set Type Variable. Global variables store a single instance of that variable type (Number, Boolean, Object, Object List, etc.)

## Local Scope
A Local Scope variable is similar to a global variable, except Local Scope variables only exists within the brain it was declared. Local scope is the easiest way to store a bucket of data, such as settings for a script, and can be used to store Object Lists like any other variable type.

## Object Scope
An Object Scope is a variable that is stored by an Object. Declaring an Object Scope variable creates an instance of that variable within every object in the level. Object Scope variables cannot be accessed at the Local or Global level and can only be accessed by passing the object which the variable exists to the Get/Set Type Variable node's Object input pin.

Object Scope variables take an initial value, which all objects created on the level will have by default. If this value is left empty, there is no way to define an initial value except by altering that variable's declaration.

Object Scope variables can be used to store variables per object. For example, a declared number variable can store the number of player deaths, and it can be tracked for each object that exists in the game.

## Usage
Global scope should be used for anything that needs to be accessed by all scripts, including scripts created by other brains/players. Local scope is recommended to store script settings and other script-specific data. Object scope is best used to store variables per object, like the number of player deaths.

It's important for Global variables to be unique to avoid conflicts with other scripts that may declare the same variable. All variables, regardless of scope, can only be declared once, and its initial value is read when the node is instanced at game start. Changing the variable's value will not change its initial value.

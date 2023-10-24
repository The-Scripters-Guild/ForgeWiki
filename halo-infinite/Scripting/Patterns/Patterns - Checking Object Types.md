# Pattern - Checking Object Types

This concept applies for weapons, vehicles, and equipment, but the example below describes it as if you were checking if something is a vehicle. 

To determine if an object is a vehicle in Forge, you can use the "Are Same Vehicle Type" node. There is currently no direct node to test if an object is a vehicle, just for checking against *types* of vehicles.

Here's how to do it:

1. Choose the object you want to check.
2. Choose a static reference to an object that you know is not a vehicle, such as the script brain.
3. Connect references to both of these objects to an "Are Same Vehicle Type" node.
4. If the object is not a vehicle, the "Are Same Vehicle Type" output pin will return true. If it is a vehicle, it will return false. Be careful as this can seem backwards.

#### Contributors
Captain Punch
DeceitfulEcho

# Creating a Spherical Boundary

## Creating a Spherical Boundary

Creating a spherical boundary in game development can be an effective way to control player movement within a specific area. This technique can work whether the player character is on foot or in a vehicle.

### Basic Concept

Start by subtracting the coordinates of the center of the boundary vector from the coordinates of the player's location; you would use `Get Object Location` and `Subtract Vectors` to get the needed data. Then you would use a `Get Vector Length` node to get the distance between these two points, followed by comparing that length against the sphere's radius to determine if the player is inside it or not and using the boolean output with a `Branch` node to change the flow of execution.

### Code Example

Here is an example of some pseudocode that accomplishes this goal. In this case, `VectorLength` is the result of the `Get Vector Length` operation, and `SphereRadius` is the radius of your spherical boundary. If `VectorLength` is greater than `SphereRadius`, the player is outside the boundary.

```
# Pseudocode
BoundaryCenter = GetBoundaryCenter()
PlayerPosition = GetPlayerPosition()

VectorLength = GetVectorLength(PlayerPosition - BoundaryCenter)

if (VectorLength > SphereRadius) {
    // Player is outside the boundary
}
```

Here's an example of how you might implement this in a node graph. You'll need to adjust `Operand B` to control the size of the boundary, and adjust the `Timer Delay` to control how often the boundary check runs.

https://media.discordapp.net/attachments/1041350507568042135/1041350507672907919/414991d1-60fd-463f-b1fe-c52b311b603a.png?width=718\&height=404

### Optimization

An optimization trick can be applied here to avoid the costly square root calculation in the Get Vector Length operation. Instead of using Get Vector Length, you can use a Dot Product operation with the output of the Subtract Vectors operation fed into both inputs. This changes the calculation from √(x² + y² + z²) to x² + y² + z².

Remember, if you use this optimization, the distance in COMPARE: Operand B also needs to be squared.

````
# Pseudocode with optimization
BoundaryCenter = GetBoundaryCenter()
PlayerPosition = GetPlayerPosition()

VectorDifference = PlayerPosition - BoundaryCenter
SquaredDistance = DotProduct(VectorDifference, VectorDifference)

if (SquaredDistance > SphereRadius^2) {
    // Player is outside the boundary
}
```

#### Contributors
Captain Punch
TheProgrammer165
ShambullZ
````

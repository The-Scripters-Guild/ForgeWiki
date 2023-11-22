# Spawning Players in Vehicles

This wiki entry explains how to make players spawn in vehicles and manage spawned vehicles efficiently.

**Warning**: Use with care. Too many vehicles on the map can severely affect network performance.

Use the "Set Spawn In Vehicle For Player" node to enable or disable spawning a player in a specific type of vehicle. 

To apply this from the game/round start without having players have their initial spawns on foot:

1. Block spawns
2. Apply the trait
3. Unblock spawns

**Note**: Ensure that on first spawn, if spawning in a Wasp, the player is forced to exit and re-enter the vehicle.*

\* *This is because there is a bug with spawning in Wasps for first spawn. Players will be standing on top of the Wasp instead of being properly seated in the vehicle.* 

## Vehicle Management

### Registering Vehicles with Players

1. When a player spawns, register their vehicle in an object scoped variable scoped to each player and in an object list for tracking active vehicles.
2. When players enter vehicles, register the vehicle as their vehicle by saving it in the object scoped variable and adding it to the active vehicles list.

### Cleaning Up Vehicles

1. On vehicle exit, set a wait of X seconds (where X is the desired cleanup delay).
2. If the vehicle is unoccupied after the wait and not registered to a player, remove it from the active vehicles list and clean up the vehicle.

You can also check the count of active vehicles and only perform cleanup if it's above a certain threshold.

### Vehicle Cleanup Methods

1. Set the position of the vehicle to 0, 0, -1000 to destroy it quietly.
2. Use "Delete Object" to make the vehicle explode.
3. Get its current health and damage it just enough to make it go red for an animated deletion.

#### Contributors
Captain Punch
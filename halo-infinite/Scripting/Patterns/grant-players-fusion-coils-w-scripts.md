# Sending Fusion Coils Directly to Player's Hands

In Halo Infinite's Forge Mode, mode designers may want to be able to send Fusion Coils directly to a player's hands. Since Kong Slayer doesn't give control over when player has a coil it is not a viable base mode to provide this functionality. 

This method relies on the following fact of Halo's engine:
All carryables are weapons. Fusion coils are carryable.

To send a Fusion Coil directly to a player's hands, you can detect the weapon type of a fusion coil and use that to send one to the player's primary weapon slot. To do this, you can put a coil somewhere out of boundary (outside of the level), get an object reference to it, and you can spawn new ones in players hands with that reference using normal weapon-granting nodes, such as `Give Player New Weapon`.

#### Contributors
Captain Punch
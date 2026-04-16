# Colored Boundaries

To create colored boundaries in Infinite one can use certain objects with unique properties that can be manipulated to achieve the desired effect. One such method is by lighting up the hill volumes for some of the game's normally invisible objects, allowing you to turn the visuals for the hills on and off by manipulating those objects.

The items that can be used for this method include:

* Named Location Volumes (Yellow)
* Soft Safe Volumes (Light Green)
* Safe Volumes (Green)
* Respawn Volumes (Blue)
* Soft Kill Volumes (Red)
* Kill Volumes (Light Orange)
* Damage Emitter (Bold Orange)

All of these items can be seen, moved, and spawned/despawned. However, after moving one of these zones, it creates and leaves a "ghost object" in its original spawn location that cannot be affected in any way. Despawning/spawning objects before moving them does not change the outcome of this fact.

Both Kill Volumes will still kill the player, but it is easy to avoid the Soft Kill adverse affects by making it 0.5 thin and not at ground level. To prevent kill zone issues completely, simply put a safe zone around it.

The soft variants of the kill and safe volumes have a different shade.

For more specific effects, different objects can be used. The Attrition Dodgeball Overtime Zone and Stronghold Capture Zone can be used for a pulsing transparent white, while a Hacking Terminal can be used for a very transparent white with a solid white ring on ground level. Fusion coils can be used for a solid transparent white and can also be interacted with, so the boundaries move with them. Note that fusion coils and strongholds have a permanent up direction to their boundary animation.

**Contributors**\
Captain Punch\
Nokyard\
Hitbox Unknown

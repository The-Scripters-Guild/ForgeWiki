# AI Spawners

AI Spawners are used to spawn campaign AI units. In order for the AI units to spawn, the boundary of the object must intersect a nav mesh. Depending on the type of AI Spawner being used, one to many campaign AI Units can be spawned at a time via droppod, Phantom, or in-place.

### Squads

AI units produced by spawners are logically and behaviorally grouped together by the engine into collections known as squads. From within the spawn logic of the spawner, a squad label can be set. 
All units produced by the spawner are tagged by the set label, allowing Forgers to reference squads of AI units from within a script brain without requiring a direct reference to the squad or spawner object.

Once a squad is spawned, the individual units making up the squad can be scripted in a script or mode brain to later join a different squad by changing its squad label.
Multiple spawners can produce AI Units for the same squad. Because squad labels are limited to the military phonetic alphabet, this means that Forge supports the creation and manipulation of 26 unique squads.
However, the engine supports a maximum of 32 campaign AI units in a match so reaching the limit of 26 squads is an edge case and should be rare.

### Unique Properties

As with all Forge objects, AI Spawners can be configured to suit different needs for a map via unique properties in the Object Properties menu.

#### Unit Selection

Campaign AI unit can be selected for spawning via the unit selection menu. Unit type and weapon type can be configured here, with the weapon type being dependent on the species of the unit.
For example, Grunts can only use pistols, while Jackals can use pistols and shouldered weapons, like the M392 Bandit and Cindershot. Only base weapon types can be selected in the dropdown menu.

#### Spawn Logic

These properties dictate the parameters of how AI units spawned via the spawner enter the map. This includes the Triggered by Script toggle which allows you to control when AI are placed in the map via a script or mode brain.

#### Squad Behaviors

The available spawner objects let you configure set behavior traits to apply to the AI spawned from the spawner. These include toggling senses, idle behavior, and even disabling behaviors all together.

#### AI Zone

AI move zones are used to configure a path of movement. To direct AI units to move to a predetermined location outside the spawner, a move zone places on the map can be selected. 
Setting the AI move zone to a zone a part of a chain of move zones will cause spawned AI units to move to each zone in the chain.

### Spawner Types

There are three Forge objects used to mark the spawn location of campaign AI. Each one differs in how it delivers the AI units to their spawn locations. If the spawner boundry fails 
to intersect the nav mesh, a message will be displayed in the feed to inform the player.

#### Droppod

The droppod spawner will produce a single AI unit at a time via a droppod from the sky. Once the AI unit has exited the pod, 
it will overload and destroy itself. If an object obstructs the entry path of the droppod, it will phase through it and deliver
the AI unit to where it intersects with the nav mesh.

#### Phantom

The Phantom spawner will deploy a squad of AI Units from a Phantom dropship. Also configurable are whether the phantom is 
equipped with weapons and vehicles. As the Phantom travels to the spawn location, it can be damaged and destroyed, 
preventing the AI units from entering gameplay.

Objects obstructing the Phantom drop off location or path can interfere with the spawn process so it is important to 
verify that the dropship can reach its destination as expected.

#### Spawner

The spawner will produce a squad of AI units in place. This is comparable to the spawning of a player in how the units are 
produced. 

If the volume of the object is obstructed, the configured squad is at risk of spawning inside obstructing objects.

#### Vehicle Spawner

A variation of the spawner, this object allows players to configure vehicles driven by AI units. The species of the unit is 
dependent on what type of vehicle is selected. If no unit is configured to drive a vehicle, the vehicle will spawn driverless.

If the the volume of the object is obstructed, the configured vehicles are at risk of spawning inside of obstructing objects.

### Scripting

AI spawners are scriptable from within a script or mode brain. Multiple nodes exist that take in AI spawners as a parameter.


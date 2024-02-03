# AI Spawners

AI Spawners are used to spawn campaign AI units. In order for the AI units to spawn, the boundary of the object must intersect a nav mesh. Depending on the type of AI Spawner being used, one to many campaign AI Units can be spawned at a time via droppod, Phantom, or in-place.

### Squads

AI units produced by spawners are logically and behaviorally grouped together by the engine into collections known as squads. From within the spawn logic of the spawner, a squad label can be set. 
All units produced by the spawner are tagged by the set label, allowing Forgers to reference squads of AI units from within a script brain without requiring a direct reference to the squad or spawner object.

### Unique Properties

As with all Forge objects, AI Spawners can be configured to suit different needs for a map via unique properties in the Object Properties menu.

#### Unit Selection

A campaign AI unit can be selected for spawning via the unit selection menu. Unit type and weapon type can be configured here, with the weapon type being dependent on the species of the unit.
For example, Grunts can only use pistols, while Jackals can use pistols and shouldered weapons, like the M392 Bandit and Cindershot. Only base weapon types can be selected in the dropdown menu.

#### Spawn Logic

These properties dictate the parameters of how AI units spawned via the spawner enter the map. This includes the Triggered by Script toggle which allows you to control when AI are placed in the map via a script or mode brain.

#### Squad Behaviors

The available spawner objects let you configure set behavior traits to apply to the AI spawned from the spawner. These include toggling senses, idle behavior, and even disabling behaviors all together.

#### AI Zone

AI move zones are used to configure a path of movement. To direct AI units to move to a predetermined location outside the spawner, a move zone places on the map can be selected. 
Setting the AI move zone to a zone a part of a chain of move zones will cause spawned AI units to move to each zone in the chain.

### Spawner Types

There are three Forge objects used to mark the spawn location of campaign AI. Each one differs in how it delivers the AI units to their spawn locations.
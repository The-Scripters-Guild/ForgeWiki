# AI Spawner

Spawns AI units. The object boundary must intersect the nav mesh, to see the Nav Mesh data
toggle the *Nav Mesh Visualization* to ON in the **Tool Settings** menu. Up to 32 AI units and 4 Phantoms can exist at a 
time, but runtime budgets may decrease this limit.

# Remarks

This is comparable to the spawning of a player in how the units are produced.

## Object Properties

### Unit 1 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 2 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 3 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 4 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 5 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 6 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 7 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Unit 8 Selection
| Property | Description                                              |
|----------|----------------------------------------------------------|
| Unit     | The AI unit to spawn in this slot.                       |
| Weapon   | The weapon that will be used by the AI unit in this slot.|

### Spawn Logic
| Property            | Description                                                                                                                                      |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Face Forwards       | If enabled, the spawned AI units will face the same direction as the spawner object.                                                             |
| Triggered by Script | If enabled, the spawner will not automatically spawn AI units and will instead wait for a script call to activate it.                            |
| Initial Spawn Delay | The number of seconds into the round before the AI units spawn. Set to 0 to cause the units to spawn immediately.                                |
| Squad Label		  | The Squad Label used by the spawned AI units. Each spawner will spawn AI units as a squad and nodegraph can use these labels to identify squads. |

### Squad Behaviors
| Property         | Description                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------|
| Set Deaf         | If enabled, the spawned AI units will not perceive audio cues such as gunfire.                              |
| Set Blind        | If enabled, the spawned AI units will not perceive visual cues such as the player walking in front of them. |
| Set Inactive     | If enabled, the spawned AI units will not make any behavior decisions or be active.                         |
| Set Magic Sight  | If enabled, the spawned AI units will be able to see enemies through walls and terrain.                     |
| Wander When Idle | If enabled, the units spawned from the spawner will wander around their assigned zone while idle.           |

### AI Zone
| Property     | Description                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AI Move Zone | The AI Move Zone that the spawner's AI units will be assigned to. Linking a zone will allow the spawner's AI units to move and fight outside the vicinity of the spawner. To cancel a link, select this AI spawner from the list of options. |

**Contributors**

Mr. Admirals
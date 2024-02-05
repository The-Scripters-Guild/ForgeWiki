# AI Vehicle Spawner

Spawns AI units inside of vehicles. 32 AI units maximum; impacts vehicle and runtime budgets. 
Must be touching nav mesh to function.

## Remarks

The species of the unit is dependent on what type of vehicle is selected. If no unit is 
configured to drive a vehicle, the vehicle will spawn driverless.

## Object Properties

### Vehicle 1 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 2 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 3 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 4 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 5 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 6 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 7 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Vehicle 8 Selection 
| Property | Description                                                  |
|----------|--------------------------------------------------------------|
| Vehicle  | The vehicle that will be driven by the AI unit in this slot. |
| Unit     | The AI Unit that will spawn in this slot.                    |

### Squad Behaviors
| Property         | Description                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------|
| Set Deaf         | If enabled, the spawned AI units will not perceive audio cues such as gunfire.                              |
| Set Blind        | If enabled, the spawned AI units will not perceive visual cues such as the player walking in front of them. |
| Set Inactive     | If enabled, the spawned AI units will not make any behavior decisions or be active.                         |
| Set Magic Sight  | If enabled, the spawned AI units will be able to see enemies through walls and terrain.                     |
| Wander When Idle | If enabled, the units spawned from the spawner will wander around their assigned zone while idle.           |

### Spawn Logic
| Property            | Description                                                                                                                                      |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Triggered by Script | If enabled, the spawner will not automatically spawn AI units and will instead wait for a script call to activate it.                            |
| Initial Spawn Delay | The number of seconds into the round before the AI units spawn. Set to 0 to cause the units to spawn immediately.                                |
| Squad Label		  | The Squad Label used by the spawned AI units. Each spawner will spawn AI units as a squad and nodegraph can use these labels to identify squads. |

### AI Zone
| Property     | Description                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AI Move Zone | The AI Move Zone that the spawner's AI units will be assigned to. Linking a zone will allow the spawner's AI units to move and fight outside the vicinity of the spawner. To cancel a link, select this AI spawner from the list of options. |
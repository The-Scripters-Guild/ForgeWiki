# AI Spawning

Campaign AI units are placed in a map using AI Spawners. In order for the AI units to spawn, the boundary of the object must intersect a nav mesh. 
Depending on the type of AI Spawner being used, one to many campaign AI Units can be spawned at a time via droppod, Phantom, or in-place. A
maximum of 32 AI units can be spawned at a time.

## Scripting

AI Spawners and AI Vehicle Spawners are designed to be initialized to spawn AI units at a single location. Once the first squad has spawned,
these two AI Spawners will only be able to spawn AI units at the original location, even if the object itself has been moved in a script. In
order to spawn AI units at different locations, the spawner must be deleted, spawned, positioned and initailized again via script before
being used.

To perform the initialization, a _Wait For N Seconds_ node can be used with its parameter set to 0 seconds. This one frame delay will allow the
engine to properly initialize the AI Spawner in its new position before it is used.

## Nodegraph Reference

{% content-ref url="halo-infinite\scripting\nodes\node-data\specific-nodes\ai\get-squad-definition-from-ai-spawner.md" %}
[get-squad-definition-from-ai-spawner.md](halo-infinite\scripting\nodes\node-data\specific-nodes\ai\get-squad-definition-from-ai-spawner.md)
{% endcontent-ref %}
{% content-ref url="halo-infinite\scripting\nodes\node-data\specific-nodes\ai\trigger-ai-spawner.md" %}
[get-squad-definition-from-ai-spawner.md](halo-infinite\scripting\nodes\node-data\specific-nodes\ai\trigger-ai-spawner.md)
{% endcontent-ref %}
{% content-ref url="halo-infinite\scripting\nodes\node-data\specific-nodes\ai-advanced\get-all-ai-spawners.md" %}
[get-squad-definition-from-ai-spawner.md](halo-infinite\scripting\nodes\node-data\specific-nodes\ai-advanced\get-all-ai-spawners.md)
{% endcontent-ref %}
{% content-ref url="halo-infinite\scripting\nodes\node-data\specific-nodes\ai-advanced\get-squads-from-spawner.md" %}
[get-squad-definition-from-ai-spawner.md](halo-infinite\scripting\nodes\node-data\specific-nodes\ai-advanced\get-squads-from-spawner.md)
{% endcontent-ref %}
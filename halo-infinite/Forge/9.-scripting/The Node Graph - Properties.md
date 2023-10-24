# Nodegraph Properties
- The per-Script-Brain node limit is 128 nodes, but can be less depending on how many entities you have present in that graph, as each node contributes differently and each pin with data set and each connection are also considered entities.
- Deleting objects doesn't immediately refund the budget because that object is still in the undo stack. The best way to truly refresh your budget is to save your map, leave the Forge session, and then load into the map again in Forge.
- There is no intended "invisible" limit on script brains -- the only limit we have is 128 nodes per script brain.
- A script that has been deleted might still run after deletion, its nodegraph can't be accessed, and persists across saves/sessions. This is known as a "ghost brain".

## Notable Updates
Season 3 added a budget check whenever a player added nodegraph content in order to reduce the incidence of “Dedicated Server Failed to Load” errors.

- If your map has too many “nodegraph entities” (nodes + connections + properties), this check will prevent you from adding nodes, duplicating nodes, or adding more connections.
- This resulted in a functional global budget of about 200-250 nodes per map after the Season 3 update, which is a pretty low ceiling.
- A hotfix raised the Nodegraph Entity limit from 800 to 2048.
- Most players should now be able to add nodes and connections to any map that was functioning during the Winter Update.
- Maps should be able to comfortably hold scripts with up to 512 nodes before running into the duplication limit or the “Dedicated Server Failed to Load” bug.

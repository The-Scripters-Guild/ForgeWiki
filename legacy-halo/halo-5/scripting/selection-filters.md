# Selection Filters

#### What Are Selection Filtering Mods?

In Halo 5 Scripting, selection filtering mods are used in Action settings found in Mod Lists. Selection filtering mods "add in" and "filter out" which **Objects**, **Targets**, **Players**, and **Elements** affect whether or not that Action runs, as well as which **Objects**, **Targets**, **Players**, and **Elements** that Action will affect. Action filtering mods are sometimes hidden and must be accessed by clicking OBJECTS, TARGETS, or NUMBERS, or they will sometimes appear after selecting other settings in Actions. (See [Actions](https://www.forgehub.com/wiki/h5-actions/) page for specific settings).&#x20;

Examples of script Actions that affect Objects, Targets, and Players include movement, move towards target, player traits, and scoring scripts. Below is a list of all Mods and their descriptions. When selecting mods, you will first have the option to choose between the first twelve listed below. Once you choose one of these, the other options will be available. Team and Label mods have an additional sub-menu.

### Mods Definitions

**SPECIAL MODS** There are some mods that refer to objects/players that vary based on the circumstance. ACTIVATOR and EXTRA are defined by the Script's Condition. Only some Conditions do this, and ACTIVATOR and/or EXTRA show up within all the script's Actions when these are chosen.

* **THIS** refers to the object containing the script
* **ACTIVATOR** usually the object or player that triggers, or "activates" the Condition
* **EXTRA** usually players or objects identified in the Condition (see mod definitions for more information)

**GENERAL TYPES OF MODS** To build a list of objects/players to select for an Action to work on, use the add mod type to increase the size of the list and then use the filtering mod types to remove some to refine the list of objects/players to be selected.

* **\[add]** is the only mod type that can add players and objects to the initially empty list and later can add more "in addition to" those already defined.
* **\[exclude]** removes only the players and objects with property values that match the type and sometimes the specified value for the chosen mod.
* **\[include]** removes any players and objects that do not match the type and values specified by the mod, leaving only those that match. \[include] mods remove the widest range of players and objects out of the general mod types.

### Diving Deeper into Selection Mods

**\[add] Mod**

The \[add] mods are the only ones to add Objects and Players to the list "in addition to". \[include], \[exclude], and \[remove] all remove items (see definitions below).

**ACTIVATOR and EXTRA Mods**

In mod filtering, ACTIVATOR is determined by the Object or Player that was chosen in that Action's Condition settings.

* The Condition Message:Received gets its ACTIVATOR from the Message:Send Action that sends the message, either sharing its ACTIVATOR, or using the Message:Send script object if set to THIS.
* Similarly, Power Check: ACTIVATOR is passed to the script by the Power Set action that triggers this condition.
* Interacted: ACTIVATOR is the player that interacted with the switch, powerup, etc.
* Boundary Check: ACTIVATOR is the objects and players that just crossed the boundary and meet the condition.
* For Message Received and Power Check only the last action to call Message Send or Power Set will be able to pass its object or player to the condition. Boundary Check can pass multiple objects to ACTIVATOR.
* Objects/Players returned by EXTRA depend on which condition the script has.
* When using Boundary:Check set to Continuous, use EXTRA for both players and objects.
* Number Check: EXTRA returns the objects or players whose number changed. Objects numbers can only be checked by scripts in the object itself. Players whose specified number channel was changed are all returned in a group by EXTRA.

**Select First/Select Last Mods**

* First/Last change if objects are off the map at the same time and then spawned into the map. First is the 1st one to spawn on the map.
* Likely an array is used and it's filled back in with lowest open position 1st whenever objects spawn.
* That means despawning/spawning 1 object just puts it back where it left.
* So 2 objects can be despawned (they don't have to leave the map at the same time, just both off the map for any time together) and the 1st one spawned in will be chosen by Select First before the other.
* Players can switch First/Last order with objects, but there might be more to it.
* Forge monitor mode doesn't seem to switch it, but dying does.
* Objects spawned at the same time (like the beginning of a game or round) probably get added with a process that works the same way each time, but it might be much safer to use some Despawn/Spawn scripts and the Despawn/Respawn object settings to set them up reliably at the start of each round (Spawned) before play begins (Round Event: Start).

### Mods Gotchas

**Despawned Objects**

We can't use filtering mods to select destroyed or despawned objects or players. For example, if attempting to use the target filtering mods OBJECTS=THIS \[add], Group Siblings \[add], because the object is not found on the map, THIS \[add] returns nothing and then no siblings can be added. You can work around this by temporarily spawning the object using the Condition when Destroyed/Despawned, then using Action Spawn (Force=ON), then the Action Despawn with your mod filters OBJECTS=THIS \[add], Group Siblings \[add].

The same is true for boundary mods such as Boundary:THIS\[include]. If the object with the boundary is despawned, any mods pertaining to boundary are disregarded, since no boundary exists.

**Labels**

Any object that either has a label entered into its properties or a script exists either directly or remotely that will change its label will physically shift on one rotation axis (predefined by the piece) upon spawning in Xbox customs. This also happens any time you place any script directly on a piece (in its properties). This doesn't happen in Forge on the Xbox, and doesn't happen on the pc at all.

Unfortunately, Label mods are needed to script physical changes to the piece such as Move:Offset, Color Change, and Despawn, perhaps non-physical too.

**\[Add] Mod Gotchas**

Adding a respawn time in an object's properties appears to fix the Grouped-Object\[add] glitch, so it's possible that it might be a workaround for these others.

* **Boundary This\[Add]** - does not perform the assigned task to objects contained within and sometimes selects objects from outside the boundary. A fix is to use Number Change or Spawn Order Change to change the number of objects that enter a boundary, then use Number Check to trigger your desired Actions.
* **Team This\[Add]** - Similarly to Boundaries, this appears to be something that should work, yet doesn't. If you want a script-scheme to work with everything, you want the team of the object holding the script to be Neutral. But, no team value allows this to work.
* **Grouped-Object (Parent w/ Label) \[Add]** - Weirdly enough, this STILL doesn't work! You can see it in forge, perfect. Go to customs, and you'll never see a piece despawn etc. There is no combination of Sibling, Parent Exclude, or anything else that will make it work. As stated above, it does work in forge, so the selection methodology may seem correct, yet it just doesn't work in customs. Again, adding a respawn time in an object's properties appears to fix this glitch.

### Complete Mods List with Descriptions

_Mods with an asterisk are the only ones available for the first slot in the mods list._

* **THIS \[add]**: Appends the THIS object to the list.
* **ACTIVATOR \[add]**: Appends the ACTIVATOR object to the list.
* **EXTRA \[add]**: Appends EXTRA objects to the list identified by the Condition.
* **Players \[add]**: Appends all players (living and dead) to the list.
* **Team \[add]**: Appends all the objects on an explicit team to the list.
* **Team:THIS \[add]**: Appends all the objects on THIS object's team to the list.
* **Team:ACTIVATOR \[add]**: Appends all the objects on the ACTIVATOR object's team to the list.
* **Label \[add]**: Appends all the objects with label to the list.
* **Label:THIS \[add]**: Appends all the objects sharing a label with THIS object to the list.
* **Label:ACTIVATOR \[add]**: Appends all the objects sharing a label with the ACTIVATOR object to the list.
* **Boundary:THIS \[add]**: Appends all the objects in THIS object's boundary to the list.
* **Boundary:ACTIVATOR \[add]**: Appends all the objects in ACTIVATOR object's boundary to the list.
* **THIS \[remove]**: Removes the THIS object from the list.
* **ACTIVATOR \[remove]**: Removes the ACTIVATOR object from the list.
* **EXTRA \[remove]**: Removes the EXTRA objects from the list.
* **Objects \[include]**: Removes all objects from the list that are players.
* **Objects \[exclude]**: Removes all objects from the list that aren't players.
* **Players \[include]**: Removes all objects that aren't players from the list.
* **Players \[exclude]**: Removes all players from the list.
* **Dead \[include]**: Removes objects from the list that are not dead. Non-health-based objects (blocks, etc.) are removed.
* **Dead \[exclude]**: Removes objects from the list that are dead. Non-health-based objects (blocks, etc.) are removed.
* **Groups \[include]**: Removes objects from the list that are not in groups.
* **Groups \[exclude]**: Removes objects from the list that are in groups.
* **Group: Parents \[add]**: For each grouped object in the list, add its parent to the list.
* **Group: Parents \[exclude]**: Removes the objects from the list that are group parents.
* **Group:Siblings \[add]**: For each grouped object in the list, add all the children in its group to the list.
* **Group:Siblings \[exclude]**: Remove objects from the list that are group children.
* **Team \[include]**: Remove objects from the list that aren't on the explicit team.
* **Team \[exclude]**: Remove objects from the list that are on the explicit team.
* **Team:THIS \[include]**: Remove objects from the list that aren't on THIS object's team.
* **Team:THIS \[exclude]**: Remove objects from the list that are on THIS object's team.
* **Team:ACTIVATOR \[include]**: Remove objects from the list that aren't on the ACTIVATOR object's team.
* **Team:ACTIVATOR \[exclude]**: Remove objects from the list that are on the ACTIVATOR object's team.
* **Boundary:THIS \[include]**: Remove all objects from the list that aren't in THIS object's boundary.
* **Boundary:THIS \[exclude]**: Remove all objects from the list that are in THIS object's boundary.
* **Boundary:ACTIVATOR \[include]**: Remove all objects from the list that aren't in the ACTIVATOR object's boundary.
* **Boundary:ACTIVATOR \[exclude]**: Remove all objects from the list that are in the ACTIVATOR object's boundary.
* **Label \[include]**: Remove all objects from the list that don't share the explicit label.
* **Label \[exclude]**: Remove all objects from the list that share the explicit label.
* **Label:THIS \[include]**: Remove all objects from the list that don't share a label with THIS object.
* **Label:THIS \[exclude]**: Remove all objects from the list that share a label with THIS object.
* **Label:ACTIVATOR \[include]**: Remove all objects from the list that don't share a label with the ACTIVATOR object.
* **Label:ACTIVATOR \[exclude]**: Remove all objects from the list that share a label with the ACTIVATOR object.
* **Number \[include]**: Remove all objects from the list that don't match the explicit Number.
* **Number \[exclude]**: Remove all objects from the list that match the explicit Number.
* **Number:THIS \[include]**: Remove all objects from the list with a Number that doesn't match the Number of THIS object.
* **Number:THIS \[exclude]**: Remove all objects from the list with a Number that matches the Number of THIS object.
* **Number:ACTIVATOR \[include]**: Remove all objects from the list with a Number that doesn't match the Number of the ACTIVATOR objects.
* **Number:ACTIVATOR \[exclude]**: Remove all objects from the list with a Number that matches the Number of the ACTIVATOR objects.
* **Order \[include]**: Remove all objects from the list that don't match the explicit Spawn Order.
* **Order \[exclude]**: Remove all objects from the list that match the explicit Spawn Order.
* **Order:THIS \[include]**: Remove all objects from the list with a Spawn Order that doesn't match THIS object.
* **Order:THIS \[exclude]**: Remove all objects from the list with a Spawn Order that matches THIS object.
* **Order:THIS Number \[include]**: Removes all objects from the list with a Spawn Order that doesn't match THIS object's Number Value.
* **Order:THIS Number \[exclude]**: Removes all objects from the list with a Spawn Order that matches THIS object's Number Value.
* **Order:ACTIVATOR \[include]**: Remove all objects from the list with a Spawn Order that doesn't match the ACTIVATOR objects.
* **Order:ACTIVATOR \[exclude]** Remove all objects from the list with a Spawn Order that matches the ACTIVATOR objects.
* **Order:ACTIVATOR:Number \[include]** Remove all objects from the list with a Spawn Order that doesn't match the ACTIVATOR objects Number Value.
* **Order:ACTIVATOR:Number \[exclude]** Remove all objects from the list with a Spawn Order that matches the ACTIVATOR objects Number value.
* **Select First** Removes all but the first X \[specified by Count] objects from the list.
* **Select Last** Removes all but the last X \[specified by Count] objects from the list.
* **Select Random** Removes all but random X \[specified by Count] objects from the list.
* **Select Nearest** Removes all but the X \[specified by Count] objects from the list nearest to THIS object.
* **Select Farthest** Removes all but the X \[specified by Count] objects from the list farthest from THIS object.
* **\[NOTHING]** When used as the first modifier, generates an empty list. Otherwise, does nothing.

## Complete Labels Sub-Menu List

This is a complete list of the labels available when filtering using any of the Labels mods.

* slayer: include
* slayer: exclude
* slayer: standard: include
* slayer: free-for-all: include
* slayer: multi-team: include
* slayer: doubles: include
* ctf: include
* ctf: exclude
* ctf: flag: spawn & return
* ctf: standard: include
* ctf: neutral-flag: include
* ctf: object
* strongholds: include
* strongholds: exclude
* strongholds: base
* strongholds: standard: include
* strongholds: one-base: include
* breakout: include
* breakout: exclude
* sportsball: spawn
* sportsball: return
* sportsball: include
* sportsball: exclude
* sportsball: object
* infected: include
* infected: exclude
* minigame: include
* minigame: exclude
* minigame:1: object
* minigame:2: object
* minigame:3: object
* minigame:4: object
* minigame:5: object
* forge: include
* user: alpha
* user: barvo
* user: charlie
* user: delta
* user: echo
* user: foxtrot
* user: golf
* user: hotel
* user: india
* user: juliet
* user: kilo
* user: lima
* user: mike
* user: november
* user: oscar
* user: papa
* user: quebec
* user: romeo
* user: sierra
* user: tango
* user: uniform
* user: victor
* user: whiskey
* user: x-ray
* user: yankee
* user: zulu
* oddball:include
* oddball:exclude

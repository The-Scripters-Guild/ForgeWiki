# Area Monitors

An `Area Monitor` node is a powerful tool in game development that allows the game to recognize the boundary of an object. Here are some important things to know about using an Area Monitor node:

- To create an Area Monitor, you need to use an Area Monitor node and relate that node to the object that has the boundary you want to monitor. To create this relation, you must connect an object reference to the Area Monitor node's Monitor Object pin. The node will then recognize the boundary of the object and monitor any objects that enter or exit that area.
- The `Get Objects in Area Monitor` node can be used in conjunction with the Area Monitor node to get a list of objects that have entered or exited the monitored area during an unrelated event.
- By plugging the Area Monitor node into the appropriate "____ Area" nodes, you can trigger events in the game when objects enter or exit the monitored area. Examples of these nodes include `Player Entered Area` and `Object Exited Area`.
- Area Monitors can also be registered as audio zones using the `Register Audio Zones` node. If you want to remove an audio zone, you can use the `Unregister Audio Zone` node.
- When tracking something to see if it is in the zone or not, to change its traits, keep lists up to date, etc, it is almost always more efficient to have circuits set up tracking enter/exit events and modifying those things at the time of those events than constantly polling the contents of the zone using a timer.

Area Monitors are a versatile tool that can be used in a variety of scenarios to trigger events, monitor objects, and manage audio.

#### Contributors
Captain Punch
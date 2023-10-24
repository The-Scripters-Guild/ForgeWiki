# Using Pub-Sub for Scripting in Halo Infinite's Forge Mode

In Halo Infinite's Forge Mode, pub-sub (short for publisher-subscriber) pattern can be used to communicate between different script brains without needing an explicit reference. This can be achieved by using a self-reference to the script brain itself, even when it is copied.

One example of using pub-sub in Forge mode is in the system that handles nav markers for tsg.Sportsball (https://discordapp.com/channels/220766496635224065/1038672314969116743). The pattern involves obtaining the object reference and passing it to the central logic through pub-sub communication channels. This approach allows the central logic to extract the team information from the object's metadata and assign appropriate Nav Marker settings for each team.

Specifically, that example works as follows:

* Waypoints are defined.
* A custom event is triggered that the output for exists on each goal's script brain (the script brains are the goal objects).
* The only thing this custom event output does is fire another custom event where the output only exists once, on the brain where waypoints are configured.
* However, this custom event has the object reference of the goal passed back through it.
* This, in effect, creates a for-each loop that runs for each goal, passing their object references back to the main logic and allowing for the code that places their waypoints based on their team affiliation to exist only once on the level.

Overall, the use of pub-sub in scripting for Halo Infinite's Forge mode allows for more efficient communication and flexible design patterns without relying on explicit references.

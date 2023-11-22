# Using Pub-Sub for Scripting in Halo Infinite's Forge Mode

Pub/Sub (short for publisher-subscriber) is an asynchronous and scalable messaging pattern that decouples services producing messages from services processing those message. For our purposes, this means we can broadcast events without needing to target specific objects when making that broadcast, but still have a set of specific objects respond to those broadcasts.

In Halo Infinite's Forge Mode, the pub-sub pattern can be used to communicate between different script brains without needing an explicit reference. This can be achieved by using a self-reference to the script brain itself, which will always self reference, even when the brain is copied (the new brain will have a node referencing itself).

With a single subscriber object (a Script Brain) the pattern involves obtaining the object reference and passing it to the central logic through pub-sub communication channels, for which we are using sets of global Custom Events. This approach allows the central logic to extract the information from the object's metadata and execute code in relation to it.

Specifically, this works as follows:
- A custom event, we'll call this [publish], is triggered. An [On Custom Event, Global] node for this event exists on each subscriber script brain.
- The only thing this custom event output does is trigger another custom event, we'll call this one [publishReturn]. It only has one output node, on the same brain that has the trigger for [publish]
- [publishReturn] has the object reference of the subscriber brain, as well as possibly a number or object list, passed back through it. 
- This, in effect, creates a for-each loop that runs for each subscriber, passing their object references back to the main logic and allowing for the code that needs to run in relation to the captured data to exist on a single Script Brain and only once.

Overall, the use of pub-sub in scripting for Halo Infinite's Forge mode allows for more efficient communication and flexible design patterns without relying on explicit references.

#### Contributors
Captain Punch
Kwatzy
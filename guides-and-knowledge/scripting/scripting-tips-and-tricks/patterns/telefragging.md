---
description: >-
  Putting players in the respawn loop without triggering a death event by
  sending them so far out of bounds the game resets their biped.
---

# Telefragging

In Halo 5, this was accomplished by teleporting the player far out of bounds into regions that would trigger the biped reset. \
\
Halo Infinite is very similar, in that the mechanic works the same, but the process doesn't require manipulating teleporters. \
\
The simple method for this is using a Multiply node to get values beyond 1000 and using that to feed a Vector 3 and subsequent Teleport Player node. \
\
\- Multiply (1000 x 1000)\
\- Vector 3 (plug Multiply result into \*each\* input)\
\- Teleport Player (to the Vector 3)\
\
**Contributors**\
Captain Punch\
TheProgrammer163

# Referencing Thrown Grenades

This wiki entry explains how to get an object reference for a thrown grenade and use that reference with further scripts. This method relies on the fact that objects in an Area Monitor are added to the end of the list of objects in that area when they are first detected inside of it, the most recent object to enter the zone will always be last in the list.

## Method

1. **Use `On Grenade Thrown` event:** Utilize this event to detect when a player throws a grenade.
2. **Create an Area Monitor:** Set up an Area Monitor that follows the player to track grenades and projectiles.
3. **Access grenades and projectiles:** Retrieve grenades and projectiles from the Area Monitor when they enter it. They will behave like any other objects.
4. **Detect the most recent grenade:** To find the most recent grenade, get the objects from the Area Monitor and select the last object in the list.

#### Contributors
Captain Punch
Cookies
AgentZero


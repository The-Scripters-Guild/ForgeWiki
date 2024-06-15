---
description: >-
  Track information about AI units and reference it after death. Example code
  spawns tokens per enemy type at death location that players can pick up.
---

# tsg ai totems and kill tokens

##

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption><p>An image of the prefab. The blue cubes are the Totem objects. Each of the two brains below them handles Totems and Kill Tokens, respectively. The lower brain acts as an area monitor that deletes excess Kill Tokens if they are generated and not put into play, the glass is just there to funnel them and make it so they don't fall past that zone. The turret is used to generate the Kill Tokens.</p></figcaption></figure>

## Current File

[tsg ai totem and kill token kit v1](https://www.halowaypoint.com/halo-infinite/ugc/prefabs/5de45543-2314-470b-aba8-64ef9165f795)

### Boilerplate

This is a subset of the boilerplate code provided by the `tsg init` prefab.

If this is being used alongside an install of `tsg init`, this code should be deleted.

`tsg init` is explained in detail here: [tsg init](../map-mode-setup/tsg-init.md)

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

### Totems

#### Variable Declaration

* `mobTotems` - Object List Variable, Global
  * Objects with label User: Mike are added to this list at declaration.
* `totemOwners` - Object List Variable, Global
  * Holds the list of entities that have totems assigned to them.
* `assignedTotems` - Object List Variable, Global
  * Holds the list of totems that are currently assigned to entities.
* `cooldownTotems` - Object List Variable, Global
  * Holds the list of totems that are on cooldown, which prevents them from being assigned.
* `totemOwner` - Object Variable, Object
  * Stores a reference to the entity a totem is assigned to.
  * Is scoped to the totem owned by that entity.

<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

#### Poll Totems and Check Totem Owner Status

* For each Totem, check if `totemOwner` is a valid object
* If false, that AI is no longer alive/in the simulation
  * Remove Totem from `assignedTotems`
  * Add Totem to `cooldownTotems`
  * Call `ownerDied` to process the death of the current Totem's owner

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

#### Update Totem Ownership

* Clean up `totemOwners` list
  * For each AI Unit, remove from `totemOwners`
  * For each assigned Totem, add `totemOwner` to `totemOwners`
* For each AI Unit not in `totemOwners`...
  * Assign the first unassigned Totem that is not in `cooldownTotems` to the current unit
  * Assign the current unit as it's Totem's `totemOwner`
  * Add the current Totem to `assignedTotems`

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

#### State Monitoring

* Call `checkTotemOwnership`
* For each assigned Totem, set Totem location to offset from it's owner
  * Adjust offset with Vector 3 node

<figure><img src="../../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

#### Handle Totem Losing Ownership

* Call `processOwnerDeath`
* Wait N Seconds to keep Totem data available
* Delete and spawn Totem to reset Totem data
* Remove Totem from `cooldownTotems` so that it can be used again

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### Kill Tokens

#### Variable Declaration

* `killTokens` - Object List Variable, Global
  * Objects that are created to drop from dead units are added to this list when they are created.
* `activeKillTokens` - Object List Variable, Global
  * Kill Tokens that are in play and haven't been picked up are added to this list.
  * This list is not relevant to Gunball Machine Tokens.
* `playerInventory` - Number Variable, Object
  * The value that is adjusted to represent how many Kill Tokens a player has acquired.
* `killTokenValue` - Number Variable, Object
  * The number of Kill Tokens that an unit is configured to drop.
  * This value defaults to 1 and can be augmented during Totem config or any time between then and the unit's death

<figure><img src="../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

#### Totem Configuration

* Toggle event via adjusting hard-coded Branch node
* In this example, the Totem owner is examined and the value of `killTokenValue` is set based on their Character Type using a switch case

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

#### Distribute Kill Tokens on Owner Death

* For `killTokenValue` iterations...
  * Add the input Totem's position, plus offset, to `v3Queue`
  * Wait 0.1 Seconds
  * Call `gunball` to generate a Kill Token

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

#### Handle Kill Token Reset (Recursive Loop)

* Check to see if Totem is in `activeKillTokens` or if time has run out
  * If true, remove the Totem from `activeKillTokens` and delete it
  * If false, call `resetTokenLoop` with the input number value minus 1

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

#### Poll Active Kill Tokens and Player Locations to Handle Token Pick Up

* For each active Kill Token...
  * For each Player (all players)
    * Get current Player distance from current Kill Token
    * Check if distance < 8 units
    * If true, remove Kill Token from `activeKillTokens`, delete it, and increment `playerInventory` for current Player, and call `tokenPU`\* event

\* screenshot says 'motePU' instead of 'tokenPU'

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

#### Handle Players Dropping Kill Tokens on Death

* Call `tokenDrop` when a Player is killed
* For `playerInventory` \* X (where X is a 0-1 scalar to modify the magnitude) iterations...
  * Add the player's location, plus offset, to `v3Queue`
* Wait 0.1 seconds
* Call `gunball`
* Set current player's `playerInventory` to 0

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

### Gunball Machine

#### Clean Up Excess Kill Tokens and Prevent Token Pick Up as Weapon

* Sometimes the Gunball Machine makes extra Tokens
  * When tokens fall into the boundary, they are excess that wont get assigned, delete them
* Tokens shouldn't be picked up as weapons
  * On Token pickup, force dropping that Token

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

#### Generate Tokens

* Preload Gunball Machine at `gameplayInit`
  * Give turret a weapon (Generic Ball or Skull)
* On `gunball`
  * For input Iterations...
    * Wait 0.1 seconds
    * Give turret a weapon
    * Wait 0 seconds
    * Force turret to drop weapon
* On Weapon Dropped
  * Check if dropping unit is Gunball Machine (turret)
    * If true, add the dropped weapon to killTokens
    * Wait 0.1 seconds
    * Call `sendIt` and pass the dropped weapon

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

#### Put Generated Kill Tokens into Play

* Add current Token to `activeTokens`
* Set current Token to random rotation
* Set current Token position to Index 1 of `v3Queue`
* Update `v3Queue` to remove that entry
* Set current Token velocity to random (in ranges) upward and sideways velocity to produce fountain effect
* Call `resetTokenLoop` for current Token

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

## Contributors

Captain Punch

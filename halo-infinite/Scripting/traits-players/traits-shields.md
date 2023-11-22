# Shields

There may be times when you want to modify a player's base shields. This can be achieved through a combination of adjusting the game mode settings and applying scripted traits.

It is not possible to strip shields from a player using negative modifiers or damage object nodes. The damage object node will damage the player, but their shields will recharge and they will have the damaged shields UI and audio the whole time they are down; it can also bleed through and damage the player's health. 

As of Season 3, you can only grant *Bonus* Shields w/ traits.  As with the rest of the system, the label is very literal and very obviously tells you that you can only add to the value a player has as their base shield value.

## Adjusting Game Mode Settings

Mode settings determine the base shield value for all players. You can both reduce and raise a player's base shield value, here.

To have players spawn without shields, or with shields less than the default maximum, you need to change the settings for the game mode that you are loading the level with. It cannot 

## Applying Scripted Traits

Declare a Trait Set with `Declare Trait Set` with a `Bonus Shields` node plugged into it and apply it to players with `Apply Trait Set`.

If you have set the base shields to 0, you can grant Bonus Shields with a scalar of 1 using scripted traits to give the default base shields. You can remove this trait to take shields away, or you can give values between 0 and 1 to create diminished shield states for your mode designs.

It is important to note that traits stack, so you should remove a shield-granting trait before applying another if you're trying to adjust max shields for a player and want a predictable experience of you aren't intending for having stacking traits in your designs.

#### Contributors
Captain Punch
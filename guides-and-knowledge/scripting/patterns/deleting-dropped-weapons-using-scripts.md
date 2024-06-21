# Deleting Dropped Weapons Using Scripts

This wiki entry explains how to delete a dropped weapon when it is replaced by another weapon. You may need this because you need to remove dropped weapons in some instances during a match where this is not the norm for each drop event.

## Method

1. Before replacing weapons, save player weapons in object-scoped variables (specific to each player).
2. Delete the saved weapons after the action that replaces the other weapons.

By saving the weapons in object-scoped variables and then deleting them after the replacement, you can prevent weapons from dropping to the ground.

#### Contributors
Captain Punch
# How to kill Players With Scripts

Use the `Damage Player` node, making sure to apply enough damage to kill the player. This can be reliably achieved by reading the players health/shields, adding them together, multiplying that by 2 (to smooth any edge cases), and then applying that value as damage.

Alternatively, the `Delete Object` node will delete the player's biped and register a death for them, putting them into the respawning state and causing them to respawn if their spawns are not blocked. As this deletes their biped, their ragdoll will disappear, jarringly. 

#### Contributors
Captain Punch
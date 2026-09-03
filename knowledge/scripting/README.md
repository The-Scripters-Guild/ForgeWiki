---
description: >-
  testing the bot
---

# Scripting Know-how

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Managing player weapons through scripting involves different approaches depending on whether you intend to modify the player's inventory or simply change their current equipped item.

## Weapon Management Options

There are multiple ways to handle weapon changes depending on the desired outcome.

### Adding a New Weapon to Inventory
If the goal is to add a weapon to a player's inventory—which often results in them equipping it if they do not currently have one—use the following nodes:

* **[Give Player New Weapon](../../scripting/nodes/inventory/give-player-new-weapon.md)**: The standard node for adding an object to a player's inventory.
* **[Give Player Specific Weapon](../../scripting/nodes/inventory/give-player-specific-weapon.md)**: Used specifically for handing off a particular weapon object.

### Switching Between Held Weapons
If the player already possesses the weapon in their inventory and you want to force them to pull it out, use:

* **[Switch To First Weapon Of Type](../../scripting/nodes/inventory/switch-to-first-weapon-of-type.md)**: Use this to force a player to switch to a specific weapon type (such as switching from a pistol to a shotgun) if they already possess that weapon type.

## Managing Weapon Stance States

The **[Set Player Weapon Lowered](../../scripting/nodes/inventory/set-player-weapon-lowered.md)** node is used to set the lowered weapon state to TRUE or FALSE.

{% hint style="warning" %}
The game engine does not carry the "lowered" state over to the third-person character rig when a player performs a manual weapon swap.
{% endhint %}

### Bug In 3rd Person View
**The Issue:**
The game engine does not carry the "lowered" state over to the third-person character rig when a player performs a manual weapon swap. As a result, if a player is currently using a lowered weapon and swaps to a new one, the first-person view will correctly remain lowered, but the third-person model will default back to the raised (firing/aiming) position.

**The Solution:**
If you require a player to remain in a lowered stance through a weapon swap, you must call this node (setting it to true) immediately after the swap to manually re-apply the lowered state to the third-person model.

***

## Source Data

* Discord thread: [bot testing](https://discord.com/channels/220766496635224065/1545070232672931850/1545070232672931850)

#### <mark style="color:green;">Contributors</mark>

Captain Punch
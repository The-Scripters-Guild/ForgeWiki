---
description: >-
  Techniques for using Sandbox settings and weapon swapping to
  simulate magazine sizes.
---

# Nav Seed Points

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While Forge provides several methods for managing ammunition, scripting specific magazine capacities often requires a combination of Sandbox settings and weapon swapping to achieve desired results.

## Managing Magazine Capacity

Standard nodes such as [Add Player Ammo - Equipped](../../../scripting/nodes/inventory/add-player-ammo-equipped.md) and [Add Player Ammo - Unequipped](../../../scripting/nodes/inventory/add-player-ammo-unequipped.md) typically affect reserve ammunition rather than the current magazine count. To control the number of shots available before a reload is required, it is more effective to use Sandbox settings.

<figure><img src="../../../.gitbook/assets/IMG_6238.jpg" alt="A script attempting to manage ammo via team comparison."><figcaption><p>A script attempting to manage ammo via team comparison.</p></figcaption></figure>

{% hint style="info" %}
Sandbox settings in the custom game lobby allow for precise control over initial ammunition, but these settings apply globally to all players and bots.
{% endhint %}

<figure><img src="../../../.gitbook/assets/IMG_6246.jpg" alt="Sandbox settings used to define initial weapon ammunition."><figcaption><p>Sandbox settings used to define initial weapon ammunition.</p></figcaption></figure>

## Team-Specific Workarounds

To provide different magazine counts for different teams, a weapon-swapping workaround can be used via the [Give Player New Weapon](../../../scripting/nodes/inventory/give-player-new-weapon.md) node.

* **Full Magazine Teams:** Use the [On Player Spawned](../../../scripting/nodes/events-players/on-player-spawned.md) event to immediately give the player their intended weapons. Because the weapons are being issued via a script at spawn, they will arrive with full magazines regardless of Sandbox restrictions.
* **Limited Magazine Teams:** Allow the Sandbox settings to dictate the limited magazine count. You can use a [Wait For N Seconds](../../../scripting/nodes/logic/wait-for-n-seconds.md) node followed by a weapon swap to refresh the loadout or simulate a reload cycle.

<figure><img src="../../../.gitbook/assets/IMG_6245.jpg" alt="The player team spawning with the intended full magazines."><figcaption><p>The player team spawning with the intended full magazines.</p></figcaption></figure>

{% content-ref url="../../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md" %}
[submitting-content-to-the-wiki.md](../../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md)
{% endcontent-ref %}

***

## Source Data

* Discord thread: [Scripting limited ammo?](https://discord.com/channels/220766496635224065/1485449878598320339/1485449878598320339)

#### <mark style="color:green;">Contributors</mark>

Local Stranger\
Okom
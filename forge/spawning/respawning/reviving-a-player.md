---
description: >-
  Learn how to enable and configure player reviving mechanics,
  including manual orb activation and auto-revive settings.
---

# Reviving a Player

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While modes like Attrition or Firefight: King of the Hill have native revival systems, any custom game mode can be configured with these mechanics. This replaces the standard respawn cycle with a system where dead players drop Revive Orbs for teammates to activate.

## Enabling Reviving

To enable the reviving mechanic and override standard respawning functionality, navigate to `Health & Damage → Team Revive` in the settings of the desired game mode and apply a value other than "None". 

Enabling this functionality adds an additional win condition: if all players on one team are dead and can no longer be revived, the round will end.

### Auto-revive

Auto-revive allows players to be automatically revived after they have been dead for a specific duration. This is enabled by navigating to `Health & Damage → Auto-Revive` in the game mode settings. 

* The duration before an automatic respawn can be adjusted using the `Auto-Revive Timer`.
* Players who are automatically revived will spawn on a [Respawn Point](respawn-points.md) rather than at the location of their Revive Orb.

## Respawning and Map Requirements

When manual reviving is enabled, players who die drop a **Revive Orb**. A teammate can activate this orb to respawn the player at the position where the orb was dropped. 

{% hint style="info" %}
Maps intended for game modes using Revive Orbs should include enough [Respawn Points](respawn-points.md) to match the maximum intended player count. This is because if multiple players trigger an auto-revive at once (such as when progress in Firefight: King of the Hill triggers a set change), they may attempt to fill multiple respawn points simultaneously.
{% endhint %}

***

## Source Data

* Discord thread: [Reviving a Player](https://discord.com/channels/220766496635224065/1536542239134589098/1536542239134589098)

#### <mark style="color:green;">Contributors</mark>

Okom

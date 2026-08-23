---
description: >-
  An unconventional method for removing specific player names via Nav
  Marker visibility settings.
---

# Hiding Player Name Visibility

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

While player names are typically fixed in Halo Infinite, scripting provides an unconventional way to remove a specific player's name globally for all players.

## Hiding a Player's Name

To remove a player's name, a Nav Marker must be attached to that player using the [Attach Nav Marker To Object](../../../scripting/nodes/ui-nav-markers/attach-nav-marker-to-object.md) node. In custom games, this action inherently overrides the player's name.

### Hiding the Nav Marker

Because an attached Nav Marker remains visible and follows the player, its visibility must be adjusted to ensure it does not appear. This is achieved by using the [Set Player Distance Visibility Params](../../../scripting/nodes/ui-nav-markers/set-player-distance-visibility-params.md) node on the Nav Marker with the following settings:

* Min Distance: 0.00
* Max Distance: 0.00

This configuration clamps the visible viewing distance to 0, effectively making the Nav Marker hidden at all times. This technique works in both team-based modes and free-for-all modes where FFA Allegiance is utilized to create allied teammates.

<figure><img src="../../../.gitbook/assets/hide-player-name-script.webp" alt="hide-player-name-script.png"><figcaption><p>The required scripting nodes.</p></figcaption></figure>
<figure><img src="../../../.gitbook/assets/2026-08-23_JPEGView-rkKj.webp" alt="2026-08-23_JPEGView-rkKj.jpg"><figcaption><p>Friendly name hidden.</p></figcaption></figure>
<figure><img src="../../../.gitbook/assets/2026-08-23_JPEGView-kTvu.webp" alt="2026-08-23_JPEGView-kTvu.jpg"><figcaption><p>Enemy name hidden.</p></figcaption></figure>

{% hint style="warning" %}
The effect of disappearing player names cannot be previewed in Forge mode and only functions within a custom game.
{% endhint %}

## Restoring Player Name Visibility

To show a player's name again after using the Nav Marker attachment method, the Nav Marker must be detached from the player. A Nav Marker can be detached by having the object despawn or by adjusting the marker's position using the [Set Nav Marker Position](../../../scripting/nodes/ui-nav-markers/set-nav-marker-position.md) node.

#### Implementation Constraints

If a single Nav Marker is attached to multiple players, updating its position will cause it to detach from all of those players simultaneously. To selectively remove the Nav Marker (and thus the name) from only one specific player, the marker must first be detached from all players and then reattached to everyone except the intended target.

<figure><img src="../../../.gitbook/assets/detach-one-nav.webp" alt="detach-one-nav.png"><figcaption><p>An example of detaching a Nav Marker from an object.</p></figcaption></figure>
<figure><img src="../../../.gitbook/assets/2026-08-23_HaloInfinite-ArTw.webp" alt="2026-08-23_HaloInfinite-ArTw.jpg"><figcaption><p>A background player with their name successfully returned.</p></figcaption></figure>

## Removing Player Outlines

As an additional option, player outlines can be removed via the mode settings of the loaded mode using the following configurations in order to achieve a uniquely clean player UI, without any adjustments to players' local HUD settings:

* `HUD → Friendly Player Outlines`: Off
* `HUD → Enemy Player Outlines`: Off

<figure><img src="../../../.gitbook/assets/2026-08-23_JPEGView-05IJ.webp" alt="2026-08-23_JPEGView-05IJ.jpg"><figcaption><p>The mode settings used to disable player outlines.</p></figcaption></figure>

***

## Source Data

* Discord thread: [Hiding Player Name Visibility](https://discord.com/channels/220766496635224065/1541139305098125343/1541139305098125343)

#### <mark style="color:green;">Contributors</mark>

Okom

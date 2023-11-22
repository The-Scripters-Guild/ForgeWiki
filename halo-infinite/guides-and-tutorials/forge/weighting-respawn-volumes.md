---
description: >-
  Setting up your map to support different game modes with separate respawn
  combinations. This tutorial will focus on setting up the map for CTF game
  modes.
---

# Weighting Respawn Volumes

### Required Objects

* Spawn Volume Respawn

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption><p>Spawn Volume (Respawn)</p></figcaption></figure>

### Non-Weighted Respawn Volumes

Non-weighted respawn volumes are meant to

#### Labels

* Label 1: **Include CTF**

#### Team

Select the desired team (**Eagle** or **Cobra**) just below the boundary settings.

#### Spawn Volume Properties

* Weight: **0**
* Disable spawn points: **ON**
* Affects opposing team: **ON**

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption><p>Non-Weighted Respawn Volume</p></figcaption></figure>

### Weighted Respawn Volumes

Weighted respawn volumes can be useful for multiple reasons, mainly to help players spawn in to safe areas or potentially near combat action. This can useful after you have a baseline understanding of how your map is being played.

Since this example of the Spawn Volume Respawn is being setup for Capture the Flag game mode, the **Include CTF** label must be set on the object.

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Weighted Respawn Volume</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption><p>Weighted Respawn Volumes Overview</p></figcaption></figure>

### Label Set up

Settings under Gameplay -> Labels you will want to set the label to include CTF (or what ever game mode you are working with) this will make the volume only spawn up for CTF.\
Note: For example if you leave this blank you and decide to play slayer, Team sided spawns will still be on which can create a negative experience for spawn killing/ spawn control. So Just be mindful what volumes are set up for what mode

### Designated Team

What this will do is will disable any spawn from any other teams expect the destinated team that was set up above.

Why we set up the weight to be 0 so the volume doesn’t create any positive weighting for these zones the next section will set up weighted volumes. So its best to sperate Team designated volumes from weighted volumes to give the user better control over how their map behaves.

After these are set up Feel free to scale the size and placement of the volume to your desire on how you want your map to play. Usually you will just want to cover the designated team side of the map. You can create over lap but this will make it so no one will spawn in this location. Flip side if you decide not to create over lap you will create a neutral location where both teams can spawn.

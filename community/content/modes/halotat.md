---
description: >-
  Success in the help channel brought me here! thanks @Deathcrawller.
  We're working on bringing STRAFTAT's fast paced, best of 3 rounds to
  Halo Infinite.
---

# HALOTAT

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

HALOTAT is a project designed to bring the fast-paced, best-of-three round combat style of STRAFTAT to Halo Infinite. The mode emphasizes momentum-based movement and efficient match management through advanced scripting and prefab organization.

## Movement and Momentum

The gameplay experience is centered around high-speed interaction with the environment. One primary goal is to implement mechanics that allow for more vertical and lateral mobility than standard movement provides.

### Wall Jumping and Surface Interaction

To facilitate wall jumping, the system can utilize raycasting directed at the sides of the player. If the raycast detects a hit with a static surface, an invisible platform can be placed momentarily beneath the player to enable a jump.

<figure><img src="../../../.gitbook/assets/circlejump.webp" alt="Wall jumping movement"><figcaption><p>The circle jump demonstrates a method for performing wall-based jumps.</p></figcaption></figure>

Additionally, developers have explored the possibility of creating low-friction surfaces, similar to ice-themed maps, to enhance sliding mechanics, though the reliability of such surfaces may be limited.

## Spawning and Match Management

Managing how and where players appear is critical for maintaining the intended flow of the rounds.

### Spawn Sequencing and Randomization

Spawning can be managed by setting individual spawn orders within the object properties of each spawn point. For more complex setups, such as matches involving multiple zones, scripts can be used to cycle through spawn points.

To introduce variety into each match, spawning groups can be randomized. This is achieved by using a generic list of numbers to assign new spawn orders to specific groupings of spawn points at the start of a round.

<figure><img src="../../../.gitbook/assets/image-c08a.webp" alt="Spawning script brain"><figcaption><p>This script brain shows a method for managing spawn sequences.</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-78e3.webp" alt="Script error display"><figcaption><p>A script brain displays a warning regarding undeclared identifiers.</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-939c.webp" alt="Complex spawn logic"><figcaption><p>Several script brains work together to manage complex spawning and zone transitions.</p></figcaption></figure>

{% hint style="warning" %}
Using scripts to manage spawn sequencing may result in race conditions unless the scripts are injected into the existing spawn initialization process.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image-1d49.webp" alt="Gameplay view of spawns"><figcaption><p>Players are shown at spawn points within a configured match environment.</p></figcaption></figure>

### Playlist Organization via Prefabs

To streamline the creation of playlists, "maps" can be saved as prefabs. This approach allows a single map file to load a collection of different environment setups, effectively functioning as a playlist.

{% hint style="info" %}
While it is recommended to keep these map prefabs relatively simple, the hard limit for objects within a prefab is 255.
{% endhint %}

***

## Source Data

* Discord thread: [HALOTAT](https://discord.com/channels/220766496635224065/1475678585476874320/1475678585476874320)

#### <mark style="color:green;">Contributors</mark>

Aimless_E\
Deathcrawller\
Frogwyn\
Okom
---
description: >-
  Building the Audio of a forge map means generating a simple
  audio occlusion approximation of the map's geometry using
  voxelization technology.
---

# Building Audio

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Building the audio of a Forge map involves creating an approximation of environmental geometry to determine how sound interacts with the surroundings.

## Geometry Approximation and Occlusion

The building process creates an accurate approximation of the Forge map's geometry using voxelization technology. While there appears to be real-time occlusion occurring through approximated audio portals—allowing for roughly accurate muffling even if data is not up to date—it is recommended that a rebuild be performed whenever changes are made to the map's geometry to ensure accuracy.

<figure><img src="../../../.gitbook/assets/2026-08-16_brave-Ldny.webp" alt="Map audio building overview"><figcaption><p>A debug view of Aquarius inaccessible in Forge that reveals the underlying audio voxelization data.</p></figcaption></figure>

{% hint style="info" %}
A detailed look of the technical implementation of how audio data is handled in Halo Infinite can be seen here: [Chase Thompson Demo Reel: Halo Infinite](https://vimeo.com/776812151).
{% endhint %}

### Voxelization Mechanics

The generation of the audio occlusion map takes into account all visible objects on the map at the time of the build. However, if an object's visibility is hidden via the folder structure, it will be ignored by the process.

## Optimization Strategies

To ensure efficient data management, players can optimize the audio generation process to reduce both total build time and resulting download size. 

* Hide objects that are not involved in gameplay occlusion scenarios, such as distant skybox geometry or inaccessible areas.
* Place these non-essential items into a folder and hide them during the audio building process. This avoids generating unnecessary audio voxelization data in those specific areas.

{% hint style="info" %}
Building Audio is strictly limited to the generation of audio occlusion voxelization data; it does not activate or alter the usage of Audio Emitters or scripted audio.
{% endhint %}

***

## Source Data

* Discord thread: [Building Audio](https://discord.com/channels/220766496635224065/1538501688925626470/1538501688925626470)

#### <mark style="color:green;">Contributors</mark>

Okom

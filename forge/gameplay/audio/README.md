---
description: >-
  Implementation of audio in Forge via placeable emitters and scripted
  methods including 3D sound, music, and announcer voiceovers.
---

# Audio

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Audio in Forge can be implemented through the use of placeable objects or via scripting to play sound at specific locations, for individual players, or globally across a map.

## Audio Emitters

Audio Emitters are unique because their primary purpose is solely to emit audio. While some other objects like FX can also produce sound as a secondary function, the Audio Emitter allows for selecting from 24 different categories of audio loops, ranging from Alarms to Water and Insect sounds.

These emitters feature functionality that allows them to play distinct sounds for "friendly" and "enemy" players based on the object's Team setting. Players sharing a team with the object are considered friendly. Also if the object's Team is set to Neutral, the "friendly" sound plays for all players.

### Volume and Playback

Audio Emitters have a relatively low volume compared to primary sound effects like gunfire. Because there is no parameter within the object properties to adjust its loudness, the most effective way to increase perceived loudness is by stacking multiple instances of the same audio source in a single position.

{% hint style="info" %}
When previewing an Audio Emitter's output, the sound plays directly at the position of the Forge Monitor rather than the physical location of the object.
{% endhint %}

## Scripted Audio

Scripted audio offers greater versatility than placeable objects, although it can still be used to trigger sounds on already-placed objects.

### 3D Audio

3D Audio consists of scripted sounds played at a set position on the map. There are two primary categories of these sounds:

* **Ambient Loops:** These use the same audio loops available to the Audio Emitter object and utilize the following nodes:
  * **[Set Object 3D Audio Loop](../../../scripting/nodes/audio/set-object-3d-audio-loop.md):** Begins an audio loop at a specific object.
  * **[Stop Object 3D Audio Loop](../../../scripting/nodes/audio/stop-object-3d-audio-loop.md):** Stops the audio loop associated with that object.

* **Objective Alerts:** These consist of unique sounds related to interacting with game mode objectives, such as picking up a flag or losing a zone. They are used via:
  * **[Play 3D Audio For All Players](../../../scripting/nodes/audio/play-3d-audio-for-all-players.md)**
  * **[Play 3D Audio For Opposing Teams](../../../scripting/nodes/audio/play-3d-audio-for-opposing-teams.md)**
  * **[Play 3D Audio For Team](../../../scripting/nodes/audio/play-3d-audio-for-team.md)**

Some of these objective sounds are heard globally, while others exhibit volume drop-off as the player moves away from the sound's position. A resource for previewing how these sounds function can be found at [Halo Infinite Forge Mode Audio](https://www.youtube.com/watch?v=E24SkQXYUpM).

### Music

Music is a highly immersive feature that can be played globally, for specific teams, or per player through various "Music" nodes. Unlike other scripted audio, music in Forge cannot be positional. The volume of the playback can be adjusted via the Target Volume property, and fade-in/fade-out durations are controlled with the Fade Time property.

A reference library for all available music can be found at [Halo Infinite Forge Music Reference Library](https://lunnzies.notion.site/Halo-Infinite-Forge-Music-Reference-Library-2920870254d980c5ac0af86735699884).

#### Announcer Voiceovers

Announcer voiceovers provide audio cues that originate from game mode progression hints or when players achieve medals. These lines can be played globally, for specific teams, or per player. While there is no dedicated preview resource, the extensive selection of voices is named accurately (for example, "Enemy Captured Zone B"), allowing users to anticipate the content by name. Additionally, a special node, [Play Nearing Victory Audio For All Players](../../../scripting/nodes/audio/play-nearing-victory-audio-for-all-players.md), allows for playing the native "Player Nearing Victory" audio line to all players simultaneously.

### Audio Zones

Audio Zones are an uncommon feature intended to muffle or mute footstep sounds within the boundary of a specified [Area Monitor](../../../scripting/nodes/variables-basic/area-monitor.md). However, current observations suggest that these nodes may not function as intended, as significant changes in footstep volume have not been detected during test scenarios.

***

## Source Data

* Discord thread: [Audio](https://discord.com/channels/220766496635224065/1538486256856735845/1538486256856735845)

#### <mark style="color:green;">Contributors</mark>

Okom

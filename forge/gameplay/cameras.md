---
description: >-
  Cinematic camera sequences used to show map views at match start and
  winner stances at match end.
---

# Cameras

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Cameras are utilized to provide cinematic perspectives during the beginning and end of a match. These camera sequences are relatively simple in nature and offer limited opportunities for creative manipulation.

## Map Intro Cameras

Map Intro Cameras are used at the very start of a match to present a sequence of fade-in shots showcasing the map. To create one complete sequence, a pair of two Map Intro Camera objects is required; it is standard practice to use at least three pairs (six objects total) to display three distinct views of the map during the intro.

The camera perspectives play in order according to the Sequence Order property. Once all assigned camera pairs have been displayed, the order restarts from the beginning. Note that timing for these sequences is local to each individual player; consequently, it is not feasible to time global events (such as vehicle movement) with the camera sequence. Additionally, cameras cannot display different views for different teams, meaning every team will see the same sequence.

### Properties

The standard properties for a Map Intro Camera are straightforward:

* Sequence Order: An increasing value where the first camera is 1.00.
* Camera Blend: Set to Start or End.

To achieve the intended transition pattern, the first camera should have a Sequence Order of 1.00 and a Camera Blend set to Start. The second camera should have a Sequence Order of 2.00 and a Camera Blend set to End. Subsequent cameras follow this alternating pattern with increasing Sequence Order values.

{% hint style="info" %}
When placing Map Intro Cameras, it is useful to set your Field of View (FOV) to 73 to match the FOV used in camera shots. To mimic an angle accurately, spawn a Map Intro Camera object and move it close enough so that the position gizmo is at the center of your screen; you can then use Object-space rotation to match the desired perspective.
{% endhint %}

## Winning Team Outro

The Winning Team Outro provides a camera view at the conclusion of a match, featuring four members of the winning team in customizable stances. 

Because the camera perspective uses a very low FOV, it cannot be quickly previewed in-editor. To ensure that players fit within the framed scene and do not appear incorrectly against the background, ensure the Winning Team Outro object is placed sufficiently far away from the intended backdrop. While some creators use this feature to frame parts of the map elegantly behind players, others choose to build a custom scene specifically around the camera view.

### Orientation

The orientation of the Winnging Team Outro should be limited to rotation on the Yaw axis, which determines the direction the camera faces. 

{% hint style="warning" %}
Avoid applying rotation to the Pitch or Roll axes on Winning Team Outro objects. Doing so can cause significant offsets in the camera view, often resulting in players appearing underneath the map.
{% endhint %}

To enhance the visual quality of the final shot, forgers occasionally use 3-point lighting around the four players to improve the presentation of the winning team.

***

## Source Data

* Discord thread: [Cameras](https://discord.com/channels/220766496635224065/1536633993116651520/1536633993116651520)

#### <mark style="color:green;">Contributors</mark>

Okom
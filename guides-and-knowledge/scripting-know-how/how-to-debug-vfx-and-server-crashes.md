---
description: >-
  >-
---

# How to debug vfx and server crashes

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

When developing scripted custom game modes, maps may experience two primary types of instability: VFX flickering (where all effects in a scene are disabled but gameplay remains functional) or sudden server crashes.

## Debugging methodology

Because Forge does not provide detailed crash or debug logs for internal issues, troubleshooting relies on isolation and existing system logs.

### Script isolation

To identify which specific script is causing instability, use a process of elimination:
* Remove all scripting from the map and test for the issue.
* If the issue is no longer present, reintroduce half of the scripts and test again.
* Repeat this process, narrowing down the active scripts until the culprit is identified.

### Logging limitations

The Global Log within Forge is the primary source of information, but it has limitations. It can indicate when a script fails to execute fully, but it may not provide specific diagnostic data for Forge-level crashes or VFX failures.

## Common causes of instability

### VFX overload

Server crashes are sometimes related to FX overload. This can occur if a map is spawning and despawning a high volume of VFX frequently. Note that a single, very large scaled effect still counts as only one FX.

### Script performance and logic

High-frequency scripted events can impact stability. For example, running checks every 0.1 seconds to determine player locations for buff application can lead to performance issues.

#### Managing traits and buffs

When implementing buffs or traits based on player location, several methods can be used to improve performance and prevent logic errors:

* **List tracking:** Maintain lists to track which players already possess specific traits. This prevents the script from attempting to apply the same trait repeatedly.
* **Async Event validation:** To handle delayed buff application (such as checking if a player stays in an area for a certain duration), use an Async Event with a "wait" command. To ensure only the most recent check applies the buff, use an Object scoped number on the player that increments every time they enter or exit the area. The Async Event should check if the number sent at the start of the event still matches the player's current Object scoped number before applying the effect.

{% hint style="success" %}
When using Async Events for delayed logic, be cautious of the number of active events. If players frequently enter and exit areas, a high volume of long-running Async Events could potentially lead to crashes.
{% endhint %}

***

## Source Data

* Discord thread: [How to debug vfx and server crashes](https://discord.com/channels/220766496635224065/1481940440876974192/1481940440876974192)

#### <mark style="color:green;">Contributors</mark>

Terham\
Okom\
AddiCt3d 2CHa0s
---
description: >-
  Team Intro Spawns are the main way for players to spawn initially in
  team-based modes.
---

# Team Intro Spawns

A Team Intro Spawn is a [Forge Kit](../../../guides-and-knowledge/forge-know-how/forge-misc/forge-kit-objects.md) object consisting of four Initial Spawn Points and a Camera. This object is used to spawn in four players at the start of a match or round, and it has a built-in camera movement cycle that showcases each player before the initial [Gameplay Start](../../../scripting/nodes/events/on-gameplay-start.md).

Team Intro Spawns can be assigned to different Teams, and the Squad setting should be adjusted if more than four players per team should spawn on separate Team Intro Spawns.

The object names for the Team Intro Spawn are `Team Intro Arrow Front`, `Team Intro Arrow Left` & `Team Intro Arrow Right`.

<figure><img src="../../../.gitbook/assets/cover-team-intro-spawn.jpg" alt="A Team Intro Spawn"><figcaption></figcaption></figure>

## Placing the object

### Object path

* `Gameplay`
  * `Match Flow`
    * Team Intro Arrow Front
    * Team Intro Arrow Left
    * Team Intro Arrow Right

### Placement

The Team Intro Spawn should be placed where a group of four players on a Team should initially spawn on. In most cases these are in or around the main bases. If some of the spawn points on the Team Intro Spawn are floating, the players will be put on the nearest surface, and won't float in the air.

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-regular-forge.jpg" alt=""><figcaption><p>A good placement of a Team Intro Spawn</p></figcaption></figure>

### Camera

After the [Map Intro Camera](../../gameplay/cameras/map-intro-cameras/) sequence has ended and all players have successfully spawned in the game, the Camera in the Team Intro Spawn object will go through a static cycle showcasing all four players on it. After the four players have been shown, the Camera will move to the static position shown on the Forge Kit object.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-player1.jpg" alt=""><figcaption><p>Camera sequence 1</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-player2.jpg" alt=""><figcaption><p>Camera sequence 2</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-regular-ingame.jpg" alt=""><figcaption><p>Camera sequence 3</p></figcaption></figure>

</div>

#### Line-of-sight blockers

Make sure that no objects are blocking the view of the Camera. Otherwise, the Camera movement will look weird as it's passing through solid geometry or blocking the view towards the players at the end.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-blocked1.jpg" alt=""><figcaption><p>Geometry partly blocking visibility of the Camera from a Team Intro Arrow Front</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-blocked2.jpg" alt=""><figcaption><p>The Camera view at the end of the Team Intro sequence</p></figcaption></figure>

</div>

#### Height

The spawn points can intersect the ground by 1.5 units and still let a player spawn on them. Any floating spawns will set the player on the nearest surface underneath them.

<figure><img src="../../../.gitbook/assets/team-intro-spawn-height-1.5units-down.jpg" alt=""><figcaption><p>A spawn point can be 1.5 units under the ground and still spawn a player</p></figcaption></figure>

In situations where the ground is uneven and some spawns may be floating, the view of the final Camera should be prioritized over the height positioning of the spawn points.&#x20;

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-height-high-forge.jpg" alt=""><figcaption><p>High camera positioning in Forge</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-height-high-ingame.jpg" alt=""><figcaption><p>High camera positioning in gameplay</p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-height-low-forge.jpg" alt=""><figcaption><p>Low camera positioning in Forge</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-height-low-ingame.jpg" alt=""><figcaption><p>Low camera positioning in gameplay</p></figcaption></figure>

</div>

{% hint style="success" %}
Prioritize the final Camera placement over spawn point height as long as all players are able to spawn on their spawn point. This ensures that all players are fully visible in the final Camera view.
{% endhint %}

#### Blocked spawns

Placing the spawns lower than 1.5 units into the ground will cause them to be blocked. If a player can't spawn on their designated spawn point of the Team Intro Spawn, they will be relocated to a [Respawn Point](../respawning/respawn-points/) on the map. If no Respawn Points are available, [Backup Spawn Points](backup-spawn-points.md) will be used.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-too-low-forge.jpg" alt=""><figcaption><p>Spawn positioning too low causing some players to be blocked from spawning</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-camera-too-low-ingame.jpg" alt=""><figcaption><p>3/4 players are unable to spawn on blocked spawn points</p></figcaption></figure>

</div>

#### Rotation

The Team Intro Spawn can be rotated without issues, as long as no spawn points get blocked in the process. The final Camera view will take on the rotation of the Camera in the Forge Kit object.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-tilt-forge.jpg" alt=""><figcaption><p>Team Intro Spawn tilted to the left</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-tilt-ingame.jpg" alt=""><figcaption><p>One spawn was blocked due to the tilt</p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-sideways-forge.jpg" alt=""><figcaption><p>Team Intro Spawn 90° sideways</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-sideways-ingame.jpg" alt=""><figcaption><p>All of the spawns still work even with the object sideways</p></figcaption></figure>

</div>

If the Team Intro Spawn is placed upside-down, the player showcase order is reversed, and the final Camera rotation will be upside-down.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-upsidedown-forge.jpg" alt=""><figcaption><p>Team Intro Spawn upside-down</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-rotation-upsidedown-ingame.jpg" alt=""><figcaption><p>All of the spawns work when the object is upside-down</p></figcaption></figure>

</div>

{% hint style="info" %}
While it is possible to rotate the Team Intro Spawn to manipulate the final Camera view, it's not standard practice and will often look weird.
{% endhint %}



## Properties

### Physics

Setting the Physics value to "Phased" or "No Collision" will make moving the object easier as it won't collide with other objects.

### Assigning a Team

The <mark style="color:orange;">Team Designator</mark> property determines which Team spawns on the Team Intro Spawn.

| ADVANCED PROPERTIES |        |
| ------------------- | -----: |
| Team Designator:    | `TEAM` |

### Assigning a Squad

The <mark style="color:orange;">Squad</mark> property determines which Squad spawns on the Team Intro Spawn. Squads are used to order which Team Intro Spawns are filled first.

| ADVANCED PROPERTIES |         |
| ------------------- | ------: |
| Squad:              | `SQUAD` |

<details>

<summary><code>SQUAD</code> options</summary>

1. Alpha
2. Bravo
3. Charlie
4. Delta
5. Echo
6. Foxtrot
7. Gamma
8. Hotel

</details>

{% hint style="info" %}
When more than four players are present on a Team, the Squad order will be used to determine which Team Intro Spawn the players will initially spawn on.
{% endhint %}

## Practical setup

Here are examples on how to set up Team Intro Spawns in practice.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-cobra.jpg" alt=""><figcaption><p>Three Team Intro Spawns on Cobra Team</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-eagle.jpg" alt=""><figcaption><p>Three Team Intro Spawns on Eagle Team</p></figcaption></figure>

</div>

### 4v4

#### <mark style="background-color:blue;">Eagle Team</mark>

Team Intro Spawn 1

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |          `Alpha` |

#### <mark style="background-color:red;">Cobra Team</mark>

Team Intro Spawn 1

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 2 (Cobra)` |
| Squad:              |          `Alpha` |

### 12v12

#### <mark style="background-color:blue;">Eagle Team</mark>

Team Intro Spawn 1

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |          `Alpha` |

Team Intro Spawn 2

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |          `Bravo` |

Team Intro Spawn 3

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |        `Charlie` |

#### <mark style="background-color:red;">Cobra Team</mark>

Team Intro Spawn 1

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 2 (Cobra)` |
| Squad:              |          `Alpha` |

Team Intro Spawn 2

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 2 (Cobra)` |
| Squad:              |          `Bravo` |

Team Intro Spawn 3

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 2 (Cobra)` |
| Squad:              |        `Charlie` |

{% hint style="info" %}
It's possible to add more than the required minimum amount of Team Intro Spawns if you want to support a larger lobby in Custom Games. Just remember to increment the Squad value for each new Team Intro Spawn per Team.
{% endhint %}

### Infection & Firefight:King of The Hill

Infection and Firefight:King of The Hill are modes where Team Intro Spawns are required only on the Eagle side.

<figure><img src="../../../.gitbook/assets/team-intro-spawn-infection.jpg" alt=""><figcaption><p>Eagle side Team Intro Spawn on an Infection map</p></figcaption></figure>

{% hint style="success" %}
The same Team Intro Spawns used for a 4v4 or 12v12 setup can be used as the spawns for Infection and FFKOTH, as long as the object [labeling](team-intro-spawns.md#labeling) doesn't prevent it.
{% endhint %}

#### <mark style="background-color:blue;">Eagle Team</mark>

Team Intro Spawn 1

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |          `Alpha` |

Team Intro Spawn 2 (Infection)

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |          `Bravo` |

Team Intro Spawn 3 (Infection)

| ADVANCED PROPERTIES |                  |
| ------------------- | ---------------: |
| Team Designator:    | `Team 1 (Eagle)` |
| Squad:              |        `Charlie` |

{% hint style="info" %}
The standard player count of Infection is 12 with 10 of the players being Survivors, requiring three Team Intro Spawns.

Firefight:King of The Hill is intended for only four players so one Team Intro Spawn is enough.
{% endhint %}

Read more about Infection and Firefight:King of The Hill:

{% content-ref url="../../modes/infection.md" %}
[infection.md](../../modes/infection.md)
{% endcontent-ref %}

{% content-ref url="../../modes/firefight/firefight-koth/" %}
[firefight-koth](../../modes/firefight/firefight-koth/)
{% endcontent-ref %}



## Labeling

In some cases, it can be useful to have players spawn in a different location in asymmetrical modes that may be played on the same map where a symmetrical Team Intro Spawn setup is present. For these situations, Labels can be used to include and exclude certain spawns.

<div>

<figure><img src="../../../.gitbook/assets/team-intro-spawn-ctf-exclude.jpg" alt=""><figcaption><p>CTF Exclude label on a Cobra spawn</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/team-intro-spawn-ctf-include.jpg" alt=""><figcaption><p>CTF Include label on another Cobra spawn</p></figcaption></figure>

</div>

### Assigning Labels

Regular spawns

| LABELS   |                    |
| -------- | -----------------: |
| Label 1: | `ALT MODE` Exclude |

Alternative spawns

| LABELS   |                    |
| -------- | -----------------: |
| Label 1: | `ALT MODE` Include |

{% hint style="info" %}
Make sure that the Team Designator and Squad values are setup correctly for the alternative mode spawns as well. If no other Team Intro Spawns are present for a Team in the alternative mode, the Squad value needs to start from Alpha.
{% endhint %}

Read more about Labels:

{% content-ref url="../../forge-basics-and-ui/forge-interface-and-controls/object-properties/labels.md" %}
[labels.md](../../forge-basics-and-ui/forge-interface-and-controls/object-properties/labels.md)
{% endcontent-ref %}



***

#### <mark style="color:green;">Contributors</mark>

Okom

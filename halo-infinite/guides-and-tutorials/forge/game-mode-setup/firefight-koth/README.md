---
description: How to configure your own Firefight KOTH modes and levels.
---

# Firefight KOTH

<figure><img src="../../../../../.gitbook/assets/firefight-header.png" alt=""><figcaption></figcaption></figure>

## Mode Config

By default, the mode is set up with predetermined squad definitions and the overrides to allow this built-in config are enabled.

<div>

<figure><img src="../../../../../.gitbook/assets/firefight-override-map-ai-placements.png" alt=""><figcaption><p>Overriding the AI Spawners on the level is required for the Override AI Placements Source setting to matter.</p></figcaption></figure>

 

<figure><img src="../../../../../.gitbook/assets/firefight-override-ai-placement-source.png" alt=""><figcaption><p>This setting determines if the mode will use 343's preconfigured Firefight experience, or if it will override it.</p></figcaption></figure>

</div>

These settings can be changed to make the mode pull lists from the Mode Options, or from the level itself. By default, the mode will override the settings on spawners placed on the level and use a configuration that we cannot see nor edit provided by 343 as the stock behavior of the mode.

The stock mode options provides a robust experience with a variety of enemies preselected. You can still control the flow of combat by deciding \*when\* specific spawners would be used (using the Subgroup Index setting), and it doesn't require configuring spawners with enemies.

Using the custom waves gives players easy ways to create modes like Gruntpocalypse and expect to be able to play them on any level that is properly configured for the base mode. To use the custom waves in the game mode settings, Override Map AI Placements must be set to `TRUE` and Override AI Placements Source must be set to `Custom`.\
\
To use the settings of spawners to decide which enemies to spawn, Override Map AI Placements simply needs to be set to `FALSE`.&#x20;

### Wave Config

<figure><img src="../../../../../.gitbook/assets/Firefight - Wave Set Options.jpg" alt=""><figcaption></figcaption></figure>

<details>

<summary>Wave Options</summary>

* Custom Wave A
* Custom Wave B
* Custom Wave C
* Custom Wave D
* Custom Wave E
* Custom Wave F
* Custom Wave G
* Standard Brutes 1
* Standard Brutes 2
* Standard Brutes 3
* Standard Elites 1
* Standard Elites 2
* Standard Elites 3
* Standard Grunts 1
* Standard Grunts 2
* Standard Grunts 3
* Standard Hunters 1
* Standard Hunters 2
* Standard Jackals 1
* Standard Jackals 2
* Standard Jackals 3
* Standard Jackal Sniper
* Standard Marines 1
* Standard Marines 2
* Standard Marines 3
* Standard Skimmers 1
* Standard Skimmers 2
* Standard Skimmers 3

</details>

<figure><img src="../../../../../.gitbook/assets/Firefight - Custom Waves Options.jpg" alt=""><figcaption><p>Custom Waves can be set up with up to 5 unit types apiece. <br>All spawnable units are available to be selected.</p></figcaption></figure>

## Minimum Object Placements

* 5 KotH Capture Zones w/ Label `Firefight Objective`
  * Each one must have a unique Group Index, set from 1 to 5
* 5 Zone Capture Plates\* w/ Label `Firefight Plate`
  * To affiliate one with a hill, just place it inside that hill's boundary
* 5 AI Spawners set to Team 2 w/ Label `Firefight Spawner`
  * If all of your spawners are only set to Subgroup Index 1 and Subgroup Index 2, they will only trigger as if they were set to Subgroup Index 1
    * Setting any spawners to Subgroup Index 3 will solve this issue
  * It will not matter what you set the enemies to on the spawner
  * There must be at least 1 each for Group Indexes 1-5
    * Generally, you would want to have many more than 1 spawner per Group Index
  * Triggered By Script should be set to `ON`
* 1 Weapon Pad or Rack\*\*
* 1 Equipment Pad\*\*

\* _Not required for the mode to function, but required for full UX and for Matchmaking standards_\
\*\* _Required because the "Weapon Drop" code can't run without them, which breaks the mode logic._

## Configuring Spawners

Aside from setting up enemies for bespoke experiences, which is not required for stock Firefight KoTH, the important settings for Spawners are all in the Indexes section.&#x20;

### Group Index

Group Index determines which hill the spawner will be affiliated with, which allows players to curate where enemies are coming from for each hill. Each spawner can only have a single Group Index.

<figure><img src="../../../../../.gitbook/assets/group-index-tooltip.png" alt=""><figcaption></figcaption></figure>

### Subgroup Indexes

Subgroup Indexes are different in that spawners can be assigned none or all of them. While Group Indexes determine which hill must be active for the spawner to be active, the Subgroup Index determines the juncture at which the spawner will be triggered during that phase.

<figure><img src="../../../../../.gitbook/assets/subgroup-index-tooltip.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../../.gitbook/assets/spawner-group-subgroup-index.png" alt=""><figcaption><p>Group Index and Subgroup Index control when a spawner is called during play.</p></figcaption></figure>

#### Subgroup Index 1

* Triggered _once_, when the hill is incoming.

#### Subgroup Indexes 2-10

* Triggered in sequence as the enemies from the prior spawn event are defeated, looping back to the start after all subgroups with members have been triggered.
* This sequence ends with the hill has reached 5% capture progress and the boss wave is spawned.

#### Subgroup Index Boss

* Triggered _once_, when the hill has reached 75% capture progress for the first time by Team 1.

### Other Considerations

\
Magic Sight should be set to `ON` for spawners that you want to ensure find the players.

Live Fire and other small levels prepared by 343 only use Subgroup Index 1, 2, and Boss, while Deadlock (a BTB level) uses 1-5 and Boss. Use the scale of these levels and how complexly their subgroup index config is done as your metric for how much depth is needed to prepare the mode on your levels.

**Contributors**\
Captain Punch\
Artifice\
Green

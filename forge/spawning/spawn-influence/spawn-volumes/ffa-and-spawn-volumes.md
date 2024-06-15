# FFA & Spawn Volumes

Implementing FFA Slayer respawns on maps that disallow spawn flipping in Slayer gametypes (designated with an Include Slayer label on spawn volumes with Affects Opposing Team & Disable Spawn Points set to "On") can be negatively affected by Spawn Volumes.

### Solution: 'Exclude FFA All' Label

To address the issue, it is recommended to put an Exclude FFA All label on map-covering spawn volumes set to Eagle and Cobra teams. This ensures that these volumes are ignored in FFA gametypes. Without this exclusion, players in the Neutral team (FFA) would have limited safe spawn areas, potentially causing undesirable gameplay situations.

### FFA Allegiance and Spawn System

FFA mode automatically sets the player's team to Neutral. The primary concern is that there are no safe spawns for the Neutral team if there are Spawn Volumes blocking spawns for all teams other than Team 1 and Team 2.

### Understanding FFA Allegiance

In FFA, the concept of Teams is replaced by FFA Allegiance. When units have Neutral FFA Allegiance, they find all other units to be hostile (neutral AI do not see other neutral AI as hostile), which is the default behavior in FFA.\
\
Players can be assigned an Allegiance, which uses the same datatype as Teams, and thus the same labels. Units with the same (non-neutral) FFA Allegiance see each other as if they are on the same team and see units with differing Allegiances as hostile.&#x20;

**Contributors**\
Captain Punch\
Okom\
VidGamesPete\
Yumudas Beegbut\
All Seeing Sage


# Trait Nodes

<details>
<summary>Combine Trait Lists

### Input Pins

pinId: Trait List A\
dataType: trait_list\
settings: defaultValue: String:Editor SettingspinId: Trait List B\
dataType: trait_list\
settings: defaultValue: String:Editor SettingspinId: Trait List C\
dataType: trait_list\
settings: defaultValue: String:Editor SettingspinId: Trait List D\
dataType: trait_list\
settings: defaultValue: String:Editor Settings

### Output Pins

pinId: Combined Trait List\
dataType: trait_list\
userData:

#### Editor Settings

### Node Category: Players_Traits</summary>
</details>

<details>
<summary>Get Random N Traits</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Trait List\
N

### Input Pins

pinId: Trait List\
dataType: trait\_list

#### Editor Settings

pinId: N\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1.0

### Output Pins

pinId: New List\
dataType: trait\_list\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Declare Trait Set Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Trait A\
dataType: forge\_trait

#### Editor Settings

settings: defaultValue: String: nil

pinId: Trait B\
dataType: forge\_trait

#### Editor Settings

settings: defaultValue: String: nil

pinId: Trait List\
dataType: trait\_list\
settings: defaultValue: String:

#### Editor Settings

userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Create Trait Set</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Trait A\
dataType: forge\_trait

#### Editor Settings

settings: defaultValue: String: nil

pinId: Trait B\
dataType: forge\_trait

#### Editor Settings

settings: defaultValue: String: nil

pinId: Trait List\
dataType: trait\_list\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Unused
</details>

<details>
<summary>Remove Trait Set From Player Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Player\
Remove Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Player\
dataType: object

#### Editor Settings

pinId: Remove Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Remove All Trait Sets Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Remove Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Remove Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Apply Trait Set To Player Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Player\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Player\
dataType: object

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Apply Trait Set For Seconds Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Player\
Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Player\
dataType: object

#### Editor Settings

pinId: Seconds\
dataType: number

#### Editor Settings

MinRange: 0

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Apply Trait Set Until Death Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute userData:

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Weapon Pickup Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Weapon Pickup\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Grenade Pickup Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Grenade Pickup\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Equipment Pickup Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Equipment Pickup\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Prevent Weapon Firing Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Prevent Firing

### Input Pins

pinId: Prevent Firing\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Prevent Weapon Firing\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Prevent Grenade Throwing Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Prevent Throwing

### Input Pins

pinId: Prevent Throwing\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Prevent Grenade Throwing\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Weapon Dropping Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapons Persist On Drop

### Input Pins

pinId: Weapons Persist On Drop\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Weapon Dropping\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Weapon Damage Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Weapon Damage\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Weapon Switch Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0.05\
Step: 0.05

### Output Pins

pinId: Trait: Weapon Switch Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Reload Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Empty Reload Scalar\
Tactical Reload Scalar

### Input Pins

pinId: Empty Reload Scalar\
dataType: number

#### Editor Settings

MinRange: 0.05\
Step: 0.05

pinId: Tactical Reload Scalar\
dataType: number

#### Editor Settings

MinRange: 0.05\
Step: 0.05

### Output Pins

pinId: Trait: Reload Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Infinite Ammo Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Infinite Ammo\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Bottomless Clip Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Bottomless Clip\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Grenade Damage Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Grenade Damage\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Grenade Detonation Radius Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Grenade Detonation Radius\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Grenade Impulse Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Grenade Impulse\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Melee Damage Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Melee Damage\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Melee Impulse Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Melee Impulse\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Melee Recovery Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0.05\
Step: 0.05

### Output Pins

pinId: Trait: Melee Recovery Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

MinRange: 0\
Step: 0.05

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Vehicle Passenger Only Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Vehicle Passenger Only\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: VFX - Active Camo Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Intensity Scalar\
Interpolation Scalar

### Input Pins

pinId: Intensity Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 1\
Step: 0.05

pinId: Interpolation Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: VFX - Active Camo\
dataType: forge\_trait\
userData:

#### Editor Settings

MinRange: 0\
Step: 0.05

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: VFX - Overshield Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: VFX - Overshield\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Shield HUD Visible Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Shield HUD Visible\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Motion Tracker Visible Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Motion Tracker Enabled

### Input Pins

pinId: Motion Tracker Enabled\
dataType: bool

#### Editor Settings

pinId: Enabled While Zooming\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: Trait: Motion Tracker Visible\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Motion Tracker Range Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Inner Ring Scalar\
Extended Range Scalar\
Vehicle Range Scalar

### Input Pins

pinId: Inner Ring Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Extended Range Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Vehicle Range Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Motion Tracker Range\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Damage Resistance Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Direct Damage Scalar\
Grenade Damage Scalar\
Explosive Damage Scalar

### Input Pins

pinId: Direct Damage Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Grenade Damage Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Explosive Damage Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Damage Resistance\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Headshot Protection Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Headshot Protection\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Deathless Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Deathless\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Shield Maximum Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 6.5\
Step: 0.05

### Output Pins

pinId: Trait: Shield Maximum\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Shield Recharge Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Recharge Delay Scalar\
Recharge Rate Scalar

### Input Pins

pinId: Recharge Delay Scalar\
dataType: number

#### Editor Settings

MinRange: -1000\
MaxRange: 1000\
Step: 0.05

pinId: Recharge Rate Scalar\
dataType: number

#### Editor Settings

MinRange: -1\
MaxRange: 1000\
Step: 0.05

### Output Pins

pinId: Trait: Shield Recharge\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Health Maximum Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 10\
Step: 0.05

### Output Pins

pinId: Trait: Health Maximum\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Health Recharge Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Recharge Delay Scalar\
Recharge Rate Scalar

### Input Pins

pinId: Recharge Delay Scalar\
dataType: number

#### Editor Settings

MinRange: -1000\
MaxRange: 1000\
Step: 0.05

pinId: Recharge Rate Scalar\
dataType: number

#### Editor Settings

MinRange: -1\
MaxRange: 1000\
Step: 0.05

### Output Pins

pinId: Trait: Health Recharge\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Vampirism Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Shield Scalar\
Health Scalar

### Input Pins

pinId: Shield Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Health Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Vampirism\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Jump Height Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Jump Height\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Movement Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Movement Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Movement Speed With Turret Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Movement Speed With Turret\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Player Gravity Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: -1000\
Step: 0.05

### Output Pins

pinId: Trait: Player Gravity\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Sprint Enabled Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Sprint Enabled\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Sprint Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Top Speed Scalar\
Time to Top Speed Scalar

### Input Pins

pinId: Top Speed Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Time to Top Speed Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Sprint Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Slide Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slide Speed Scalar\
Slide Duration Scalar

### Input Pins

pinId: Slide Speed Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

pinId: Slide Duration Scalar\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 0.05

### Output Pins

pinId: Trait: Slide Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Sprint Reload Enabled Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Sprint Reload Enabled\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Sprint Resets Recharge Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Sprint Resets Recharge\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Clamber Enabled Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins

pinId: Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Trait: Clamber Enabled\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Clamber Speed Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Scalar

### Input Pins

pinId: Scalar\
dataType: number

#### Editor Settings

MinRange: 0.05\
Step: 0.05

### Output Pins

pinId: Trait: Clamber Speed\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits
</details>

<details>
<summary>Trait: Loadout Weapons Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Primary Weapon Type

### Input Pins

pinId: Primary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Secondary Weapon Type\
dataType: weapon\_type\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: Trait: Loadout Weapons\
dataType: forge\_trait\
userData:

#### Editor Settings

#### Editor Settings

### Node Category: Players\_Traits\\
</details>

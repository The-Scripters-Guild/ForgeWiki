# Action Nodes

<details>

<summary>Spawn Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Spawn

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Spawn\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Reset Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Reset

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Reset\
dataType: object

#### Editor Settings

pinId: Reset Position\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

pinId: Reset Rotation\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

pinId: Reset Velocity\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Set Object Team To Neutral</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Set To Neutral

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Set To Neutral\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Delete Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Delete

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Delete\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Damage Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Damage\
Damage Amount

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Damage\
dataType: object

#### Editor Settings

pinId: Damage Amount\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 1000\
Step: 0.5

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Set Object Health Percentage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Percentage

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Percentage\
dataType: number

#### Editor Settings

MinRange: 1\
MaxRange: 100\
Step: 0.5

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Set Object Health Absolute</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Health Amount

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Health Amount\
dataType: number

#### Editor Settings

MinRange: 1\
MaxRange: 1000\
Step: 0.5

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Set Object Position</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Move\
Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Move\
dataType: object

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

pinId: Is Relative Position\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Set Object Velocity</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Move\
Velocity

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Move\
dataType: object

#### Editor Settings

pinId: Velocity\
dataType: vector3

#### Editor Settings

pinId: Is Relative\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Set Object Rotation</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Move\
Rotation

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Move\
dataType: object

#### Editor Settings

pinId: Rotation\
dataType: vector3

#### Editor Settings

pinId: Is Relative\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object To Move\
Angular Velocity

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object To Move\
dataType: object

#### Editor Settings

pinId: Angular Velocity\
dataType: vector3

#### Editor Settings

pinId: Is Relative\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Start Object Audio Loop</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Sound Tag

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Is Enemy Sound\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

pinId: Is Ally Sound\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

properties: propertyName: Sound Tag\
dataType: tag

#### Editor Settings

TagType: sound\_looping

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Stop Object Audio Loop</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Stop Ally Sound\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

pinId: Stop Enemy Sound\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Play Audio For All Players</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Position\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute properties: propertyName: Sound Tag\
dataType: tag

#### Editor Settings

TagType: sound\_response\
settings: defaultValue: String: nil

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Play Audio For Players On Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute properties: propertyName: Sound Tag\
dataType: tag

#### Editor Settings

TagType: sound\_response\
settings: defaultValue: String: nil

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Play Audio For Players Not On Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute properties: propertyName: Sound Tag\
dataType: tag

#### Editor Settings

TagType: sound\_response\
settings: defaultValue: String: nil

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Branch General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Condition

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Condition\
dataType: bool

#### Editor Settings

### Output Pins

pinId: Execute If True\
dataType: execute

#### Editor Settings

pinId: Execute If False\
dataType: execute

#### Editor Settings

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>For Each Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Objects

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Objects\
dataType: object\_list

#### Editor Settings

### Output Pins

pinId: On Loop Complete\
dataType: execute

#### Editor Settings

pinId: Execute Per Object\
dataType: execute

#### Editor Settings

pinId: Current Object\
dataType: object

#### Editor Settings

pinId: Current Index\
dataType: number

#### Editor Settings

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>For Each Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Objects

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Objects\
dataType: object\_list

#### Editor Settings

### Output Pins

pinId: On Loop Complete\
dataType: execute

#### Editor Settings

pinId: Execute Per Player\
dataType: execute

#### Editor Settings

pinId: Current Player\
dataType: object

#### Editor Settings

pinId: Current Index\
dataType: number

#### Editor Settings

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>For Each Bot</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Objects

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Objects\
dataType: object\_list

#### Editor Settings

### Output Pins

pinId: On Loop Complete\
dataType: execute

#### Editor Settings

pinId: Execute Per Bot\
dataType: execute

#### Editor Settings

pinId: Current Bot\
dataType: object

#### Editor Settings

pinId: Current Index\
dataType: number

#### Editor Settings

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>For N Iterations</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Iteration Count

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Iteration Count\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1

### Output Pins

pinId: On Loop Complete\
dataType: execute

#### Editor Settings

pinId: Execute Iteration\
dataType: execute

#### Editor Settings

pinId: Current Iteration\
dataType: number

#### Editor Settings

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>Trigger Custom Event</summary>

### Node Rules

ruleID: ValidUserIdentifier\
IdentifierKey: Identifier\
DeclarationNodeType: On Custom Event ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Object\
dataType: object\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Number\
dataType: number\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Object List\
dataType: object\_list\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Events\_Custom

</details>

<details>

<summary>Trigger Custom Event Global</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Object\
dataType: object\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Number\
dataType: number\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Object List\
dataType: object\_list\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Events\_Custom

</details>

<details>

<summary>Trigger Custom Event Global Async</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Object\
dataType: object\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Number\
dataType: number\
settings: defaultValue: String: nil

#### Editor Settings

pinId: Object List\
dataType: object\_list\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Events\_Custom

</details>

<details>

<summary>Set Slayer Score Per Kill</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer\
Team Score\
Player Score

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Slayer\
dataType: mode\_slayer

#### Editor Settings

pinId: Team Score\
dataType: number

#### Editor Settings

pinId: Player Score\
dataType: number

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Slayer Score Per Assist</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer\
Team Score\
Player Score

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Slayer\
dataType: mode\_slayer

#### Editor Settings

pinId: Team Score\
dataType: number

#### Editor Settings

pinId: Player Score\
dataType: number

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Slayer Suicide Penalty</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer\
Team Penalty\
Player Penalty

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Slayer\
dataType: mode\_slayer

#### Editor Settings

pinId: Team Penalty\
dataType: number

#### Editor Settings

pinId: Player Penalty\
dataType: number

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Slayer Teamkill Penalty</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer\
Team Penalty\
Player Penalty

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Slayer\
dataType: mode\_slayer

#### Editor Settings

pinId: Team Penalty\
dataType: number

#### Editor Settings

pinId: Player Penalty\
dataType: number

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set NavMarker Icon</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
IconIndex

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: IconIndex\
dataType: nav\_marker\_icon

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Set NavMarker Text</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
String

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: String\
dataType: string\_id

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Attach NavMarker To Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
Object\
Offset

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: Object\
dataType: object

#### Editor Settings

pinId: Offset\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Set NavMarker Position</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Set NavMarker Enabled</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: Enabled\
dataType: bool

#### Editor Settings

settings: defaultValue: Bool: true

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Set NavMarker Team Visibility</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
Team\
IsNegate

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

pinId: IsNegate\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Set NavMarker Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker\
Team

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Clear NavMarker Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: NavMarker

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: NavMarker\
dataType: nav\_marker

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI\_Nav\_Markers

</details>

<details>

<summary>Teleport Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Position

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

pinId: Teleport Player's Vehicle\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Set Player Camo</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Duration in Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Duration in Seconds\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 20

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Set Player Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Team

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Adjust Player Grenades</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Grenade Type\
Grenade Count

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Grenade Type\
dataType: grenade\_type

#### Editor Settings

pinId: Grenade Count\
dataType: number

#### Editor Settings

MinRange: -99\
MaxRange: 99\
Step: 1.0

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Refill Default Grenades</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Empty Player Grenades</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Empty Player Ammo</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Refill Player Ammo</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Add Player Ammo - Primary</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Refill Percent

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Refill Percent\
dataType: number

#### Editor Settings

MinRange: 0.0\
MaxRange: 100\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Add Player Ammo - Secondary</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Refill Percent

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Refill Percent\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 100\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Give Player New Weapon</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Weapon Type\
Weapon Addition Method

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Weapon Addition Method\
dataType: weapon\_addition\_method

#### Editor Settings

pinId: Wait Until Completion\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Give Player Specific Weapon General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Weapon\
Weapon Addition Method

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Weapon\
dataType: object

#### Editor Settings

pinId: Weapon Addition Method\
dataType: weapon\_addition\_method

#### Editor Settings

pinId: Wait Until Completion\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Switch to First Weapon of Type</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Weapon Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Weapon Type\
dataType: weapon\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Drop Specific Weapon General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Weapon

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Weapon\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Drop Weapon of Type General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Weapon Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

#### Editor Settings

pinId: Weapon Type\
dataType: weapon\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\\

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Wait For N Seconds Gameplay</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Seconds\
dataType: number

#### Editor Settings

MinRange: 0

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Logic

</details>

<details>

<summary>Set Vehicle Enterable By Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Vehicle\
dataType: object

#### Editor Settings

pinId: Enterable By Player\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Print Boolean To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Boolean

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Boolean\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Print Number To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Number

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Number\
dataType: number

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Print Player To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Print Team To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Print Vector3 To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vector

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Vector\
dataType: vector3

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Print Control State To Killfeed</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Control State

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Control State\
dataType: generic\_zone\_control\_state

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Debug

</details>

<details>

<summary>Empty Player Equipment</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Refill Player Equipment</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Attempt to Enter Vehicle</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Vehicle

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

#### Editor Settings

pinId: Vehicle\
dataType: object

#### Editor Settings

pinId: Preferred Seat\
dataType: seat\_type\
settings: defaultValue: String: Any

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles\\

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit operation: Add\\

pinId: Preferred Seat

</details>

<details>

<summary>Kick Player From Vehicle</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Kick Unit From Vehicle</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Clear Splash for All Players</summary>

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

Node Category: Unused

</details>

<details>

<summary>Clear Splash for Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI

</details>

<details>

<summary>Push Splash to All Players</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Message

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Duration in Seconds\
dataType: number\
settings: defaultValue: Float: 5

#### Editor Settings

MinRange: 2.5

pinId: Message\
dataType: ui\_message

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Push Splash to Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Message

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Duration in Seconds\
dataType: number\
settings: defaultValue: Float: 5

#### Editor Settings

MinRange: 2.5

pinId: Message\
dataType: ui\_message

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI

</details>

<details>

<summary>Push Splash to Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Message

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Duration in Seconds\
dataType: number\
settings: defaultValue: Float: 5

#### Editor Settings

MinRange: 2.5

pinId: Message\
dataType: ui\_message

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Update Objective Banner for Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Enabled

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Enabled\
dataType: bool

#### Editor Settings

pinId: Message\
dataType: ui\_message

#### Editor Settings

settings: defaultValue: String: nil

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: UI

</details>

<details>

<summary>Set Spawn In Vehicle For All Players</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled\
Vehicle Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Enabled\
dataType: bool

#### Editor Settings

pinId: Vehicle Type\
dataType: vehicle\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Set Spawn In Vehicle For Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled\
Player\
Vehicle Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Enabled\
dataType: bool

#### Editor Settings

pinId: Vehicle Type\
dataType: vehicle\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Set Spawn In Vehicle For Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Enabled\
Team\
Vehicle Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Enabled\
dataType: bool

#### Editor Settings

pinId: Vehicle Type\
dataType: vehicle\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Flip Vehicle</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Vehicle\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Scale and Destroy Vehicle</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle\
Duration in Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Vehicle\
dataType: object

#### Editor Settings

pinId: Duration in Seconds\
dataType: number

#### Editor Settings

MinRange: 0

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Vehicles

</details>

<details>

<summary>Set Loadout Weapons For All Players</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Primary Weapon Type\
Secondary Weapon Type\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Primary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Secondary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Loadout Weapons For Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Primary Weapon Type\
Secondary Weapon Type\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Primary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Secondary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Loadout Weapons For Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Primary Weapon Type\
Secondary Weapon Type\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Primary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Secondary Weapon Type\
dataType: weapon\_type

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Clear Loadout Weapons For All Players</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Clear Loadout Weapons For Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Clear Loadout Weapons For Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Apply Immediately

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

pinId: Apply Immediately\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Override Loadouts For All Players</summary>

### Input Pins

pinId: ActionStart\
dataType: execute

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

Node Category: Unused

</details>

<details>

<summary>Override Loadouts For Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Override Loadouts For Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Give Player New Equipment</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Equipment Type

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Equipment Type\
dataType: equipment\_type

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Adjust Player Equipment Charges</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Charge Count

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Charge Count\
dataType: number

#### Editor Settings

MinRange: -99\
MaxRange: 99\
Step: 1.0

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Set Player Equipment Charges</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Charge Count

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Charge Count\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 99\
Step: 1.0

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory\_Equipment

</details>

<details>

<summary>Set Player FFA Allegiance</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Team

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Set Respawn Penalty</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Penalty Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Penalty Seconds\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Set Spawn Point Enabled</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Spawn Point

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Spawn Point\
dataType: object

#### Editor Settings

pinId: Enabled\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects

</details>

<details>

<summary>Block Player Respawns</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Respawn Message

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Respawn Message\
dataType: respawn\_message

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Unblock Respawns for Player</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Add Bot Ambition To Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Target Object\
Bot Ambition

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Target Object\
dataType: object

#### Editor Settings

pinId: Bot Ambition\
dataType: forge\_bot\_ambition

#### Editor Settings

pinId: Team\
dataType: team\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Remove Bot Ambitions From Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Target Object

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Target Object\
dataType: object

#### Editor Settings

pinId: Only Specific Ambition Type\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

pinId: Ambition Type\
dataType: bot\_ambition\_type\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Add Bot To Match</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Bot Difficulty

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Bot Difficulty\
dataType: bot\_difficulty

#### Editor Settings

pinId: Team\
dataType: team\
settings: defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Bots

</details>

<details>

<summary>Remove All Bots From Match</summary>

### Input Pins

pinId: ActionStart\
dataType: execute

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

Node Category: Bots

</details>

<details>

<summary>Remove Specific Bot From Match</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Bot Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Bot Player\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Bots

</details>

<details>

<summary>Set Player Mark Override</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Override Enabled

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Override Enabled\
dataType: bool

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Players

</details>

<details>

<summary>Translate Object To Point</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Position\
Duration in Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

pinId: Duration in Seconds\
dataType: number

#### Editor Settings

MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in\
settings: defaultValue: String: CURVE\_BUILT\_IN.None

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Rotate Object To Point</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Rotation\
Duration in Seconds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Rotation\
dataType: vector3

#### Editor Settings

pinId: Duration in Seconds\
dataType: number

#### Editor Settings

MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in\
settings: defaultValue: String: CURVE\_BUILT\_IN.None

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Move Object To Transform</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Destination Object\
Duration in Seconds\
Movement Curve

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Object\
dataType: object

#### Editor Settings

pinId: Destination Object\
dataType: object

#### Editor Settings

pinId: Duration in Seconds\
dataType: number

#### Editor Settings

MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Objects\_Transform

</details>

<details>

<summary>Set Player Weapons Lowered</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object

#### Editor Settings

pinId: Enabled\
dataType: bool\
settings: defaultValue: Bool: true

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Inventory

</details>

<details>

<summary>Set Weapon Total Rounds</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon\
Rounds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Weapon\
dataType: object

#### Editor Settings

pinId: Rounds\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Weapon Magazine Ammo</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon\
Magazine Rounds

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Weapon\
dataType: object

#### Editor Settings

pinId: Magazine Rounds\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Set Weapons Reserve Ammo</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon\
Percent

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Weapon\
dataType: object

#### Editor Settings

pinId: Percent\
dataType: number

#### Editor Settings

MinRange: 0\
MaxRange: 100\
Step: 1

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Unused

</details>

<details>

<summary>Register Audio Zone</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Monitor\
Audio Zone Effect

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Monitor\
dataType: area\_monitor

#### Editor Settings

pinId: Audio Zone Effect\
dataType: forge\_audio\_zone\_effect

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Unregister Audio Zone</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Monitor

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Monitor\
dataType: area\_monitor

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Audio

</details>

<details>

<summary>Activate Generic Zone</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Zone

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Zone\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Generic\_Objectives

</details>

<details>

<summary>Deactivate Generic Zone</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Zone

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Zone\
dataType: object

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Generic\_Objectives

</details>

<details>

<summary>Create Stopwatch</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Start Immediately\
dataType: bool\
settings: defaultValue: Bool: false

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Stopwatches

</details>

<details>

<summary>Start Stopwatch</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Stopwatches

</details>

<details>

<summary>Restart Stopwatch</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Stopwatches

</details>

<details>

<summary>Reset Stopwatch</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Stopwatches

</details>

<details>

<summary>Pause Stopwatch</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

#### Editor Settings

#### Node Category: Stopwatches\\

</details>

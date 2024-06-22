# Manipulation Nodes

<details>

<summary>Add Object To List</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
Object To Add

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: Object To Add\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Remove Object From List</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
Object To Remove

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: Object To Remove\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>List Contains Object</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
Object

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Contains Object\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get List Size</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

#### Output Pins

pinId: Object Count\
dataType: number\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Object at Index</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
Index

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: Index\
dataType: number\\

**Editor Settings**

MinRange: 1\
Step: 1.0

#### Output Pins

pinId: Object\
dataType: object\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get First N Objects</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
N

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: N\
dataType: number\\

**Editor Settings**

MinRange: 0\
Step: 1.0

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Last N Objects</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
N

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: N\
dataType: number\\

**Editor Settings**

MinRange: 0\
Step: 1.0

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Random N Objects</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List\
N

#### Input Pins

pinId: Object List\
dataType: object\_list\\

**Editor Settings**

pinId: N\
dataType: number\\

**Editor Settings**

MinRange: 0\
Step: 1.0

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Combine Object Lists</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List A\
Object List B

#### Input Pins

pinId: Object List A\
dataType: object\_list\\

**Editor Settings**

pinId: Object List B\
dataType: object\_list\\

**Editor Settings**

#### Output Pins

pinId: Combined List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Shared Objects</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List A\
Object List B

#### Input Pins

pinId: Object List A\
dataType: object\_list\\

**Editor Settings**

pinId: Object List B\
dataType: object\_list\\

**Editor Settings**

#### Output Pins

pinId: Shared List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Unique Objects</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object List A\
Object List B

#### Input Pins

pinId: Object List A\
dataType: object\_list\\

**Editor Settings**

pinId: Object List B\
dataType: object\_list\\

**Editor Settings**

#### Output Pins

pinId: Unique List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Object Health</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: PercentHealth\
dataType: number\
userData:

**Editor Settings**

pinId: CurrentVitality\
dataType: number\
userData:

**Editor Settings**

pinId: MaximumVitality\
dataType: number\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Object Shield</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: PercentShield\
dataType: number\
userData:

**Editor Settings**

pinId: CurrentVitality\
dataType: number\
userData:

**Editor Settings**

pinId: MaximumVitality\
dataType: number\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Object Position</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Position\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Object Rotation</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Rotation\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Object Velocity</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Velocity\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Object Angular Velocity</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Angular Velocity\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Object Forward Vector</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Forward\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Object Up Vector</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Up\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Objects\_Transform\\**

</details>

<details>

<summary>Get Personal Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Total Score\
dataType: number\
userData:

**Editor Settings**

pinId: Round Score\
dataType: number\
userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Player Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Total Score\
dataType: number\
userData:

**Editor Settings**

pinId: Round Score\
dataType: number\
userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Team Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: Team\
dataType: team\\

**Editor Settings**

#### Output Pins

pinId: Total Score\
dataType: number\
userData:

**Editor Settings**

pinId: Round Score\
dataType: number\
userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Object Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Team\
dataType: team\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Is Valid Object</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Valid Object\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Is Player</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is A Player\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Is Dead</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Dead\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get All Players On Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: Team\
dataType: team\\

**Editor Settings**

#### Output Pins

pinId: Players\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get All Players</summary>

#### Output Pins

pinId: Players\
dataType: object\_list\
userData:

**Editor Settings**

#### Node Category: Players\\

</details>

<details>

<summary>Get Random Player</summary>

#### Output Pins

pinId: Player\
dataType: object\
userData:

**Editor Settings**

#### Node Category: Players\\

</details>

<details>

<summary>Get Number of Players</summary>

#### Output Pins

pinId: Player Count\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Players\\

</details>

<details>

<summary>Get Objects in Prefab</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Object List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Max Rounds</summary>

#### Output Pins

pinId: Maximum Rounds\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>Get Current Round</summary>

#### Output Pins

pinId: Current Round\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>Get Round Time</summary>

#### Output Pins

pinId: Seconds Remaining\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>Set Round Time</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Seconds Remaining

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Seconds Remaining\
dataType: number\\

**Editor Settings**

MinRange: 0\
Step: 1.0

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Score To Win</summary>

#### Output Pins

pinId: Score To Win\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>Set Score To Win</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Score To Win

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Score To Win\
dataType: number\\

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Number Of Teams</summary>

#### Output Pins

pinId: Number of Teams\
dataType: number\
userData:

**Editor Settings**

#### Node Category: Players\\

</details>

<details>

<summary>Get Objects in Area</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Monitor

#### Input Pins

pinId: Monitor\
dataType: area\_monitor\\

**Editor Settings**

#### Output Pins

pinId: Objects\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get Slayer Score Per Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer

#### Input Pins

pinId: Slayer\
dataType: mode\_slayer\\

**Editor Settings**

#### Output Pins

pinId: Team Score\
dataType: number\\

**Editor Settings**

userData:

pinId: Player Score\
dataType: number\\

**Editor Settings**

userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Slayer Score Per Assist</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer

#### Input Pins

pinId: Slayer\
dataType: mode\_slayer\\

**Editor Settings**

#### Output Pins

pinId: Team Score\
dataType: number\\

**Editor Settings**

userData:

pinId: Player Score\
dataType: number\\

**Editor Settings**

userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Slayer Suicide Penalty</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer

#### Input Pins

pinId: Slayer\
dataType: mode\_slayer\\

**Editor Settings**

#### Output Pins

pinId: Team Penalty\
dataType: number\\

**Editor Settings**

userData:

pinId: Player Penalty\
dataType: number\\

**Editor Settings**

userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Slayer Teamkill Penalty</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Slayer

#### Input Pins

pinId: Slayer\
dataType: mode\_slayer\\

**Editor Settings**

#### Output Pins

pinId: Team Penalty\
dataType: number\\

**Editor Settings**

userData:

pinId: Player Penalty\
dataType: number\\

**Editor Settings**

userData: userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Adjust Personal Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Score Adjustment

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: Score Adjustment\
dataType: number\\

**Editor Settings**

Step: 5.0

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Adjust Player Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Score Adjustment

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: Score Adjustment\
dataType: number\\

**Editor Settings**

Step: 1.0

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Adjust Team Score</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team\
Score Adjustment

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team\\

**Editor Settings**

pinId: Score Adjustment\
dataType: number\\

**Editor Settings**

Step: 1.0

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Player Holding Item</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Player\
dataType: object\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Unit Holding Item</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

#### Input Pins

pinId: Object\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Unit\
dataType: object\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Player Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Vehicle\
dataType: object\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Unit Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Vehicle\
dataType: object\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Is Driving Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Driving\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Gunner In Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Gunner\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Passenger In Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Passenger\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is In Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is In Vehicle\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Vehicle Driver</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Driver\
dataType: object\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Vehicle Gunner</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Gunner\
dataType: object\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Vehicle Occupants</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Occupant List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Vehicle Enterable By Player</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Enterable By Player\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Is Camouflaged</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Camouflaged\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Units\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Grappling</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Grappling\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Is Detected</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Detected\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Units\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Detected by Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Team

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

pinId: Team\
dataType: team\\

**Editor Settings**

#### Output Pins

pinId: Is Detected\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Units\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is In Knockback</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Grappling\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Units\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Overshield On</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Overshield On\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Player Aiming Vector</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Aiming Vector\
dataType: vector3\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Is Airborne</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Airborne\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Units\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Boarding</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Boarding\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Crouching</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Crouching\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Is Lunging</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Lunging\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Is Zoomed</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Zoomed\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Mark Is Overridden</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Mark Overridden\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Player Grenade Count</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Grenade Type

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: Grenade Type\
dataType: grenade\_type\\

**Editor Settings**

#### Output Pins

pinId: Grenade Count\
dataType: number\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Get Loadout Grenade Count</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Grenade Type

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: Grenade Type\
dataType: grenade\_type\\

**Editor Settings**

#### Output Pins

pinId: Loadout Grenade Count\
dataType: number\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Are Same Object</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object A\
Object B

#### Input Pins

pinId: Object A\
dataType: object\\

**Editor Settings**

pinId: Object B\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Are Same Object\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Are Same Player</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player A\
Player B

#### Input Pins

pinId: Player A\
dataType: object\\

**Editor Settings**

pinId: Player B\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Are Same Player\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Player Equipment Charges</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Charge Count\
dataType: number\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Get Player Weapons</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Equipped Weapon\
dataType: object\
userData:

**Editor Settings**

pinId: Unequippped Weapon\
dataType: object\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>End Round</summary>

#### Input Pins

pinId: ActionStart\
dataType: executepinId: End Game\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>End Round - All Lose</summary>

#### Input Pins

pinId: ActionStart\
dataType: executepinId: End Game\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>End Round - All Tie</summary>

#### Input Pins

pinId: ActionStart\
dataType: executepinId: End Game\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>End Round - Winning Player</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: End Game\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>End Round - Winning Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Team\
dataType: team\\

**Editor Settings**

pinId: End Game\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Squared Vehicle Speed</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Squared Vehicle Speed\
dataType: number\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Create UI Message</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Message Template

#### Input Pins

pinId: Message Template\
dataType: message\_template\\

**Editor Settings**

pinId: String 1\
dataType: string\_id\
settings: defaultValue: String: nil

**Editor Settings**

pinId: String 2\
dataType: string\_id\
settings: defaultValue: String: nil

**Editor Settings**

pinId: Player\
dataType: object\
settings: defaultValue: String: nil

**Editor Settings**

#### Output Pins

pinId: Message\
dataType: ui\_message\
userData:

**Editor Settings**

**Node Category: UI\\**

</details>

<details>

<summary>Create UI Message B</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Message Template

#### Input Pins

pinId: Message Template\
dataType: message\_template\_b\\

**Editor Settings**

pinId: String 1\
dataType: string\_id\
settings: defaultValue: String: nil

**Editor Settings**

pinId: X\
dataType: number\
settings: defaultValue: String: nil

**Editor Settings**

Step: 1.0

pinId: Y\
dataType: number\
settings: defaultValue: String: nil

**Editor Settings**

Step: 1.0

#### Output Pins

pinId: Message\
dataType: ui\_message\
userData:

**Editor Settings**

**Node Category: UI\\**

</details>

<details>

<summary>Get Vehicle Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Vehicle Type\
dataType: vehicle\_type\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Are Same Vehicle Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle A\
Vehicle B

#### Input Pins

pinId: Vehicle A\
dataType: object\\

**Editor Settings**

pinId: Vehicle B\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Are Same Base Vehicle Type\
dataType: bool\
userData:

**Editor Settings**

pinId: Are Same Vehicle Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Is Vehicle Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle\
Vehicle Type

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

pinId: Vehicle Type\
dataType: vehicle\_type\\

**Editor Settings**

#### Output Pins

pinId: Is Vehicle Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Is Overturned</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle

#### Input Pins

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Overturned\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Vehicles\\**

</details>

<details>

<summary>Get Weapon Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon

#### Input Pins

pinId: Weapon\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Weapon Type\
dataType: weapon\_type\
userData:

**Editor Settings**

pinId: Base Weapon\
dataType: base\_weapon\_type\\

**Editor Settings**

userData:

pinId: Configuration\
dataType: variant\_weapon\_type\\

**Editor Settings**

userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Are Same Weapon Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon A\
Weapon B

#### Input Pins

pinId: Weapon A\
dataType: object\\

**Editor Settings**

pinId: Weapon B\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Are Same Base Weapon Type\
dataType: bool\
userData:

**Editor Settings**

pinId: Are Same Weapon Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Is Weapon Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon\
Weapon Type

#### Input Pins

pinId: Weapon\
dataType: object\\

**Editor Settings**

pinId: Weapon Type\
dataType: weapon\_type\\

**Editor Settings**

#### Output Pins

pinId: Is Weapon Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Is Holding Weapon Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Weapon Type

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

pinId: Weapon Type\
dataType: weapon\_type\\

**Editor Settings**

#### Output Pins

pinId: Is Holding Weapon Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Holding Specific Weapon</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Weapon

#### Input Pins

pinId: Unit\
dataType: object\\

**Editor Settings**

pinId: Weapon\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Has Specific Weapon\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\\**

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename\\

pinId: Player\
data: Unit

</details>

<details>

<summary>Get Is Forge Mode</summary>

#### Output Pins

pinId: Is Forge Mode\
dataType: bool\
userData:

**Editor Settings**

#### Node Category: Game\_Mode\\

</details>

<details>

<summary>Get Is Game Mode</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Game Mode

#### Input Pins

pinId: Game Mode\
dataType: game\_mode\_label\\

**Editor Settings**

pinId: Result in Forge Mode\
dataType: bool\
settings: defaultValue: Bool: false

**Editor Settings**

#### Output Pins

pinId: Is Game Mode\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Game\_Mode\\**

</details>

<details>

<summary>Get Ni1</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins \\

#### Output Pins

pinId: nilBool\
dataType: bool\
userData:

**Editor Settings**

pinId: nilNumber\
dataType: number\
userData:

**Editor Settings**

pinId: nilObject\
dataType: object\
userData:

**Editor Settings**

pinId: nilTag\
dataType: tag\
userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Is Holding Equipment Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player\
Equipment Type

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

pinId: Equipment Type\
dataType: equipment\_type\\

**Editor Settings**

#### Output Pins

pinId: Is Holding Equipment Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Get Equipment Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Equipment

#### Input Pins

pinId: Equipment\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Equipment Type\
dataType: equipment\_type\
userData:

**Editor Settings**

pinId: Is Powerup\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Are Same Equipment Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Equipment A\
Equipment B

#### Input Pins

pinId: Equipment A\
dataType: object\\

**Editor Settings**

pinId: Equipment B\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Are Same Equipment Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Get Is Holding Any Equipment</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Holding Any Equipment\
dataType: bool\
userData:

**Editor Settings**

pinId: Is Holding Powerup\
dataType: bool\
userData:

**Editor Settings**

pinId: Equipment Type\
dataType: equipment\_type\
userData:

**Editor Settings**

**Node Category: Inventory\_Equipment\\**

</details>

<details>

<summary>Get Player FFA Allegiance</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Team\
dataType: team\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Player Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Team\
dataType: team\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get Respawn Timer</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Seconds Remaining\
dataType: number\
userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Respawn Penalty</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Penalty Seconds\
dataType: number\
userData:

**Editor Settings**

**Node Category: Players\\**

</details>

<details>

<summary>Get All Spawn Points</summary>

#### Output Pins

pinId: Spawn Points\
dataType: object\_list\
userData:

**Editor Settings**

#### Node Category: Objects\\

</details>

<details>

<summary>Get All Spawn Points For Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: Team\
dataType: team\\

**Editor Settings**

#### Output Pins

pinId: Spawn Point\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Was Melee Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

#### Output Pins

pinId: Was Melee Kill\
dataType: bool\
userData:

**Editor Settings**

pinId: Was Backsmack\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was Weapon Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

#### Output Pins

pinId: Was Weapon Kill\
dataType: bool\
userData:

**Editor Settings**

pinId: Was Headshot\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was With Specific Weapon</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Weapon

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

pinId: Weapon\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Was With Specific Weapon\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was With Weapon Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Weapon Type

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

pinId: Weapon Type\
dataType: weapon\_type\\

**Editor Settings**

#### Output Pins

pinId: Was With Weapon Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was Vehicle Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

#### Output Pins

pinId: Was Vehicle Kill\
dataType: bool\
userData:

**Editor Settings**

pinId: Was Splatter\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was With Specific Vehicle</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Vehicle

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

pinId: Vehicle\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Was With Specific Vehicle\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was With Vehicle Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Vehicle Type

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

pinId: Vehicle Type\
dataType: vehicle\_type\\

**Editor Settings**

#### Output Pins

pinId: Was With Vehicle Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was Grenade Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

#### Output Pins

pinId: Was Grenade Kill\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was With Grenade Type</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Grenade Type

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

pinId: Grenade Type\
dataType: grenade\_type\\

**Editor Settings**

#### Output Pins

pinId: Was With Grenade Type\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Was Assisted Kill</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

#### Input Pins

pinId: DeathContext\
dataType: death\_context\\

**Editor Settings**

#### Output Pins

pinId: Was Assisted Kill\
dataType: bool\
userData:

**Editor Settings**

pinId: Assisting Players\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Death\_Context\\**

</details>

<details>

<summary>Bot Ambition</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Ambition Type

#### Input Pins

pinId: Ambition Type\
dataType: bot\_ambition\_type\\

**Editor Settings**

#### Output Pins

pinId: Bot Ambition\
dataType: forge\_bot\_ambition\
userData:

**Editor Settings**

**Node Category: Unused\\**

</details>

<details>

<summary>Get Bot Is Difficulty</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Bot Player\
Bot Difficulty

#### Input Pins

pinId: Bot Player\
dataType: object\\

**Editor Settings**

pinId: Bot Difficulty\
dataType: bot\_difficulty\\

**Editor Settings**

#### Output Pins

pinId: Bot Is Difficulty\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Bots\\**

</details>

<details>

<summary>Get Is Bot</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Player

#### Input Pins

pinId: Player\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Is Bot\
dataType: bool\
userData:

**Editor Settings**

**Node Category: Bots\\**

</details>

<details>

<summary>Get Weapon Magazine Ammo</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon

#### Input Pins

pinId: Weapon\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Rounds\
dataType: number\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Weapon Magazine Capacity</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon

#### Input Pins

pinId: Weapon\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Maximum Rounds\
dataType: number\
userData:

**Editor Settings**

**Node Category: Inventory\\**

</details>

<details>

<summary>Get Objects By Label</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Label

#### Input Pins

pinId: Label\
dataType: megalo\_label\\

**Editor Settings**

#### Output Pins

pinId: New List\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Objects\\**

</details>

<details>

<summary>Get All Bots On Team</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: Team\
dataType: team\\

**Editor Settings**

#### Output Pins

pinId: Bot Players\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Bots\\**

</details>

<details>

<summary>Get All Bots</summary>

#### Output Pins

pinId: Players\
dataType: object\_list\
userData:

**Editor Settings**

#### Node Category: Bots\\

</details>

<details>

<summary>Get Generic Zone Control State</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Zone

#### Input Pins

pinId: Zone\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Current Control State\
dataType: generic\_zone\_control\_state\
userData:

**Editor Settings**

**Node Category: Generic\_Objectives\\**

</details>

<details>

<summary>Get Units in Generic Zone</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Zone

#### Input Pins

pinId: Zone\
dataType: object\\

**Editor Settings**

#### Output Pins

pinId: Units\
dataType: object\_list\
userData:

**Editor Settings**

**Node Category: Generic\_Objectives\\**

</details>

<details>

<summary>Get Elapsed Time</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

#### Input Pins

pinId: Identifier\
dataType: identifier\\

**Editor Settings**

#### Output Pins

pinId: Elapsed Seconds\
dataType: number\
userData:

**Editor Settings**

**Node Category: Stopwatches\\**

</details>

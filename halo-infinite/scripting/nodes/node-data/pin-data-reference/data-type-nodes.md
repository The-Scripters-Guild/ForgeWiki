# Data Type Nodes

<details>
<summary>Number Literal</summary>

### Output Pins

pinId: Out\
dataType: number\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Compare Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Operand A\
Operand B

### Input Pins

pinId: Operand A\
dataType: number\

pinId: Operand B\
dataType: number\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

pinId: Greater Than\
dataType: bool\
userData:

pinId: Less Than\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Number Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: number\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Number Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: number\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Number Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: number\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Increment Number Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Increment Value\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Increment Value\
dataType: number\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Logic
</details>

<details>
<summary>Bool Literal</summary>

### Output Pins

pinId: Out\
dataType: bool\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Declare Bool Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: bool\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Bool Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: bool\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Bool Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: bool\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Toggle Boolean Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Logic
</details>

<details>
<summary>Object Reference Reference</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: EntryId

### Output Pins

pinId: Object\
dataType: object\
userData:

EditableProperty: EntryId\
IsEditableOutput: true
settings:

properties: propertyName: EntryId\
dataType: number

</details>

<details>
<summary>Declare Object Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: object\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Object Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: object\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Object Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: object\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Object List Reference</summary>

### Input Pins

pinId: Object 1\
dataType: object\
settings:\
pinId: Object 2\
dataType: object\
settings:\
pinId: Object 3\
dataType: object\
settings:\
pinId: Object 4\
dataType: object\
settings:

### Output Pins

pinId: Object List\
dataType: object_list\
userData:

</details>

<details>
<summary>Declare Object List Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: object\_list\
settings: String: (ForgeCreateObjectList(nil))

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Object List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: object\_list\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Object List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: object\_list\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Team Literal</summary>

### Output Pins

pinId: Out\
dataType: team\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Compare Team Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team A\
Team B

### Input Pins

pinId: Team A\
dataType: team\

pinId: Team B\
dataType: team\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Team Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: team\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced\

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

Storage

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: team\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Team Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: team\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Vector3 Literal</summary>

### Input Pins

pinId: X\
dataType: number\
MinRange: -1000\
MaxRange: 1000\
Step: 0.1\
settings: Float: 0pinId: Y\
dataType: number\
MinRange: -1000\
MaxRange: 1000\
Step: 0.1\
settings: Float: 0pinId: Z\
dataType: number\
MinRange: -1000\
MaxRange: 1000\
Step: 0.1\
settings: Float: 0

### Output Pins

pinId: Out\
dataType: vector3\
userData:

</details>

<details>
<summary>Declare Vector3 Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: vector3\
settings: String: vector(0\ 0\ 0)

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced\

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

Storage

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: vector3\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Vector3 Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: vector3\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Area Monitor Parcel\ Declaration\ Literal</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

### Input Pins

pinId: Object\
dataType: object\

### Output Pins

pinId: AreaMonitor\
dataType: area\_monitor\
userData:
userData:

</details>

<details>
<summary>Declare NavMarker Declaration\ Parcel\ IdentifierDeclaration\ Literal</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: Identifier\
dataType: identifier\

### Output Pins

pinId: Out\
dataType: nav\_marker\
userData:

properties: propertyName: IconIndex\
dataType: number\
settings: String: 1
userData:

#### Node Category: UI\_Nav\_Markers
</details>

<details>
<summary>Get NavMarker Storage</summary>

### Node Rules

ruleID: ValidUserIdentifier\
IdentifierKey: Identifier\
DeclarationNodeType: Declare NavMarker

ruleID: RequiredNodeInput\
RequiredProperties: Identifier

### Input Pins

pinId: Identifier\
dataType: identifier\

### Output Pins

pinId: Out\
dataType: nav\_marker\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Slayer Parcel\ Declaration\ GameMode</summary>

### Output Pins

pinId: Slayer\
dataType: mode_slayer\
userData:\
userData:

### Node Category: Unused
</details>

<details>
<summary>Grenade Type Literal</summary>

### Output Pins

pinId: Out\
dataType: grenade_type\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Compare Grenade Type Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Grenade Type A\
Grenade Type B

### Input Pins

pinId: Grenade Type A\
dataType: grenade\_type\

pinId: Grenade Type B\
dataType: grenade\_type\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Grenade Type Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: grenade\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Grenade Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: grenade\_type\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Grenade Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: grenade\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Declare UI Message Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: ui\_message\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Message Template Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: ui\_message\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Message Template Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: ui\_message\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>String Literal</summary>

### Output Pins

pinId: Out\
dataType: string_id\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Declare String Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: string\_id\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get String Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: string\_id\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set String Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: string\_id\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Vehicle Type Literal</summary>

### Output Pins

pinId: Out\
dataType: vehicle_type\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Compare Vehicle Type Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Vehicle Type A\
Vehicle Type B

### Input Pins

pinId: Vehicle Type A\
dataType: vehicle\_type\

pinId: Vehicle Type B\
dataType: vehicle\_type\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Vehicle Type Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: vehicle\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Vehicle Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: vehicle\_type\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Vehicle Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: vehicle\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Vehicle Type Combination Literal</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Base Vehicle\
Configuration

### Input Pins

pinId: Base Vehicle\
dataType: vehicle\_type\

pinId: Configuration\
dataType: vehicle\_type\

### Output Pins

pinId: Out\
dataType: vehicle\_type\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Weapon Type Literal</summary>

### Output Pins

pinId: Out\
dataType: weapon_type\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Compare Weapon Type Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Weapon Type A\
Weapon Type B

### Input Pins

pinId: Weapon Type A\
dataType: weapon\_type\

pinId: Weapon Type B\
dataType: weapon\_type\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Weapon Type Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: weapon\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Weapon Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: weapon\_type\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Weapon Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: weapon\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Weapon Type Combination Literal</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Base Weapon\
Configuration

### Input Pins

pinId: Base Weapon\
dataType: base\_weapon\_type\

pinId: Configuration\
dataType: variant\_weapon\_type\

### Output Pins

pinId: Out\
dataType: weapon\_type\
userData:

</details>

<details>
<summary>Identifier Literal</summary>

### Output Pins

pinId: Identifier\
dataType: identifier\
userData:IsEditableOutput: true\
settings: String:

</details>

<details>
<summary>Dynamic Identifier Literal</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Number

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Number\
dataType: number\
Step: 1.0

### Output Pins

pinId: New Identifier\
dataType: identifier\
userData:
settings: String:

#### Node Category: Unused
</details>

<details>
<summary>Equipment Type Literal</summary>

### Output Pins

pinId: Out\
dataType: equipment_type\
userData:IsEditableOutput: true\
settings:

</details>

<details>
<summary>Compare Equipment Type Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Equipment Type A\
Equipment Type B

### Input Pins

pinId: Equipment Type A\
dataType: equipment\_type\

pinId: Equipment Type B\
dataType: equipment\_type\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Equipment Type Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: equipment\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Equipment Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: equipment\_type\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Equipment Type Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: equipment\_type\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Declare Trait Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: forge\_trait\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Get Trait Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: forge\_trait\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Set Trait Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: forge\_trait\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Unused
</details>

<details>
<summary>Trait List Reference</summary>

### Input Pins

pinId: Trait A\
dataType: forge_trait\
settings:\
pinId: Trait B\
dataType: forge_trait\
settings:\
pinId: Trait C\
dataType: forge_trait\
settings:\
pinId: Trait D\
dataType: forge_trait\
settings:

### Output Pins

pinId: Trait List\
dataType: trait_list\
userData:

### Node Category: Players_Traits
</details>

<details>
<summary>Declare Trait List Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: trait\_list\
settings: String: (ForgeAddTraitsToTraitList(nil))

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Get Trait List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: trait\_list\
userData:

#### Node Category: Unused
</details>

<details>
<summary>Set Trait List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: trait\_list\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Unused
</details>

<details>
<summary>Ambition Type Deliver Literal</summary>

### Output Pins

pinId: Out\
dataType: bot_ambition_type\
userData:IsEditableOutput: falseNode Category: Unused
</details>

<details>
<summary>Ambition Type Guard Literal</summary>

### Output Pins

pinId: Out\
dataType: bot_ambition_type\
userData:IsEditableOutput: falseNode Category: Unused
</details>

<details>
<summary>Ambition Type Interact Literal</summary>

### Output Pins

pinId: Out\
dataType: bot_ambition_type\
userData:IsEditableOutput: falseNode Category: Unused
</details>

<details>
<summary>Ambition Type Pickup Literal</summary>

### Output Pins

pinId: Out\
dataType: bot_ambition_type\
userData:IsEditableOutput: falseNode Category: Unused
</details>

<details>
<summary>Bot Difficulty Literal</summary>

### Output Pins

pinId: Out\
dataType: bot_difficulty\
userData:IsEditableOutput: truesettings

### Node Category: Bots
</details>

<details>
<summary>Compare Control States Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Control State A\
Control State B

### Input Pins

pinId: Control State A\
dataType: generic\_zone\_control\_state\

pinId: Control State B\
dataType: generic\_zone\_control\_state\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Megalo Label Literal</summary>

### Output Pins

pinId: Out\
dataType: megalo_label\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Nav Marker Icon Literal</summary>

### Output Pins

pinId: Out\
dataType: nav_marker_icon\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Unused
</details>

<details>
<summary>Weapon Addition Method Literal</summary>

### Output Pins

pinId: Out\
dataType: weapon_addition_method\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Forge Variable Scope Literal</summary>

### Output Pins

pinId: Out\
dataType: forge_variable_scope\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Respawn Message Literal</summary>

### Output Pins

pinId: Out\
dataType: respawn_message\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Movement Curve Literal</summary>

### Output Pins

pinId: Out\
dataType: curve_built_in\
IsEditableOutput: true\
settings: String: CURVE_BUILT_IN.NoneuserData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Forge Audio Zone Effect Literal</summary>

### Output Pins

pinId: Out\
dataType: forge_audio_zone_effect\
IsEditableOutput: true\
settings: Float: 0userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Game Mode Label Literal</summary>

### Output Pins

pinId: Out\
dataType: game_mode_label\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Generic Zone Control State Literal</summary>

### Output Pins

pinId: Out\
dataType: generic_zone_control_state\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>User Label Literal</summary>

### Output Pins

pinId: Out\
dataType: user_label\
IsEditableOutput: true\
settings:\
userData:

</details>

<details>
<summary>Declare User Label Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: user\_label\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get User Label Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: user\_label\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set User Label Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: user\_label\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Declare Squad Definition Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: ai\_squad\_definition\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Squad Definition Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: ai\_squad\_definition\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Squad Definition Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: ai\_squad\_definition\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Declare Squad Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: ai\_squad\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Squad Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: ai\_squad\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Squad Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: ai\_squad\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Compare Squad Handles Math</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Squad A\
Squad B

### Input Pins

pinId: Squad A\
dataType: ai\_squad\

pinId: Squad B\
dataType: ai\_squad\

### Output Pins

pinId: Equal\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Declare Generic Item Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: any\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>Get Generic Item Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: generic\_item\
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>Set Generic Item Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: any\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>Generic List Reference</summary>

### Input Pins

pinId: Any A\
dataType: any\
settings:\
pinId: Any B\
dataType: any\
settings:\
pinId: Any C\
dataType: any\
settings:\
pinId: Allow Duplicates\
dataType: bool\
settings: String: false

### Output Pins

pinId: Generic List\
dataType: generic_list\
userData:

### Node Category: Generic_Lists
</details>

<details>
<summary>Declare Generic List Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: any\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>Get Generic List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: generic\_list\
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>Set Generic List Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: any\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Generic\_Lists
</details>

<details>
<summary>AI Character Type Literal</summary>

### Output Pins

pinId: Out\
dataType: ai_character_type\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>AI Species Type Literal</summary>

### Output Pins

pinId: Out\
dataType: ai_species_type\
IsEditableOutput: true\
settings:\
userData:

### Node Category: Variables_Enums
</details>

<details>
<summary>Declare Wave Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: ai\_wave\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Wave Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: ai\_wave\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Wave Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: ai\_wave\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Declare Wave Manager Variable Declaration</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Initial Value\
dataType: ai\_wave\_manager\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Get Wave Manager Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: Identifier\
dataType: identifier\

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

### Output Pins

pinId: Out\
dataType: ai\_wave\_manager\
userData:

#### Node Category: Variables\_Advanced
</details>

<details>
<summary>Set Wave Manager Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties:\
Identifier\
Scope

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier\

pinId: Value\
dataType: ai\_wave\_manager\
settings:

pinId: Scope\
dataType: forge\_variable\_scope\

pinId: Object\
dataType: object\
settings:

</details>

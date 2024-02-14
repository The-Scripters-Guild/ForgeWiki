# AI Nodes

<details>
<summary>Spawn AI Squad</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Spawner

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Spawner

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI
</details>

<details>
<summary>Spawn AI Squad With Definition</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad Definition

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad Definition\
dataType: ai\_squad\_definition

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI
</details>

<details>
<summary>Get Squad Definition From Spawner General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Spawner

### Input Pins
pinId: Spawner

pinId: Squad Definition Overrides\
dataType: ai\_squad\_definition\_overrides\
settings: defaultValue: String: ForgeCreateAISquadDefinitionOverridesStruct()

### Output Pins
pinId: Squad Definition\
dataType: ai\_squad\_definition\
userData:

#### Node Category: AI
</details>

<details>
<summary>Combine Squad Overrides General</summary>

### Input Pins
pinId: Overrides A\
dataType: ai_squad_definition_overrides\
settings: defaultValue: String: nil

pinId: Overrides B\
dataType: ai_squad_definition_overrides\
settings: defaultValue: String: nil

pinId: Overrides C\
dataType: ai_squad_definition_overrides\
settings: defaultValue: String: nil

pinId: Overrides D\
dataType: ai_squad_definition_overrides\
settings: defaultValue: String: nil\

### Output Pins
pinId: Combined Overrides\
dataType: ai_squad_definition_overrides\
userData:\

#### Node Category: AI\

</details>

<details>
<summary>Squad Overrides (Initial State) General</summary>

### Input Pins
pinId: Zone\
settings: defaultValue: String: nil

pinId: Initial Combat State\
dataType: actor_basic_combat_status\
settings: defaultValue: String: nil

pinId: Facing Yaw\
dataType: number\
settings: defaultValue: String: nil\

### Output Pins
pinId: Squad Definition Overrides\
dataType: ai_squad_definition_overrides\
userData:

#### Node Category: AI\

</details>

<details>
<summary>Squad Overrides (Misc) General</summary>

### Input Pins
pinId: Team\
dataType: team\
settings: defaultValue: String: nil

pinId: Label\
dataType: user_label\
settings: defaultValue: String: ForgeCreateUserLabelStruct(nil)\
### Output Pins
pinId: Squad Definition Overrides\
dataType: ai_squad_definition_overrides\
userData:

#### Node Category: AI\

</details>

<details>
<summary>Squad Overrides (Behavior) General</summary>

### Input Pins
pinId: Blind\
dataType: bool\
settings: defaultValue: String: false

pinId: Deaf\
dataType: bool\
settings: defaultValue: String: false

pinId: Braindead\
dataType: bool\
settings: defaultValue: String: false

pinId: Magic Sight\
dataType: bool\
settings: defaultValue: String: false\

### Output Pins
pinId: Squad Definition Overrides\
dataType: ai_squad_definition_overrides\
userData:\

#### Node Category: AI\

</details>

<details>
<summary>Get Squad From Unit General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit

### Input Pins
pinId: Unit

### Output Pins
pinId: Squad\
dataType: ai\_squad\
userData:

#### Node Category: AI
</details>

<details>
<summary>Get All AI Squads General</summary>

### Output Pins
pinId: Squad List\
dataType: ai_squad_list
userData:Node Category: AI\

</details>

<details>
<summary>Get AI Squads On Team General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Team

### Input Pins
pinId: Team\
dataType: team

### Output Pins
pinId: Squad List\
dataType: ai\_squad\_list\
userData:

#### Node Category: AI
</details>

<details>
<summary>Get Squads From Spawner General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Spawner

### Input Pins
pinId: Spawner

### Output Pins
pinId: Squad List\
dataType: ai\_squad\_list\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Get Squads With Label General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Label

### Input Pins
pinId: Label\
dataType: user\_label

### Output Pins
pinId: Squad List\
dataType: ai\_squad\_list\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Get All Spawners General</summary>

### Output Pins
pinId: Spawner List\
dataType: object_list
userData:

#### Node Category: AI_Advanced
</details>

<details>
<summary>Kill All AI Squads</summary>

### Input Pins
pinId: ActionStart\
dataType: execute
### Output Pins
pinId: ActionComplete\
dataType: execute
userData:Node Category: AI
</details>

<details>
<summary>Kill AI Squad</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI
</details>

<details>
<summary>Get Units From Squad General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: Units\
dataType: object\_list\
userData:

#### Node Category: AI
</details>

<details>
<summary>Get All AI Units General</summary>

### Output Pins
pinId: Units\
dataType: object_list\
userData:

pinId: Unit Count\
dataType: number\
userData:

pinId: Random Unit\
userData:\

#### Node Category: AI
</details>

<details>
<summary>Get AI Units On Team General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Team

### Input Pins
pinId: Team\
dataType: team

### Output Pins
pinId: Units\
dataType: object\_list\
userData:

pinId: Unit Count\
dataType: number\
userData:

pinId: Random Unit\
userData:

#### Node Category: AI
</details>

<details>
<summary>Get Is AI General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Object

### Input Pins
pinId: Object

### Output Pins
pinId: Is AI\
dataType: bool\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Assign Unit To Squad</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Squad

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Unit

pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Set Global AI Difficulty</summary>

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Difficulty\
dataType: difficulty\
settings: defaultValue: String: DIFFICULTY.normal

pinId: CoOp Scalar\
dataType: coop_difficulty\
settings: defaultValue: String: COOP_DIFFICULTY.dynamic

pinId: Kill All Squads\
dataType: bool\
settings: defaultValue: String: false\

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI_Modifiers\

</details>

<details>
<summary>Apply Valhalla</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Enabled\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Apply Undetectable To AI</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Enabled

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Enabled\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Assign Squad To Team</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad\
New Team

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

pinId: New Team\
dataType: team

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Assign Squad To Zone</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Zone

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

pinId: Zone

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Get Squad Remaining Alive General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: Original Unit Count\
dataType: number\
userData:

pinId: Remaining Unit Count\
dataType: number\
userData:

pinId: Percent Remaining\
dataType: number\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Was Last Unit In Squad Gameplay</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

### Input Pins
pinId: DeathContext\
dataType: death\_context

### Output Pins
pinId: Was Last Unit In Squad\
dataType: bool\
userData:

#### Node Category: Death\_Context
</details>

<details>
<summary>Get Unit Count From Squad Definition General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad Definition

### Input Pins
pinId: Squad Definition\
dataType: ai\_squad\_definition

### Output Pins
pinId: Unit Count\
dataType: number\
userData:

pinId: Can Spawn Whole Squad\
dataType: bool\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Get AI Budget General</summary>

### Output Pins
pinId: Available Unit Count\
dataType: number
userData:

#### Node Category: AI_Advanced
</details>

<details>
<summary>Get Squad State General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: State\
dataType: actor\_basic\_combat\_status\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Compare Squad State General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad\_State\_A\
Squad\_State\_B

### Input Pins
pinId: Squad\_State\_A\
dataType: actor\_basic\_combat\_status

pinId: Squad\_State\_B\
dataType: actor\_basic\_combat\_status

### Output Pins
pinId: Are\_Same\_State\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Get AI Character Type General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit

### Input Pins
pinId: Unit

### Output Pins
pinId: Character Type\
dataType: ai\_character\_type\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Compare Character Type General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Type A\
Type B

### Input Pins
pinId: Type A\
dataType: ai\_character\_type

pinId: Type B\
dataType: ai\_character\_type

### Output Pins
pinId: Are Same Character Type\
dataType: bool\
userData:

pinId: Are Same Species\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Is AI Unit Of Species General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Species Type

### Input Pins
pinId: Unit

pinId: Species Type\
dataType: ai\_species\_type

### Output Pins
pinId: Is Of Species\
dataType: bool\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Possess AI Unit</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Player\
Unit

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Player

pinId: Unit

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Unused
</details>

<details>
<summary>Was Character Type General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: DeathContext\
Character Type\
Species Type

### Input Pins
pinId: DeathContext\
dataType: death\_context

pinId: Character Type\
dataType: ai\_character\_type

pinId: Species Type\
dataType: ai\_species\_type

### Output Pins
pinId: Are Same Character Type\
dataType: bool\
userData:

pinId: Are Same Species\
dataType: bool\
userData:

#### Node Category: Death\_Context
</details>

<details>
<summary>Was AI Killer General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: DeathContext

### Input Pins
pinId: DeathContext\
dataType: death\_context

### Output Pins
pinId: Was AI Killer\
dataType: bool\
userData:

#### Node Category: Death\_Context
</details>

<details>
<summary>Set AI Unit Magic Sight</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Magic Sight

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Unit

pinId: Magic Sight\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Set AI Unit Perception</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Blind\
Deaf

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Unit

pinId: Blind\
dataType: bool

pinId: Deaf\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Set AI Unit Braindead</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Braindead

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Unit

pinId: Braindead\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Get Squad Has Label General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Label

### Input Pins
pinId: Squad\
dataType: ai\_squad

pinId: Label\
dataType: user\_label

### Output Pins
pinId: Has Label\
dataType: bool\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Get Squad Team General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: Team\
dataType: team\
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>Set Healthbar Visible</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Visible

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Unit

pinId: Visible\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Set All Healthbars Visible</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Visible

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Visible\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Modify AI Targetable List</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: AddRemove\
Object\
Team

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: AddRemove\
dataType: add\_or\_remove

pinId: Object

pinId: Team\
dataType: team

pinId: Priority\
dataType: number\
settings: defaultValue: String: 0 MinRange: -0.95\
MaxRange: 1\
Step: 0.05

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Modify AI Targetable Object Methods</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Object\
GrenadeTargeting\
VehicleTargeting\
Discourage Melee Weapons

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Object

pinId: GrenadeTargeting\
dataType: bool

pinId: VehicleTargeting\
dataType: bool

pinId: Discourage Melee Weapons\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Get AI Targetable Object List General</summary>

### Output Pins
pinId: Object List\
dataType: object_list
userData:

pinId: Used Slots\
dataType: number
userData:

pinId: Remaining Slots\
dataType: number
userData:

#### Node Category: AI_Modifiers\

</details>

<details>
<summary>Set Squad Follow Object</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Object

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

pinId: Object

pinId: Follow Radius\
dataType: number\
settings: defaultValue: String: 50

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Set Squad Stop Following</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Modifiers
</details>

<details>
<summary>Ally Squad With FFA Player</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Squad

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

pinId: Player\
settings: defaultValue: String: nil

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Advanced
</details>

<details>
<summary>AI Wave General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Wave Type

### Input Pins
pinId: Wave Type\
dataType: ai\_wave\_type

pinId: Spawners\
dataType: object\_list\
settings: defaultValue: String: nil

pinId: Duration\
dataType: number\
settings: defaultValue: String: 0 MinRange: 0

pinId: Wave Options\
dataType: ai\_wave\_options\
settings: defaultValue: String: nil

### Output Pins
pinId: Wave\
dataType: ai\_wave\
userData:

#### Node Category: AI\_Waves
</details>

<details>
<summary>AI Wave Options General</summary>

### Input Pins
pinId: Incoming Messaging\
dataType: bool\
settings: defaultValue: String: false

pinId: Outgoing Messaging\
dataType: bool\
settings: defaultValue: String: false

pinId: Delay Spawn Until Budget\
dataType: bool\
settings: defaultValue: String: true

pinId: Extermination Percentage\
dataType: number\
settings: defaultValue: String: 100 MinRange: 1\
MaxRange: 100\

### Output Pins
pinId: Wave Options\
dataType: ai_wave_options
userData:

#### Node Category: AI_Waves\

</details>

<details>
<summary>Add Wave to Wave Manager General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Wave

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Wave\
dataType: ai\_wave

pinId: Wave Manager\
dataType: ai\_wave\_manager\
settings: defaultValue: String: ForgeCreateAIWaveManagerStruct(ForgeWaveManagerInstanceEnum.default)

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI\_Waves
</details>

<details>
<summary>Remove Upcoming Waves General</summary>

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Wave Manager\
dataType: ai_wave_manager\
settings: defaultValue: String: ForgeCreateAIWaveManagerStruct(ForgeWaveManagerInstanceEnum.default)

### Output Pins
pinId: ActionComplete\
dataType: execute\
userData:

#### Node Category: AI_Waves\

</details>

<details>
<summary>End Current Wave General</summary>

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Wave Manager\
dataType: ai_wave_manager\
settings: defaultValue: String: ForgeCreateAIWaveManagerStruct(ForgeWaveManagerInstanceEnum.default)

pinId: Victory Reason\
dataType: ai_wave_victory_reason
settings: defaultValue: String: ForgeWaveManagerVictoryReasons.none

pinId: Kill Remaining\
dataType: bool\
settings: defaultValue: String: false

pinId: Kill Stragglers\
dataType: bool\
settings: defaultValue: String: false\

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: AI_Waves\

</details>

<details>
<summary>Get Wave Manager Status General</summary>

### Input Pins
pinId: Wave Manager\
dataType: ai_wave_manager\
settings: defaultValue: String: ForgeCreateAIWaveManagerStruct(ForgeWaveManagerInstanceEnum.default)

### Output Pins
pinId: Has Active Wave\
dataType: bool\
userData:

pinId: Queue Size\
dataType: number\
userData:

#### Node Category: AI_Waves\

</details>

<details>
<summary>Get Current Wave Status General</summary>

### Input Pins
pinId: Wave Manager\
dataType: ai_wave_manager\
settings: defaultValue: String: ForgeCreateAIWaveManagerStruct(ForgeWaveManagerInstanceEnum.default)

### Output Pins
pinId: Active Squads\
dataType: ai_squad_list\
userData:

pinId: Straggler Squads\
dataType: ai_squad_list\
userData:

pinId: Percent Remaining\
dataType: number\
userData:

pinId: Duration Remaining\
dataType: number\
userData:

#### Node Category: AI_Waves\

</details>

<details>
<summary>Compare Wave Victory Reason General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Victory Reason A\
Victory Reason B

### Input Pins
pinId: Victory Reason A\
dataType: ai\_wave\_victory\_reason

pinId: Victory Reason B\
dataType: ai\_wave\_victory\_reason

### Output Pins
pinId: Are Same Victory Reason\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Compare Wave Managers General</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Wave Manager A\
Wave Manager B

### Input Pins
pinId: Wave Manager A\
dataType: ai\_wave\_manager

pinId: Wave Manager B\
dataType: ai\_wave\_manager

### Output Pins
pinId: Are Same Wave Manager\
dataType: bool\
userData:

#### Node Category: Logic\_Compare
</details>

<details>
<summary>Print Victory Reason To Killfeed</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Victory Reason

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Victory Reason\
dataType: ai\_wave\_victory\_reason

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Debug\\

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Unit

pinId: Vehicle

pinId: Preferred Seat\
dataType: seat\_type\
settings: defaultValue: String: Any

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Vehicles\\

nodeVersionRule: ruleID: NodeVersionRuleUpdatePinProperty\
nodeOperations: operation: Rename

pinId: Player\
data: Unit operation: Add

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

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Unit

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Vehicles
</details>

<details>
<summary>Clear Splash for All Players</summary>

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Unused\

</details>

<details>
<summary>Clear Splash for Player</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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
settings: defaultValue: Float: 5 MinRange: 2.5

pinId: Message\
dataType: ui\_message

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Duration in Seconds\
dataType: number\
settings: defaultValue: Float: 5 MinRange: 2.5

pinId: Message\
dataType: ui\_message

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Duration in Seconds\
dataType: number\
settings: defaultValue: Float: 5 MinRange: 2.5

pinId: Message\
dataType: ui\_message

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Enabled\
dataType: bool

pinId: Message\
dataType: ui\_message\
settings: defaultValue: String: nil

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Vehicle Type\
dataType: vehicle\_type

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Enabled\
dataType: bool

pinId: Vehicle Type\
dataType: vehicle\_type

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Enabled\
dataType: bool

pinId: Vehicle Type\
dataType: vehicle\_type

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Vehicle

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Vehicle

pinId: Duration in Seconds\
dataType: number\
MinRange: 0

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Secondary Weapon Type\
dataType: weapon\_type

pinId: Apply Immediately\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Primary Weapon Type\
dataType: weapon\_type

pinId: Secondary Weapon Type\
dataType: weapon\_type

pinId: Apply Immediately\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Primary Weapon Type\
dataType: weapon\_type

pinId: Secondary Weapon Type\
dataType: weapon\_type

pinId: Apply Immediately\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Apply Immediately\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Apply Immediately\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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
userData:

#### Node Category: Unused\

</details>

<details>
<summary>Override Loadouts For Player</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Player

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Equipment Type\
dataType: equipment\_type

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Charge Count\
dataType: number\
MinRange: -99\
MaxRange: 99\
Step: 1.0

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Charge Count\
dataType: number\
MinRange: 0\
MaxRange: 99\
Step: 1.0

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Team\
dataType: team

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Penalty Seconds\
dataType: number\
MinRange: 0\
Step: 1

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Spawn Point

pinId: Enabled\
dataType: bool\
settings: defaultValue: Bool: true

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Respawn Message\
dataType: respawn\_message

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Target Object

pinId: Bot Ambition\
dataType: forge\_bot\_ambition

pinId: Team\
dataType: team\
settings: defaultValue: String: nil

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Target Object

pinId: Only Specific Ambition Type\
dataType: bool\
settings: defaultValue: Bool: true

pinId: Ambition Type\
dataType: bot\_ambition\_type\
settings: defaultValue: String: nil

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Team\
dataType: team\
settings: defaultValue: String: nil

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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
userData:

#### Node Category: Bots\

</details>

<details>
<summary>Remove Specific Bot From Match</summary>

### Node Rules
ruleID: RequiredNodeInput\
RequiredProperties: Bot Player

### Input Pins
pinId: ActionStart\
dataType: execute

pinId: Bot Player

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Override Enabled\
dataType: bool

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Object

pinId: Position\
dataType: vector3

pinId: Duration in Seconds\
dataType: number\
MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in\
settings: defaultValue: String: CURVE\_BUILT\_IN.None

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Object

pinId: Rotation\
dataType: vector3

pinId: Duration in Seconds\
dataType: number\
MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in\
settings: defaultValue: String: CURVE\_BUILT\_IN.None

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Object

pinId: Destination Object

pinId: Duration in Seconds\
dataType: number\
MinRange: 0

pinId: Movement Curve\
dataType: curve\_built\_in

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Player

pinId: Enabled\
dataType: bool\
settings: defaultValue: Bool: true

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Weapon

pinId: Rounds\
dataType: number\
MinRange: 0\
Step: 1

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Weapon

pinId: Magazine Rounds\
dataType: number\
MinRange: 0\
Step: 1

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Weapon

pinId: Percent\
dataType: number\
MinRange: 0\
MaxRange: 100\
Step: 1

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Audio Zone Effect\
dataType: forge\_audio\_zone\_effect

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Zone

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Zone

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

pinId: Start Immediately\
dataType: bool\
settings: defaultValue: Bool: false

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

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

### Output Pins
pinId: ActionComplete\
dataType: execute
userData:

#### Node Category: Stopwatches
</details>

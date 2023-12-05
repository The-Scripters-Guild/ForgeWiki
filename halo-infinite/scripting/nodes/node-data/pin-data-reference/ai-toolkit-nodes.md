# AI Toolkit Nodes

<details>

<summary>Declare Encounter Variable</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Initial Value\
dataType: encounter

#### Editor Settings

defaultValue: String: nil

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Get Encounter Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

pinId: Object\
dataType: object\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: Out\
dataType: encounter\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Set Encounter Variable Storage\ Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Value\
dataType: encounter\
defaultValue: String: nil

#### Editor Settings

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

pinId: Object\
dataType: object\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Declare Squad Specification Variable</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Initial Value\
dataType: squad\_specification

#### Editor Settings

defaultValue: String: nil

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Get Squad Specification Variable Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

pinId: Object\
dataType: object\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: Out\
dataType: squad\_specification\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Set Squad Specification Variable Storage\ Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Identifier\
Scope

pinId: ActionStart\
dataType: execute

pinId: Identifier\
dataType: identifier

#### Editor Settings

pinId: Value\
dataType: squad\_specification\
defaultValue: String: nil

#### Editor Settings

pinId: Scope\
dataType: forge\_variable\_scope

#### Editor Settings

pinId: Object\
dataType: object\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\_Variables\\

</details>

<details>

<summary>Create Encounter Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Area Object\
Identifier

pinId: ActionStart\
dataType: execute

pinId: Area Object\
dataType: object

#### Editor Settings

pinId: Identifier\
dataType: identifier

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Squad Follow Player Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Player

pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

#### Editor Settings

pinId: Player\
dataType: object

#### Editor Settings

properties: propertyName: Radius\
dataType: number\
defaultValue: Float: 50.0

MinRange: 10.0\
MaxRange: 100.0\
Step: 1.0

#### Editor Settings

propertyName: Refresh Distance\
dataType: number\
defaultValue: Float: 30.0

MinRange: 10.0\
MaxRange: 100.0\
Step: 1.0

#### Editor Settings

propertyName: Refresh Time\
dataType: number\
defaultValue: Float: 5.0

MinRange: 1.0\
MaxRange: 30.0\
Step: 1.0

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Squad Follow Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object\
Squad

pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

#### Editor Settings

pinId: Object\
dataType: object

#### Editor Settings

properties: propertyName: Radius\
dataType: number\
defaultValue: Float: 50.0

MinRange: 10.0\
MaxRange: 100.0\
Step: 1.0

#### Editor Settings

propertyName: Refresh Distance\
dataType: number\
defaultValue: Float: 30.0

MinRange: 10.0\
MaxRange: 100.0\
Step: 1.0

#### Editor Settings

propertyName: Refresh Time\
dataType: number\
defaultValue: Float: 5.0

MinRange: 1.0\
MaxRange: 30.0\
Step: 1.0

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Squad Go To Position Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Position

pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

#### Editor Settings

pinId: Position\
dataType: vector3

#### Editor Settings

pinId: Radius\
dataType: number\
defaultValue: Float: 50.0

MinRange: 10.0\
MaxRange: 100.0\
Step: 1.0

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Spawn Squad Storage</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: SquadSpawnDefinition

pinId: ActionStart\
dataType: execute

pinId: SquadSpawnDefinition\
dataType: ai\_squad\_definition

#### Editor Settings

pinId: Identifier\
dataType: identifier\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Assign Squad To Encounter Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Squad\
Encounter

pinId: ActionStart\
dataType: execute

pinId: Squad\
dataType: ai\_squad

#### Editor Settings

pinId: Encounter\
dataType: encounter

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Assign Object to Team Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Target

pinId: ActionStart\
dataType: execute

pinId: Target\
dataType: object

#### Editor Settings

pinId: Team\
dataType: team\
defaultValue: String: nil

#### Editor Settings

pinId: Bias\
dataType: number\
defaultValue: String: nil

#### Editor Settings

MinRange: -1.0\
MaxRange: 1.0\
Step: 0.1

pinId: Targetable Object Overrides\
dataType: targetable\_object\_overrides\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: ActionComplete\
dataType: execute

userData:

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Brute GeneralpinId: Character Type<br>dataType: ai_brute_character_type<br>defaultValue: String: AICharacterTypeIdTable.brute_minorEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: brute<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Brute Officer GeneralpinId: Character Type<br>dataType: ai_brute_officer_character_type<br>defaultValue: String: AICharacterTypeIdTable.brute_captainEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: brute_officer<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Brute Chieftain GeneralpinId: Character Type<br>dataType: ai_brute_chieftain_character_type<br>defaultValue: String: AICharacterTypeIdTable.brute_chieftanEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: brute_chieftain<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Grunt GeneralpinId: Character Type<br>dataType: ai_grunt_character_type<br>defaultValue: String: AICharacterTypeIdTable.grunt_conscript_aEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: grunt<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Elite GeneralpinId: Character Type<br>dataType: ai_elite_character_type<br>defaultValue: String: AICharacterTypeIdTable.elite_mercenaryEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: elite<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Hunter GeneralpinId: Character Type<br>dataType: ai_hunter_character_type<br>defaultValue: String: AICharacterTypeIdTable.hunterEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: hunter<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Jackal GeneralpinId: Character Type<br>dataType: ai_jackal_character_type<br>defaultValue: String: AICharacterTypeIdTable.jackal_freebooterEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: jackal<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Marine GeneralpinId: Character Type<br>dataType: ai_marine_character_type<br>defaultValue: String: AICharacterTypeIdTable.marine_assaultEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: marine<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Skimmer GeneralpinId: Character Type<br>dataType: ai_skimmer_character_type<br>defaultValue: String: AICharacterTypeIdTable.skimmerEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: skimmer<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Sentinel Boss GeneralpinId: Character Type<br>dataType: ai_sentinel_boss_character_type<br>defaultValue: String: AICharacterTypeIdTable.adjutant_resolution_spireEditor SettingsOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: sentinel_boss<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Harbinger GeneralOutput PinspinId: Character Specification<br>dataType: character_specification<br>labels: inquisitor<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Characters\</summary>



</details>

<details>

<summary>Characters For Squad GeneralpinId: Entry1<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Squad Specification<br>dataType: squad_specification<br>labels: character_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Characters For Drop Pods GeneralpinId: Entry1<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Squad Specification<br>dataType: squad_specification<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>General Characters For Phantom GeneralpinId: Entry1<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Squad Specification<br>dataType: squad_specification<br>labels: phantom_general_passenger_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Large Characters For Phantom GeneralpinId: Entry1<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Phantom Large Passengers<br>dataType: squad_specification<br>labels: phantom_general_passenger_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Characters Groups For Phantom GeneralpinId: Entry1<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Phantom Passengers<br>dataType: squad_specification<br>labels: phantom_full_passenger_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Vehicle Cargo For Phantom GeneralpinId: Large Cargo<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingspinId: Small Cargo 1<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingspinId: Small Cargo 2<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Phantom Vehicle Cargo<br>dataType: squad_specification<br>labels: phantom_vehicle_cargo_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Loadout For Phantom GeneralpinId: Phantom Passengers<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Phantom Vehicle Cargo<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Phantom Passengers Out<br>dataType: squad_specification<br>labels: phantom_full_loadout<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Ghost GeneralpinId: Driver<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Config<br>dataType: number<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Vehicle Specification Entry<br>dataType: vehicle_specification<br>labels: small_vehicle<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Vehicles\</summary>



</details>

<details>

<summary>Wraith GeneralpinId: Driver<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Gunner<br>dataType: character_specification<br>defaultValue: String: nilEditor SettingspinId: Config<br>dataType: number<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Vehicle Specification Entry<br>dataType: vehicle_specification<br>labels: large_vehicle<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit_Vehicles\</summary>



</details>

<details>

<summary>Vehicles For Squad GeneralpinId: Entry1<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: vehicle_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Squad Specification<br>dataType: squad_specification<br>labels: vehicle_group<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Merge Squad Specifications GeneralpinId: Entry1<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry2<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry3<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingspinId: Entry4<br>dataType: squad_specification<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Squad Specification<br>dataType: squad_specification<br>labels: full_squad_specification<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Build Squad Spawn Definition General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Encounter\
Team\
Squad Specification

pinId: Encounter\
dataType: encounter

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

pinId: Squad Specification\
dataType: squad\_specification

#### Editor Settings

pinId: Spawn Overrides\
dataType: spawn\_overrides\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: AI Squad Definition\
dataType: ai\_squad\_definition\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Drop Pod Spawn Settings GeneralpinId: Spawn Time Window<br>dataType: number<br>defaultValue: Float: 3.0Editor SettingspinId: Spawn Overrides<br>dataType: spawn_overrides<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Drop Pod Spawn Settings<br>dataType: drop_pod_spawn_settings<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Build Drop Pod Squad Spawn Definition General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Encounter\
Team\
Squad Specification\
Drop Pod Spawn Settings

pinId: Encounter\
dataType: encounter

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

pinId: Squad Specification\
dataType: squad\_specification

#### Editor Settings

pinId: Drop Pod Spawn Settings\
dataType: drop\_pod\_spawn\_settings

#### Editor Settings

### Output Pins

pinId: AI Squad Definition\
dataType: ai\_squad\_definition\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Build Phantom Air Drop Squad Spawn Definition General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Encounter\
Team\
Squad Specification\
Phantom Air Drop Settings

pinId: Encounter\
dataType: encounter

#### Editor Settings

pinId: Team\
dataType: team

#### Editor Settings

pinId: Squad Specification\
dataType: squad\_specification

#### Editor Settings

pinId: Phantom Air Drop Settings\
dataType: phantom\_air\_drop\_settings

#### Editor Settings

### Output Pins

pinId: AI Squad Definition\
dataType: ai\_squad\_definition\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Phantom Air Drop Settings General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Location

pinId: Location\
dataType: object

#### Editor Settings

pinId: Phantom Air Drop Ship Modifiers\
dataType: phantom\_air\_drop\_ship\_modifiers\
defaultValue: String: nil

#### Editor Settings

pinId: Phantom Air Drop Drop Modifiers\
dataType: phantom\_air\_drop\_drop\_modifiers\
defaultValue: String: nil

#### Editor Settings

pinId: Spawn Behavior Overrides\
dataType: spawn\_behavior\_overrides\
defaultValue: String: nil

#### Editor Settings

### Output Pins

pinId: Phantom Air Drop Settings\
dataType: phantom\_air\_drop\_settings\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Phantom Air Drop Drop Modifiers GeneralpinId: Initial Combat State<br>dataType: actor_basic_combat_status<br>defaultValue: String: nilEditor SettingspinId: Passenger Seat Preference<br>dataType: air_drop_passenger_seat_preference<br>defaultValue: Enumerable: PASSENGER_SEAT_PREFERENCE.BothEditor SettingspinId: Passenger Drop Height<br>dataType: number<br>defaultValue: Float: 2.0Editor SettingspinId: Vehicle Drop Height<br>dataType: number<br>defaultValue: Float: 2.0Editor SettingsOutput PinspinId: Phantom Air Drop Drop Modifiers<br>dataType: phantom_air_drop_drop_modifiers<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Phantom Air Drop Ship Modifiers GeneralpinId: Chin Gun Present<br>dataType: bool<br>defaultValue: Bool: trueEditor SettingspinId: Side Gunner Type<br>dataType: phantom_side_gunner<br>defaultValue: String: nilEditor SettingspinId: Attack After Drop Duration<br>dataType: number<br>defaultValue: Float: 0.0Editor SettingsOutput PinspinId: Phantom Air Drop Ship Modifiers<br>dataType: phantom_air_drop_ship_modifiers<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Spawn Behavior Overrides GeneralpinId: Braindead<br>dataType: bool<br>defaultValue: Bool: falseEditor SettingspinId: Blind<br>dataType: bool<br>defaultValue: Bool: falseEditor SettingspinId: Deaf<br>dataType: bool<br>defaultValue: Bool: falseEditor SettingspinId: Magic Sight<br>dataType: bool<br>defaultValue: Bool: falseEditor SettingsOutput PinspinId: Spawn Behavior Overrides<br>dataType: spawn_behavior_overrides<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Spawn At Location General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Location

pinId: Location\
dataType: object

#### Editor Settings

pinId: Radius\
dataType: number\
defaultValue: Float: 1.0

#### Editor Settings

### Output Pins

pinId: Spawn Location Override\
dataType: spawn\_location\_override\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Spawn In Area General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Area Object

pinId: Area Object\
dataType: object

#### Editor Settings

### Output Pins

pinId: Spawn Location Override\
dataType: spawn\_location\_override\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Spawn Overrides GeneralpinId: Initial Combat State<br>dataType: actor_basic_combat_status<br>defaultValue: String: nilEditor SettingspinId: Initial Facing<br>dataType: number<br>defaultValue: String: nilEditor SettingspinId: Spawn Location Override<br>dataType: spawn_location_override<br>defaultValue: String: nilEditor SettingspinId: Spawn Behavior Overrides<br>dataType: spawn_behavior_overrides<br>defaultValue: String: nilEditor SettingsOutput PinspinId: Spawn Overrides<br>dataType: spawn_overrides<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Targetable Object Overrides GeneralpinId: Vehicle Targetable<br>dataType: bool<br>defaultValue: String: nilEditor SettingspinId: Grenade Targetable<br>dataType: bool<br>defaultValue: String: nilEditor SettingspinId: Minimum Range<br>dataType: number<br>defaultValue: String: nilEditor SettingsMinRange: 0.0<br>MaxRange: 20.0<br>Step: 0.5Editor SettingspinId: Maximum Range<br>dataType: number<br>defaultValue: String: nilEditor SettingsMinRange: 0.0<br>MaxRange: 20.0<br>Step: 0.5Editor SettingsOutput PinspinId: Targetable Object Overrides<br>dataType: targetable_object_overrides<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Is Object AI Targetable General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Object

pinId: Object\
dataType: object

#### Editor Settings

### Output Pins

pinId: Is Targetable\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Unused\_AIToolkit\\

</details>

<details>

<summary>Get Current AI Targetable Object Count GeneralOutput PinspinId: Count<br>dataType: number<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Max AI Targetable Objects GeneralOutput PinspinId: Count<br>dataType: number<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

<details>

<summary>Get AI Targetable Objects GeneralOutput PinspinId: Count<br>dataType: object_list<br>userData:Editor SettingsEditor SettingsNode Category: Unused_AIToolkit\</summary>



</details>

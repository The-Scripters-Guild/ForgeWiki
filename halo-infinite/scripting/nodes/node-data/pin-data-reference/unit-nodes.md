# Unit Nodes

<details>

<summary>Teleport Unit</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Position

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

**Editor Settings**

pinId: Position\
dataType: vector3

**Editor Settings**

pinId: Teleport Unit's Vehicle\
dataType: bool\
settings: defaultValue: Bool: true

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Are Same Unit</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit A\
Unit B

#### Input Pins

pinId: Unit A\
dataType: object

**Editor Settings**

pinId: Unit B\
dataType: object

**Editor Settings**

#### Output Pins

pinId: Are Same Unit\
dataType: bool\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get All Units</summary>

#### Output Pins

pinId: Units\
dataType: object\_list\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get All Units On Team</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Team

#### Input Pins

pinId: Team\
dataType: team

**Editor Settings**

#### Output Pins

pinId: Units\
dataType: object\_list\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get Random Unit</summary>

#### Output Pins

pinId: Unit\
dataType: object\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get Unit Aiming Vector</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object

**Editor Settings**

#### Output Pins

pinId: Aiming Vector\
dataType: vector3\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get Unit Team</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object

**Editor Settings**

#### Output Pins

pinId: Team\
dataType: team\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get Unit FFA Allegiance</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object

**Editor Settings**

#### Output Pins

pinId: Team\
dataType: team\
userData:

**Editor Settings**

#### Node Category: Units\\

</details>

<details>

<summary>Get Unit Weapons</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit

#### Input Pins

pinId: Unit\
dataType: object

**Editor Settings**

#### Output Pins

pinId: Equipped Weapon\
dataType: object\
userData:

**Editor Settings**

pinId: Unequipped Weapon\
dataType: object\
userData:

**Editor Settings**

#### Node Category: Inventory\\

</details>

<details>

<summary>Give Unit New Weapon</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Weapon Type\
Weapon Addition Method

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

**Editor Settings**

pinId: Weapon Type\
dataType: weapon\_type

**Editor Settings**

pinId: Weapon Addition Method\
dataType: weapon\_addition\_method

**Editor Settings**

pinId: Wait Until Completion\
dataType: bool\
settings: defaultValue: Bool: true

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Inventory\\

</details>

<details>

<summary>Give Unit Specific Weapon</summary>

####

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Weapon\
Weapon Addition Method

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

**Editor Settings**

pinId: Weapon\
dataType: object

**Editor Settings**

pinId: Weapon Addition Method\
dataType: weapon\_addition\_method

**Editor Settings**

pinId: Wait Until Completion\
dataType: bool\
settings: defaultValue: Bool: true

**Editor Settings**

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Inventory\\

</details>

<details>

<summary>Set Unit Camo</summary>

#### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Unit\
Duration in Seconds

#### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Unit\
dataType: object

**Editor Settings**

pinId: Duration in Seconds\
dataType: number

**Editor Settings**

MinRange: 0\
MaxRange: 20

#### Output Pins

pinId: ActionComplete\
dataType: execute userData:

**Editor Settings**

#### Node Category: Units\\

</details>

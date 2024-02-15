# Generic Nodes

<details>

<summary>Add Item to Generic List</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

pinId: Any Item\
dataType: any

### Editor Settings

pinId: Allow Duplicates\
dataType: bool\
settings: defaultValue: String: false

### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Remove Item From Generic List</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

pinId: Any Item\
dataType: any

### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Combine Generic Lists</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

### Editor Settings

pinId: List B\
dataType: any

### Editor Settings

pinId: Allow Duplicates\
dataType: bool\
settings: defaultValue: String: false

### Editor Settings

### Output Pins

pinId: Combined Generic List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Get Shared Items</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

### Editor Settings

pinId: List B\
dataType: any

### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Get Unshared Items</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

### Editor Settings

pinId: List B\
dataType: any

### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>For Each Generic Item</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Generic List\
dataType: any

### Editor Settings

### Output Pins

pinId: On Loop Complete\
dataType: execute

### Editor Settings

pinId: Execute Per Generic Item\
dataType: execute

### Editor Settings

pinId: Current Generic Item\
dataType: generic\_item

### Editor Settings

userData:

pinId: Current Index\
dataType: number

### Editor Settings

userData: userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Get N Items From Generic List</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
N\
N Type

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

pinId: N\
dataType: number

### Editor Settings

MinRange: 0\
Step: 1.0

pinId: N Type\
dataType: generic\_item\_count\_type

### Editor Settings

### Output Pins

pinId: New List\
dataType: generic\_list\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Get Item at Index</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Index

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

pinId: Index\
dataType: number

### Editor Settings

MinRange: 1\
Step: 1.0

### Output Pins

pinId: Generic Item\
dataType: generic\_item\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Get Generic List Size</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

### Output Pins

pinId: Size\
dataType: number\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Item Is In Generic List</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

### Editor Settings

pinId: Any Item\
dataType: any

### Editor Settings

### Output Pins

pinId: Contains Item\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\
</details>

<details>

<summary>Cast to Number</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Number\
dataType: number\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Bool</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Boolean\
dataType: bool\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Object</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Object\
dataType: object\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Team</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Team\
dataType: team\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Vector</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Vector\
dataType: vector3\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to UI Message</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: UI Message\
dataType: ui\_message\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to String</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: String\
dataType: string\_id\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Grenade Type</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Grenade Type\
dataType: grenade\_type\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Equipment Type</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Equipment Type\
dataType: equipment\_type\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Vehicle Type</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Vehicle Type\
dataType: vehicle\_type\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Weapon Type</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Weapon Type\
dataType: weapon\_type\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to User Label</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: User Label\
dataType: user\_label\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Squad Definition</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Squad Definition\
dataType: ai\_squad\_definition\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Squad</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Squad\
dataType: ai\_squad\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Wave</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Wave\
dataType: ai\_wave\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

<details>

<summary>Cast to Wave Manager</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

### Editor Settings

### Output Pins

pinId: Wave Manager\
dataType: ai\_wave\_manager\
userData:

### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

### Editor Settings

#### Node Category: Generic\_Lists\_Casts\
</details>

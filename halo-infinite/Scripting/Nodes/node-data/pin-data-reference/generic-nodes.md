# Generic Nodes

<details>

<summary>Add Item to Generic List nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

pinId: Any Item\
dataType: any

#### Editor Settings

pinId: Allow Duplicates\
dataType: bool\
settings: defaultValue: String: false

#### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Remove Item From Generic List nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

pinId: Any Item\
dataType: any

#### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Combine Generic Lists nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

#### Editor Settings

pinId: List B\
dataType: any

#### Editor Settings

pinId: Allow Duplicates\
dataType: bool\
settings: defaultValue: String: false

#### Editor Settings

### Output Pins

pinId: Combined Generic List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Get Shared Items nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

#### Editor Settings

pinId: List B\
dataType: any

#### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Get Unshared Items nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: List A\
List B

### Input Pins

pinId: List A\
dataType: any

#### Editor Settings

pinId: List B\
dataType: any

#### Editor Settings

### Output Pins

pinId: New Generic List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>For Each Generic Item nodeCategories: Function</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List

### Input Pins

pinId: ActionStart\
dataType: execute

pinId: Generic List\
dataType: any

#### Editor Settings

### Output Pins

pinId: On Loop Complete\
dataType: execute

#### Editor Settings

pinId: Execute Per Generic Item\
dataType: execute

#### Editor Settings

pinId: Current Generic Item\
dataType: generic\_item

#### Editor Settings

userData:

pinId: Current Index\
dataType: number

#### Editor Settings

userData: userData:

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Get N Items From Generic List nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
N\
N Type

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

pinId: N\
dataType: number

#### Editor Settings

MinRange: 0\
Step: 1.0

pinId: N Type\
dataType: generic\_item\_count\_type

#### Editor Settings

### Output Pins

pinId: New List\
dataType: generic\_list\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Get Item at Index nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Index

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

pinId: Index\
dataType: number

#### Editor Settings

MinRange: 1\
Step: 1.0

### Output Pins

pinId: Generic Item\
dataType: generic\_item\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Get Generic List Size nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

### Output Pins

pinId: Size\
dataType: number\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Item Is In Generic List nodeCategories: General</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic List\
Any Item

### Input Pins

pinId: Generic List\
dataType: any

#### Editor Settings

pinId: Any Item\
dataType: any

#### Editor Settings

### Output Pins

pinId: Contains Item\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\\

</details>

<details>

<summary>Cast to Number nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Number\
dataType: number\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Bool nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Boolean\
dataType: bool\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Object nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Object\
dataType: object\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Team nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Team\
dataType: team\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Vector nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Vector\
dataType: vector3\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to UI Message nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: UI Message\
dataType: ui\_message\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to String nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: String\
dataType: string\_id\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Grenade Type nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Grenade Type\
dataType: grenade\_type\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Equipment Type nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Equipment Type\
dataType: equipment\_type\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Vehicle Type nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Vehicle Type\
dataType: vehicle\_type\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Weapon Type nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Weapon Type\
dataType: weapon\_type\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to User Label nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: User Label\
dataType: user\_label\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Squad Definition nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Squad Definition\
dataType: ai\_squad\_definition\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Squad nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Squad\
dataType: ai\_squad\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Wave nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Wave\
dataType: ai\_wave\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

<details>

<summary>Cast to Wave Manager nodeCategories: General\ Cast</summary>

### Node Rules

ruleID: RequiredNodeInput\
RequiredProperties: Generic Item

### Input Pins

pinId: Generic Item\
dataType: generic\_item

#### Editor Settings

### Output Pins

pinId: Wave Manager\
dataType: ai\_wave\_manager\
userData:

#### Editor Settings

pinId: Cast Succeeded\
dataType: bool\
userData:

#### Editor Settings

#### Editor Settings

#### Node Category: Generic\_Lists\_Casts\\

</details>

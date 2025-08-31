---
description: >-
  Documentation about the features and usage of the tsg radial template used to
  create Radial Menus.
---

# tsg radial

<figure><img src="../../../.gitbook/assets/cover-tsg-radial.png" alt="The tsg hackSwitch prefab and all of the included objects"><figcaption></figcaption></figure>

`tsg radial` is a scripting module template that simplifies the creation of Radial Menus. The method used for creating the Radial Menus is efficient and allows for intuitive navigation between multiple categories or even separate Radial Modules.

Bookmark the mode prefab below or find the it through the in-game UGC browser by searching with keywords or tags.

{% embed url="https://www.halowaypoint.com/halo-infinite/ugc/modes/97d0add6-f022-4b5e-bba9-622f34f47686" %}



## Features

A showcase of the radial menu template features and how to modify them to suit your Radial Menu.

### Opening a Menu

In `tsg radial` a Menu is opened by calling a `Custom Event, Global` associated with the desired Menu. The standard for opening Radial Menus is either with the Custom Input key, or by interacting with a switch on the level.

<div><figure><img src="../../../.gitbook/assets/radial-opening.png" alt=""><figcaption><p>Triggers and Events for opening Menus</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-main.png" alt=""><figcaption><p>An example menu</p></figcaption></figure></div>

{% hint style="info" %}
The Custom Event, Global Async `On Custom Input Tap` serves the same purpose as the node with the same name, but is a workaround for a bug. The source of Custom Event can be seen in the [initialization events](tsg-radial.md#initialization-events-and-declarations).
{% endhint %}

The events for opening a Menu rely on the following parameters:

* **Identifier**: A custom name for the event; suggested to use the naming pattern: `radial{Digit 1}_{category}` as it helps you keep track of what radial belongs where
* **Object**: The player who the Menu should be shown to
* **Number**: A 4-digit number value containing information about the Menu; used for determining which menu to return to when navigating backwards
  * **Digit 1**: Radial Module
  * **Digit 2**: Radial Category
  * **Digit 3**: Radial Page
  * **Digit 4**: Menu Item

Having these number values consistent between all Custom Events that open Menus is crucial for the script module to function correctly.

<div><figure><img src="../../../.gitbook/assets/radial-opening-event1.png" alt=""><figcaption><p>Value 1000 = main radial of the 1st Radial Module</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-opening-event2.png" alt=""><figcaption><p>Value 2203 = 3rd Menu Item from the 2nd category of the 2nd Radial Module</p></figcaption></figure></div>

{% hint style="info" %}
The 4th digit is only used if selecting the Menu Item takes you to an extra Radial Menu that has no more navigation beyond it, such as a selection for which Team's bot to remove.
{% endhint %}

### Menu creation

Each menu in `tsg radial` is built right before the menu is shown to the player. This way the most updated information can be shown on the menu, and the code used for creating the menu is all in the same place for efficiency.

<figure><img src="../../../.gitbook/assets/radial-main-code.png" alt=""><figcaption><p>Code for a building, showing and logging a Menu</p></figcaption></figure>

#### Menu Items

Radial Menus consist of a maximum 8 Menu Items (selectable sectors) per Menu, which each must be declared in the code so display the desired Title, Description, Icon and Enabled state. The Title and Description utilize a `Create UI Message` node, and the Icon and Enabled state are set by opening the properties of the `Menu Item` node.

<figure><img src="../../../.gitbook/assets/menu-item-properties.png" alt=""><figcaption><p>Menu Item node properties showing options for setting the Enabled state and Icon</p></figcaption></figure>

Each Menu Item is fed into a `Generic List` running through a `For Each Generic Item` loop that adds each Menu Item to the Menu at the index where it shows up in the Generic List. A blank Menu Item can be created by picking a new Menu Item node, leaving the Icon selection as empty, and making the Enabled state False.

<div><figure><img src="../../../.gitbook/assets/empty-menu-item-code.png" alt=""><figcaption><p>Code for creating five blank Menu Items in a Menu</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-empty-menu-item.png" alt=""><figcaption><p>Menu Items 4-8 showing as blank and unselectable</p></figcaption></figure></div>

#### Menu Variables

Menu Variables are the core of each Menu. These must be declared via the `Declare Menu Variable` node before Menu Items can be assigned to them.

The Menu Variables follow these parameters:

* **Identifier**: A custom name for the Menu; suggested to use the exact same naming pattern: `radial{Digit 1}_{category}` as used for the `Custom Event, Global` for creating the Menu as it's more streamlined
* **Scope**: Global
  * Optimally object-scope should be used for player-based menus, but a current bug is preventing object-scoped menus from functioning correctly

<div><figure><img src="../../../.gitbook/assets/declare-menu-variable-example.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/get-menu-variable-example.png" alt=""><figcaption></figcaption></figure></div>

#### Displaying the Menu

After the menu has been built, it's shown to the player in that state using the `Show Menu To Player` node. With `tsg radial` if another player opens the same menu shortly after with their own building parameters, the previous player's Menu will not be affected.

<div><figure><img src="../../../.gitbook/assets/show-menu-to-player-example.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-main.png" alt=""><figcaption></figcaption></figure></div>

#### Logging the Menu

After a Menu is displayed to a player, its Number value is stored at the end of a Generic List named `previousMenuValues`. This list is used to look up previous Menus the player has been shown to determine which Menu to navigate back to when closing a Menu. This custom Menu history tracking allows for complex nested Menus to feel intuitive navigating in and out from.

Also a Boolean Variable `radialOpen` is set to True, which is used elsewhere to track whether the player has a Menu open or not, as this is not natively tracked.

<figure><img src="../../../.gitbook/assets/tsg-radial-logMenu.png" alt=""><figcaption><p>Logging the Menu Number value in a Generic List</p></figcaption></figure>

{% hint style="info" %}
Extra code for a bug workaround is appended to the function that may become unnecessary in the future.
{% endhint %}



### Menu forwards navigation

The Menu can be navigated with the controller movement stick, mouse movement, or keyboard WASD keys and various inputs for selecting the Menu Items. Selecting a Menu Item will take you to a separate Menu or result in an action such as being granted a weapon.

<div><figure><img src="../../../.gitbook/assets/radial-main-select.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-weapons-select.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-weapons2-select.png" alt=""><figcaption></figcaption></figure></div>

#### Menu Item selection

When a Menu Item is selected, a comparison is done to determine which menu the selection was made from. If the Menu where a selection made matches a Menu in the comparison tree, a `Custom Event, Global` is fired with data that is used to determine which item was selected.

Also a Boolean Variable `radialOpen` is set to False, which is used elsewhere to track whether the player has a Menu open or not, as this is not natively tracked.

<figure><img src="../../../.gitbook/assets/menu-item-selected-code1.png" alt=""><figcaption><p>Comparison tree determining which Menu a selection was made in</p></figcaption></figure>

The reason why the `On Menu Item Selected` node is immediately being turned into a Custom Event, Global is so the comparison tree can be continued on another Script Brain. Below is an example on how to do so:

<div><figure><img src="../../../.gitbook/assets/menu-selection-continue1.png" alt=""><figcaption><p>Continuing the Menu selection comparison tree. The Object and Number connections come from the <code>On Menu Item Selected</code> Custom Event.</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/menu-selection-continue2.png" alt=""><figcaption><p>Continued Menu selection comparison tree</p></figcaption></figure></div>

The event for the item selection relies on the following parameters:

* **Identifier**: A custom name for the event; suggested to use nearly the same naming pattern: `radial{Digit 1}_{category}-select` as used for the `Get Menu Variable` for comparing the Menu as it's more streamlined
* **Object**: Player who made the Menu Item selection
* **Number**: The index of the selected Menu Item

<figure><img src="../../../.gitbook/assets/menu-item-selection-event.png" alt=""><figcaption></figcaption></figure>

#### Selection event

The filtered selection event leads into a function that determines what to do based on which index Menu Item was selected. The function uses a simple comparison tree with an optimized amount of Compare nodes to cover all values from 1-8. Comparing for 8 values is not necessary if the menu contains less selectable Menu Items to begin with.

{% hint style="info" %}
The value 0 is also in the comparison, which is used for backwards navigation purposes as the same event is reused there to determine which Menu to return to.
{% endhint %}

<div><figure><img src="../../../.gitbook/assets/radial-main-select-code.png" alt=""><figcaption><p>Main radial selection event leading to 8 different categories</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-example1-select-code.png" alt=""><figcaption><p>Category 1 selection event with weapon grants and a link to the 2nd page</p></figcaption></figure></div>

<figure><img src="../../../.gitbook/assets/radial-example1-1-select-code.png" alt=""><figcaption><p>Category 1, Page 1 selection event with weapon grants and a final Menu Item selection radial</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/radial-heatwave-select-code.png" alt=""><figcaption><p>Menu Item selection radial</p></figcaption></figure>



### Menu backwards navigation

`tsg radial` has a custom [menu history system](tsg-radial.md#logging-the-menu) where closing a Menu by pressing the Cancel button in the center of each radial will take you to the previous Menu you were in. This feature can be disabled if necessary, but is a very useful feature in large menus with multiple categories.

<div><figure><img src="../../../.gitbook/assets/radial-weapons1.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-weapons.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-main.png" alt=""><figcaption></figcaption></figure></div>

#### Menu closing filter

When a Menu is closed, the custom value of the closed Menu is removed from the `previousMenuValues` list, and it's checked whether the last item in the list is a valid number. If so, the 4-digit number value is filtered through various checks in order to open the correct Menu for the player. This Menu would be the previous Menu the player had been in.

**Digit 1** is filtered to determine which Radial Module the Menu belongs in, and a `Custom Event, Global` corresponding to the Radial Module is fired. Radial Modules are meant to represent entirely different Radial Menus, each with their own set of nested Menus for example. The 4-digit Menu logging system in `tsg radial` supports 9 separate Radial Modules which should be plenty.

<figure><img src="../../../.gitbook/assets/radial-close-filter1-code.png" alt=""><figcaption><p>Filter for determining the Radial Module of the Menu that should be returned to</p></figcaption></figure>

The event for the Menu filtering relies on the following parameters:

* **Identifier**: A custom name for the event; suggested to use the naming pattern: `menuClose_radial{Digit 1}` as it helps you keep track of which Radial Module is being processed
* **Object**: Player who closed the Menu
* **Number**: The remaining 3-digit number value after the first filtered value has been excluded

<figure><img src="../../../.gitbook/assets/radial-closing-event.png" alt=""><figcaption></figcaption></figure>

Then the second, third and fourth digits are filtered to determine the exact Menu that should be shown to the player.

* **Digit 2** determines the Radial Category. If the desired Menu has no nested menus, the [Selection event](tsg-radial.md#selection-event) for that Menu is fired with **Digit 4** fed into the Number value of the event.
* **Digit 3** determines the Radial Page. If the desired Menu has a nested menu, a branch is created that compares which page matches the comparison. The same Selection event for the desired Menu is fired as before.
* **Digit 4** determines the Menu Item or the Menu itself. In this pattern this value is usually 0, which is used in the Selection event only for this purpose to return the desired Menu to the player.

<div><figure><img src="../../../.gitbook/assets/radial-close-filter2-code.png" alt=""><figcaption><p>Filter for determining the Menu that should be returned to from Radial Module 1</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-close-filter3-code.png" alt=""><figcaption><p>Filter for determining the Menu that should be returned to from Radial Module 2</p></figcaption></figure></div>

Here's an example following how the value `110` is filtered:

<figure><img src="../../../.gitbook/assets/radial-close-filter2-code-example.png" alt=""><figcaption><p>Highlighted connections that are used when the Number <code>110</code> is processed in the Menu filtering event</p></figcaption></figure>

{% hint style="info" %}
**Note:** The Number `110` started as `1110` before having **Digit 1** removed when fed into this Custom Event.
{% endhint %}



## Background events

The essential background events that serve as the foundation for some features of `tsg radial`. These events should be left untouched when using the scripting module.

### Initialization events and declarations

Custom Events created to ensure smooth timing and predictable execution of the rest of the code.

<figure><img src="../../../.gitbook/assets/tsg-radial-init.png" alt=""><figcaption><p>Initialization events</p></figcaption></figure>

Declarations for all variables and traits in one place. More variable declarations are needed when new Menu Variables are used.

<figure><img src="../../../.gitbook/assets/tsg-radial-declarations.png" alt=""><figcaption><p>Variable and trait declarations</p></figcaption></figure>

### Menu state events

Essential events for tracking if a player has a Menu open, logging the menu values, and ways of forcefully closing the menu.

<div><figure><img src="../../../.gitbook/assets/tsg-radial-radialOpen.png" alt=""><figcaption><p>Menu state tracking</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/tsg-radial-forceClose.png" alt=""><figcaption><p>Fallback for closing the Menu by changing the aim rotation</p></figcaption></figure></div>

<div><figure><img src="../../../.gitbook/assets/tsg-radial-logMenu.png" alt=""><figcaption><p>Logging the Menu Number value and applying a bug workaround</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/tsg-radial-closeMenu.png" alt=""><figcaption><p>Forceful closing of the player's current Menu</p></figcaption></figure></div>



## Example setups

Examples of using `tsg radial` to make various types of Menus.

### Value update on Menu open

Object-based values can be fed into the `Create UI Message` nodes in order to alter what values show up in the Menu messages. These values update each time the event is called to open the Menu.

This Menu example also features a button-like Menu Item that reopens the same Menu after selecting the Menu Item at index 1 so the same Menu Item can be quickly pressed multiple times.

<figure><img src="../../../.gitbook/assets/radial-playerDamage-code.png" alt=""><figcaption><p>Pulling the player's health and shield values to be used in the Description of Menu Items</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/radial-playerDamage.png" alt=""><figcaption><p>The selected Menu Item is disabled, but still shows the Title and Description containing the player's shield amount</p></figcaption></figure>

A menu for toggling Skulls where the description of each Menu Item is updated based on if the Skull is enabled or not. First the Menu Items are added to the Menu, and then the Enabled state of them is re-evaluated with a separate for-loop that updates the Menu Item descriptions.

When any Menu Item in this Menu is selected, the same Menu is returned to the player to make the menu act in a button-like manner in addition to toggling the selected Skull.

<figure><img src="../../../.gitbook/assets/radial-skulls-code.png" alt=""><figcaption><p>Using Boolean values of certain Skulls being enabled or not to determine what is shown in the Description of a Menu Item</p></figcaption></figure>

<div><figure><img src="../../../.gitbook/assets/radial-skulls-code-off.png" alt=""><figcaption><p>Skull disabled</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-skulls-code-on.png" alt=""><figcaption><p>Skull enabled</p></figcaption></figure></div>

### Variable Enabled state values

By feeding a comparison output Boolean into the Enabled state property of a Menu Item, Menus can be built that display items in enabled or disabled states based on if the player meets the criteria for them to be selectable. In this example the player has enough points to spawn an allied Elite squad, but not a Brute squad.

<figure><img src="../../../.gitbook/assets/radial-aiAllies-code.png" alt=""><figcaption><p>Menu Items being enabled or disabled based on if the player has enough points or not. Points are deducted when a selection is made.</p></figcaption></figure>

<div><figure><img src="../../../.gitbook/assets/radial-aiAllies-true.png" alt=""><figcaption><p>Enough points to get Elite allies</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/radial-aiAllies-false.png" alt=""><figcaption><p>Not enough points to get Brute allies</p></figcaption></figure></div>

### tsg radial-example

A display of more example setups covering nearly everything `tsg radial` is capable of can be found in the module variant `tsg radial-example`. Bookmark the mode prefab below or find the it through the in-game UGC browser by searching with keywords or tags.

{% embed url="https://www.halowaypoint.com/halo-infinite/ugc/modes/7f2aa3ee-218c-42d8-844f-ee97f2357fbe" %}

<figure><img src="../../../.gitbook/assets/tsgRadial-example.jpg" alt=""><figcaption></figcaption></figure>

### tsg radial-machinima

A Machinima control Radial Menu built from `tsg radial`. Options for Camera Mode toggle, Weapon lowering, Fists and empty Sword grant, Fly mode toggle and item grants. Can be loaded as a standalone mode on any map. Bookmark the mode prefab below or find the it through the in-game UGC browser by searching with keywords or tags.

This Menu Module also contains examples of granting every type of weapon, equipment, vehicle and grenade.

{% embed url="https://www.halowaypoint.com/halo-infinite/ugc/modes/1729aa11-2af2-4275-980f-9bfda14bb8db" %}

{% embed url="https://www.youtube.com/watch?v=0tnwkerfBoc" %}



## Trivia

### Bug workarounds

There's a few mentions of some features in `tsg radial` being workarounds for bugs, so here's an explanation of all of them. Some of them are known issues listed by Halo Studios which are found [here](https://support.halowaypoint.com/hc/en-us/articles/39737155177492-Halo-Infinite-Fall-Update-2025-Patch-Notes#h_01JJQG5B1RQSM8HW3RTC7D1G9F).

#### Only one node instance working

_Using any of the nodes listed below more than once will result in only one instance of the node functioning:_

* _On Custom Input Tap_
* _On Custom Input Hold_
* _On Menu Item Selected_
* _On Player Started Sprinting_
* _On Player Stopped Sprinting_

The workaround for this is to immediately turn the node into a `Custom Event, Global Async` that serves the same purpose and can be used in multiple scripts. In `tsg radial` this is done with the nodes: On Custom Input Tap & On Menu Item Selected.



<div><figure><img src="../../../.gitbook/assets/workaround-on-custom-input-tap.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/workaround-on-menu-item-selected.png" alt=""><figcaption></figcaption></figure></div>



#### Unprompted Menus displaying for players

_Radial menus may appear during gameplay without players invoking them._

The workaround for this isn't mentioned in the documentation as it's a stealthy fix, but all that's required is to disable the visibility of the current Menu using the `Show Menu To Player` node right after the `On Menu Item Selected` & `On Menu Close` nodes.

<div><figure><img src="../../../.gitbook/assets/workaround-on-menu-item-selected.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/workaround-show-menu-to-player.png" alt=""><figcaption></figcaption></figure></div>

#### Menu Item selection doesn't work

_Selecting a Menu Item from a global-scoped Menu that has been disabled after the Menu has been shown to the player doesn't prompt a Menu Item selection._

This is not a bug, but something we have to workaround as object-scoped Menus are broken in their own ways currently, requiring us to use global-scoped menus. For the workaround, all of the Menu Items in the Menu that was just shown to the player are set to Enabled so issues don't arise for anyone who had the Menu previously open.

<figure><img src="../../../.gitbook/assets/tsg-radial-logMenu.png" alt=""><figcaption><p>The latter part of the logMenu event has the bug workaround.</p></figcaption></figure>

#### Undetected Menu closing

Opening two instances of the same global-scoped Menu simultaneously may close one instance of the Menu.

Another workaround required when working with global-scoped Menus since all players are trying to access the same global-scoped menu, some player may get caught in the process of the menu being built for some other player, and have the Menu just not show up for them when prompted.

What this results in is the custom tracking for `radialOpen` still being True cause it's assumed that the Menu got shown, but now the player is stuck with the movement locking traits. The workaround is a fallback to remove said traits by just changing the aim rotation, which is often the first thing players will do when they want to start moving again.

It's also convenient that you can't change your aim rotation while a Menu is open, so it works as a good fallback for removing the traits if something else were to prompt the Menu closing without the scripting catching on.

<figure><img src="../../../.gitbook/assets/tsg-radial-forceClose.png" alt=""><figcaption></figcaption></figure>





## Known Issues

A list of known issues that couldn't be fixed:

* Two players opening the same Menu at the simultaneously may often result in one player's Menu not displaying.
* Two players opening the same Menu at the simultaneously may rarely result in one player's Menu displaying for the other player.
* Two players opening the same Menu at the simultaneously may rarely result in one player's Menu showing all Menu Items in the Enabled state.
* Navigation between nested Menus becomes slower with latency to the server.



***

#### <mark style="color:green;">Contributors</mark>

Okom

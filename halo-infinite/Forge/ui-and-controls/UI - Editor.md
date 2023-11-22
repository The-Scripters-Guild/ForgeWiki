# Forge Editor UI

This is an overview of the UI you would see in Edit Mode while using Forge. Many elements are dynamic and adjust to the context of the current action the user is performing, and some can be shown or hidden via Tool Settings in the Forge Menu.

## Control Helper

Shows in the upper right of the screen. Automatically adjusts what is displayed based on context, including switching between showing Controller and MnK bindings as your input changes.

## Object Info Display

Shows in the bottom center of the screen. Shows the hovered or selected object's name, position, and rotation. Also shows how many objects/prefabs are selected. If more than one thing is selected, or a prefab is selected, the first object or prefab (specifically the parent object of the prefab), is what has its info displayed.

## Budget Meter

Shows in the bottom right of the screen. Displays the current Simulation Budget usage.

## Radial Menus

Show in the center of the screen, are hidden when not in use. Each radial menu is accessed by holding down a different button, shown in the Control Helper.

## Forge Menu

Shows in the upper left of the screen, is hidden when not in use. Accessed via a single button press to place a new object or by going directly to one of the other 4 submenus using a radial.

Menu items can be grouped, which is represented by a caret that is pointing to the right when collapsed and down when expanded and the child-items being indented. These can be expanded/collapsed by selecting/clicking the grouping's parent.

### Object Browser

The leftmost of the Forge Menu submenus. Can be accessed via a single button press to place a new object. It remembers your place and will return you to it.

The first entry is "Recents", which will show a list of objects you have recently spawned.

"{Prefabs}" is where you can find a list of prefabs that you have made and published, or have bookmarked from other users. Prefabs currently placed on the level are viewable in the Folders menu.

The remainder of the Object Browser menu is covered in Placeable Objects.

### Object Properties

The 2nd of the Forge Menu submenus. Can be accessed via the X radial when a object is selected.

This is where object-specific settings and metadata, such as physics settings, texturing, boundaries, etc., is accessed and fine-tuned. Different classes of objects will have different options.

#### General

**Visuals**

**Overlay**

**Transform**

**Position**

**Rotation**

**Object Mode**

#### Advanced Properties

### Folders

The 3rd of the Forge Menu submenus. Can be accessed via opening the Forge Menu and navigating over to it.

A hierarchical display of every object placed on the level in collapsable/expandable folders.

Folders group objects without binding them together, and folders can be in another folder (only 2 deep). Objects and folders can be reorganized by selecting them, clicking/selecting the 'gear' icon button, and selecting "Move".

Objects can be selected from this menu, as well as renamed to display differently for easier organization.

Using the 'eye' icon button, Objects can be hidden using this menu so that users don't have to delete, or move objects out of the way, to work on things that they would have otherwise been obstructing, or just to declutter while they work.

### Map Options

The 4th of the Forge Menu submenus. Can be accessed via opening the Forge Menu and navigating over to it.

This is where skybox, level-wide lighting, fog, and other similar things are controlled and is also where you would go to view current reasource budgets for the level.

This menu also has options to reset itself to default, and delete all unlocked objects on a level.

#### Lighting & Atmosphere

#### Decorators

#### Ambient Sound

#### Budget

#### Reset

### Tool Settings

The 5th and rightmost of the Forge Menu submenus. Can be accessed via opening the Forge Menu and navigating over to it.

Control settings for movement/rotation/scale snapping, camera speed, node graph interface controls, etc.

#### Transform

#### Camera

#### Node Graph

#### Magnets

#### Controller Scheme

#### HUD

#### Contributors:

Captain Punch

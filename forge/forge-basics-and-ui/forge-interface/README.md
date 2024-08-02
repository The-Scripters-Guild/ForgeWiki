---
description: >-
  Explanations of the interface and all of it's menus within Forge's level
  editor.
---

# Forge Interface

This page describes the elements of the Halo Infinite Forge level editor interface and what they do. It also links to other pages where you can learn more about the topics.

<figure><img src="../../../.gitbook/assets/cover-forge-interface.jpg" alt="Cover image"><figcaption></figcaption></figure>

## Limitations

Halo Infinite's Forge interface has some quality-of-life limitations as it has a static interface. Keep these in mind while reading:

* Menu placement cannot be changed
* Controls and shortcuts cannot be remapped

## Standard Interface

When you open a map in Forge, you will see the following interface:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-main.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#level-viewport">Level Viewport</a></td><td>Displays the contents of your Level, with the other menus overlaid on top.</td></tr><tr><td>2</td><td><a href="./#budget-meter">Budget Meter</a></td><td>Displays the Game Simulation Memory usage of the map.</td></tr><tr><td>3</td><td><a href="./#object-positional-data">Object Positional Data</a></td><td>Displays the position, rotation and size of the last selected object.</td></tr><tr><td>4</td><td><a href="./#controls-helper">Controls Helper</a></td><td>Displays controls and shortcuts for various actions.</td></tr></tbody></table>

### Level Viewport

The **Level Viewport** fills the entire screen and displays the contents of your level along with all Forge interfaces overlaid on top. The viewport is a 3D view of the level in real time and players can play their level in-engine using the different [Editor Modes](../editor-modes.md). There is no orthographic 2D view option in Halo Infinite's Forge.

[Forge transformation widgets](../coordinate-system-and-spaces.md) are optimized for a field of view (FOV) of 100°. A lower field of view will result in larger transformation widgets.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-fov65.jpg" alt=""><figcaption><p>FOV 65° @ 1920x1080</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-fov100.jpg" alt=""><figcaption><p>FOV 100° @ 1920x1080</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-fov120.jpg" alt=""><figcaption><p>FOV 120° @ 1920x1080</p></figcaption></figure>

</div>

Forge gameplay is optimized for window sizes above 1600x1200.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-1280x768.jpg" alt=""><figcaption><p>1280x768 @ FOV 100°</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-1600x1200.jpg" alt=""><figcaption><p>1600x1200 @ FOV 100°</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-1920x1080.jpg" alt=""><figcaption><p>1920x1080 @ FOV 100°</p></figcaption></figure>

</div>

### Budget Meter

The **Budget Meter** is located in the bottom left corner of the screen and displays the Game Simulation Memory usage of the map. Game Simulation Memory is the cost of simulating entities in a networked environment, including dynamic objects, projectiles, units, actions and similar.

This budget is often the first to reach 100% on maps that have more dynamic aspects to them such as multiple gamemode support and scripting rather than just mostly static geometry, but still many maps reach 100% on Forge Simulation Memory earlier, so the full reasoning for only displaying the Game Simulation Memory in this menu is unknown.

A decimal-accurate value of this budget can be seen in [Map Options](map-options.md) > Budget[^1]. The budget shown on the Budget Meter cannot be changed to display another budget. A yellow warning symbol appears on the Budget Meter if the Game Simulation Memory of the map reaches 80%, and at 100% the progress bar turns red.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-budget-meter-warning.jpg" alt=""><figcaption><p>Warning symbol shows up at 80%</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-budget-meter-full.jpg" alt=""><figcaption><p>Progress bar turns red at 100%</p></figcaption></figure>

</div>

Visibility of the Budget Meter can be toggled from [Tool Settings](tool-settings/) > [HUD > Budget Meter](#user-content-fn-2)[^2].

### Object Positional Data

The **Object Positional Data** menu is located at the bottom middle of the screen and displays axis values of the position, rotation and size of the last selected object. While the counterpart to this positional data interface in [Object Properties](object-properties/) > Transform can only display a maximum value of 9999.90 and a minimum of -9999.90, this on-screen menu can display values up to 2147483647.00 and down to -2147483647.00, which is the maximum value for a 32-bit signed binary integer. All values beyond those will display "EE".

For more functionality of this menu, see [Isolated Object Positional Data](./#isolated-object-positional-data).

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-32int.jpg" alt=""><figcaption><p>Object with a Y scale of 20700212480.00</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-ee.jpg" alt=""><figcaption><p>Object with a Y scale larger than 2147483647.00, displaying EE as the value</p></figcaption></figure>

</div>

How a scale of this size was achieved was with an exploit to [Bypass Object Scaling Limits](../../../guides-and-knowledge/forge-know-how/forge-exploits/bypassing-object-scaling-limits.md).

### Controls Helper

The **Controls Helper** menu is located at the top right of the screen and displays controls and shortcuts for various actions. The size of the menu will change depending on how many relevant controls and shortcuts can be done in the current state of manipulating objects or having different menus open.

While there are a lot of shortcuts shown in the helper menu, it does not display all shortcuts possible in Forge. These and more are explained in detail in [Controls and Shortcuts](../controls-and-shortcuts.md).

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-controls-helper1.png" alt=""><figcaption><p>Controls Helper menu while holding an item with the rotation widget selected</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-controls-helper2.png" alt=""><figcaption><p>Controls Helper menu when the Forge Menu is open with some categories expanded and while holding an item with the movement widget selected</p></figcaption></figure>

</div>

Visibility of the Controls Helper can be toggled from [Tool Settings](tool-settings/) > [HUD > Controls Helper](#user-content-fn-3)[^3].

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Controls and Shortcuts</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="../controls-and-shortcuts.md">controls-and-shortcuts.md</a></td></tr></tbody></table>

***

Pressing <img src="../../../.gitbook/assets/keyboard-r.png" alt="Key icon" data-size="line"> (keyboard) or <img src="../../../.gitbook/assets/controller-x.png" alt="Key icon" data-size="line"> (controller) opens up the **Forge Menu**, which houses more options:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-forge-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>5</td><td><a href="./#forge-menu">Forge Menu</a></td><td>Displays various properties related to Forge objects and map settings</td></tr></tbody></table>

### Forge Menu

The **Forge Menu** is located on the top left corner of the screen and it displays various properties related to Forge objects and map settings. The menu is divided into five unique tabs housing the most important information a Forger needs.

| Name                                      | Description                                                                                   |
| ----------------------------------------- | --------------------------------------------------------------------------------------------- |
| [Object Browser](object-browser.md)       | A list of available objects to spawn in Forge.                                                |
| [Object Properties](./#object-properties) | Properties for the selected object(s).                                                        |
| [Folders](folders/)                       | A hierarchical tree view of all objects placed on the map.                                    |
| [Map Options](map-options.md)             | Options for changing map lighting, wind and sound, and inspecting budget usage.               |
| [Tool Settings](tool-settings/)           | Options for changing the Forge tool properties, and toggling various debug options and menus. |

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Object Browser</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-browser.md">object-browser.md</a></td></tr><tr><td>Object Properties</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-properties/">object-properties</a></td></tr><tr><td>Folders</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="folders/">folders</a></td></tr><tr><td>Map Options</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="map-options.md">map-options.md</a></td></tr><tr><td>Tool Settings</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="tool-settings/">tool-settings</a></td></tr></tbody></table>



## Selected Object Interface

If an object is selected, the Forge interface changes slightly, revealing more information:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-selected-object.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#selected-object-count">Selected Object Count</a></td><td>Displays the amount of objects currently selected. A maximum of 150 can be selected at the same time.</td></tr><tr><td>2</td><td><a href="./#object-information">Object Information</a></td><td>Displays the Object Mode, Physics and Name of the last selected object.</td></tr><tr><td>3</td><td><a href="./#isolated-object-positional-data">Isolated Object Positional Data</a></td><td>Highlights the positional data of the currently selected transform gizmo.</td></tr><tr><td>4</td><td><a href="./#transform-snap-and-coordinate-space">Transform Snap and Coordinate Space</a></td><td>Displays the snap values and coordinate space of the currently selected transform gizmo.</td></tr></tbody></table>

### Selected Object Count

The **Selected Object Count** indicator is located in the bottom middle of the screen, and displays the amount of objects currently selected. A maximum of 150 objects can be selected at the same time, but more may be selected if some of the items in the selection are in a prefab. Learn more about [Bypassing 150-Object Prefab Limit](../../../guides-and-knowledge/forge-know-how/forge-exploits/bypassing-150-object-prefab-limit.md).

### Object Information

The **Object Information** string is located in the bottom middle of the screen, and displays the Object Mode, Physics and Name of the last selected object. The syntax is as follows:

> \[{Object Mode}: {Physics}] {Object Name}

The number at the end of objects is a part of the object name. If an object with a duplicate name is created, an incrementing number will be appended to the end of the object name.

The Object Mode indicator color is white for Static objects and orange for Dynamic objects. There is also a third uncommon Object Mode "None" that can be seen on gameplay objects.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-info-static.jpg" alt=""><figcaption><p>Object Mode: Static</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-object-info-dynamic.jpg" alt=""><figcaption><p>Object Mode: Dynamic</p></figcaption></figure>

</div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-info-none.jpg" alt=""><figcaption><p>Object Mode: None</p></figcaption></figure>

### Isolated Object Positional Data

The [Object Positional Data](./#object-positional-data) menu changes slightly when an object is selected and one of the three [Transform Gizmos](#user-content-fn-4)[^4] are selected; The positional data of the currently selected transform gizmo is highlighted, and the other data displays are made less opaque.

The transform gizmos can be cycled between with the following shortcuts:

* Movement: <img src="../../../.gitbook/assets/keyboard-ctrl-left.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/keyboard-w.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-lt.png" alt="Key icon" data-size="line"> (controller)
* Rotation: <img src="../../../.gitbook/assets/keyboard-ctrl-left.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/keyboard-e.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-rt.png" alt="Key icon" data-size="line"> (controller)
* Size: <img src="../../../.gitbook/assets/keyboard-ctrl-left.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/keyboard-r.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-lt.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/controller-rt.png" alt="Key icon" data-size="line"> (controller)
* Cycle between all: <img src="../../../.gitbook/assets/keyboard-tab.png" alt="Key icon" data-size="line"> (keyboard)

{% hint style="info" %}
Another way to isolate the Object Positional Data without selecting an object is to hover your cursor over the object and press <img src="../../../.gitbook/assets/keyboard-tab.png" alt="Key icon" data-size="line"> (keyboard) to cycle between the gizmos. This has no real use and is most likely a bug. A potential purpose of this is to act as a hacky way to simulate hovering over objects and previewing their properties as the movement gizmo is not rendered and is the default gizmo here.
{% endhint %}

If the same gizmo shortcut is entered while that gizmo is already selected, the gizmo will disappear and the Object Positional Data menu will return to showing all values highlighted while still having an object selected.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-isolated-movement.jpg" alt=""><figcaption><p>Movement gizmo selected</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-isolated-rotation.jpg" alt=""><figcaption><p>Rotation gizmo selected</p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-isolated-scale.jpg" alt=""><figcaption><p>Scale gizmo selected</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-isolated-nogizmo.jpg" alt=""><figcaption><p>No gizmo selected</p></figcaption></figure>

</div>

### Transform Snap and Coordinate Space

The **Transform Snap and Coordinate Space** menu is located in the top right of the screen, and displays the snap values and coordinate space of the currently selected transform gizmo. The snap values can be adjusted with <img src="../../../.gitbook/assets/keyboard-plus.png" alt="Key icon" data-size="line">/<img src="../../../.gitbook/assets/keyboard-numpad-plus.png" alt="Key icon" data-size="line"> and <img src="../../../.gitbook/assets/keyboard-minus.png" alt="Key icon" data-size="line">/<img src="../../../.gitbook/assets/keyboard-numpad-minus.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-lt.png" alt="Key icon" data-size="line">/<img src="../../../.gitbook/assets/controller-rt.png" alt="Key icon" data-size="line">/<img src="../../../.gitbook/assets/controller-lt.png" alt="Key icon" data-size="line"> & <img src="../../../.gitbook/assets/controller-rt.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/controller-dpad-horizontal.png" alt="Key icon" data-size="line"> (controller), and the space/type can be cycled with <img src="../../../.gitbook/assets/keyboard-5.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-lt.png" alt="Key icon" data-size="line">/<img src="../../../.gitbook/assets/controller-rt.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/controller-dpad-vertical.png" alt="Key icon" data-size="line"> (controller).

The available snap values are as follows:

* Movement & Scale: `<none>`, `0.001'`, `1/8'`, `1/4'`, `1/2'`, `1'`, `2'`, `4'`, `8'` & `16'`
* Rotation: `<none>`, `1/2°`, `1°`, `5`°, `15°`, `30°`, `45°`, `60°`, `90°` & `180°`

For more information about snapping, see Snapping[^5].

{% hint style="info" %}
**Note from Okom:**\
I usually use a Movement Snap of `0.001'`, Rotation Snap of `15°` or `5°,` and a Scaling Snap of `1/8'`, which work for me as the most efficient and versatile snap values after 3000+ hours of Halo Infinite Forging experience.
{% endhint %}

The available space/type values are as follows:

* Movement: `World` & `Object`
* Rotation: `World`, `Camera` & `Object`

For more information about spaces, see [Coordinate Spaces](#user-content-fn-6)[^6].

## Actions Menu

Holding <img src="../../../.gitbook/assets/keyboard-e.png" alt="Key icon" data-size="line"> (keyboard) or <img src="../../../.gitbook/assets/controller-x.png" alt="Key icon" data-size="line"> (controller) at any time while in Monitor Mode will open the radial **Actions Menu**:

<figure><img src="../../../.gitbook/assets/forge-interface-actions-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#create-prefab-create-mode-prefab">Create Prefab / Create Mode Prefab</a></td><td>Create a savable group of a minimum two objects.</td></tr><tr><td>2</td><td><a href="./#object-properties">Object Properties</a></td><td>Modify the properties of the selected object(s).</td></tr><tr><td>3</td><td><a href="./#add-to-prefab">Add To Prefab</a></td><td>Combine the selected objects into an existing selected prefab.</td></tr><tr><td>4</td><td><a href="./#weld">Weld</a></td><td>Group together Dynamic objects. The origin object has to have Normal physics.</td></tr><tr><td>5</td><td><a href="./#save-prefab">Save Prefab</a></td><td>Save a selected Prefab to My Files.</td></tr><tr><td>6</td><td><a href="./#unweld">Unweld</a></td><td>Break the weld from a group of welded Dynamic objects, making the object group into a prefab.</td></tr><tr><td>7</td><td><a href="./#ungroup">Ungroup</a></td><td>Disconnect a group of prefabbed objects or a group of welded Dynamic objects.</td></tr><tr><td>8</td><td><a href="./#object-browser">Object Browser</a></td><td>Open the Object Browser menu to see a list of available objects to spawn in Forge.</td></tr></tbody></table>

### Create Prefab / Create Mode Prefab

The **Create Prefab / Create Mode Prefab** tab is located on the top of the radial Actions Menu and is used to create a savable group of a minimum two objects. A prefab is a group of objects that pivot around a single object and can easily be saved to share with others. Prefabs have a green outline around all of the child objects within it, with the parent object having a cyan outline.

Learn more about [Prefabs](../../../ugc/metadata-and-file-management/prefabs/).

<div>

<figure><img src="../../../.gitbook/assets/prefab-albatross1.jpg" alt=""><figcaption><p>A named prefab resembling a Halo 3 vehicle prop</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/prefab-albatross2.jpg" alt=""><figcaption><p>The prefab ungrouped shows that it's made from 73 objects</p></figcaption></figure>

</div>

A Mode Prefab can be made with two or more [Mode Brains](../../../scripting/scripting-basics-and-ui/script-brains-and-mode-brains.md) as the only objects in the group of objects. Mode Brains are used to make playable [Forge Modes](#user-content-fn-7)[^7].

Learn more about [Mode Prefabs](../../../ugc/metadata-and-file-management/prefabs/mode-prefabs.md).

<div>

<figure><img src="../../../.gitbook/assets/prefab-mode-brain1.jpg" alt=""><figcaption><p>A selection of two Mode Brains</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-action-menu-prefab-mode.jpg" alt=""><figcaption><p>"Create Mode Prefab" tab in the Actions Menu</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/prefab-mode-brain2.jpg" alt=""><figcaption><p>A Mode Prefab consisting of two Mode Brains</p></figcaption></figure>

</div>

### Object Properties

The **Object Properties** tab is located on the top right of the radial Actions Menu and is used to modify the properties of the selected object(s).

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Object Properties</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-properties/">object-properties</a></td></tr></tbody></table>

### Add To Prefab

The **Add To Prefab** tab is located on the right of the radial Actions Menu and is used to combine the selected objects into an existing selected prefab. Adding new objects to an Object Prefab will reset the prefab name and make it an entirely new asset. Adding new objects to a Mode Prefab will keep the same prefab name and asset ID.

Learn more about [Prefabs](../../../ugc/metadata-and-file-management/prefabs/).

{% hint style="info" %}
Saved Object Prefabs cannot be updated with new objects while keeping the same asset ID, but Mode Prefabs can.
{% endhint %}

### Weld

The **Weld** tab is located on the bottom right of the radial Actions Menu and is used to group together Dynamic objects. The origin object of the group has to have Normal physics for the weld to be possible; the rest of the objects can be any physics, but their Object Mode must not be Static. Two vehicles cannot be welded together.

Welded Prefabs have a purple outline around all of the child objects within it, with the parent object having a cyan outline.

{% hint style="warning" %}
Mounted Turret weapons classify as vehicles so they sadly cannot be welded to other vehicles.
{% endhint %}

Welding is similar to prefabbing, but there are a few differences:

* Welds cannot contain static objects
* Vehicle physics don't apply to prefabs
* Welds cannot contain two vehicles
* Welds cannot contain some Dynamic, Normal physics objects. Currently known list:
  * Launchers

Welding is often used to create vehicles that have objects attached to them:

<div>

<figure><img src="../../../.gitbook/assets/weld-warthog-armored.jpg" alt=""><figcaption><p>A Warthog with UNSC Cover pieces welded to it that act as armor</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/weld-razorback-ammo.jpg" alt=""><figcaption><p>Razorbacks with an Ammo Crate welded to the back</p></figcaption></figure>

</div>

> Map: [Just Keep Driving - Sandtrap](https://www.halowaypoint.com/halo-infinite/ugc/maps/acf53d3b-de15-453f-8e40-901fd8272aad)

{% hint style="info" %}
The vehicles were momentarily made to have Phased physics with an exploit before welding in order to phase the cover objects into them because the only physics option for vehicles is Normal. Learn more about: [Applying Inaccessible Object Properties](../../../guides-and-knowledge/forge-know-how/forge-exploits/applying-inaccessible-object-properties.md).
{% endhint %}

Welds can also be used to make interactable map objects, sometimes using clever tricks:

<div>

<figure><img src="../../../.gitbook/assets/weld-bridge1.jpg" alt="" width="563"><figcaption><p>Interactable welded bridge</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/weld-bridge2.jpg" alt="" width="563"><figcaption><p>Artificial movement restriction on the Y axis; the sphere is a part of the weld</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/weld-bridge3.jpg" alt="" width="563"><figcaption><p>Bridge falling down after being punched</p></figcaption></figure>

</div>

> Map: [Boulevard](https://www.halowaypoint.com/halo-infinite/ugc/maps/05a4f045-0b4b-4565-a246-38fb6be62a30)

{% hint style="info" %}
The most important factor in making a welded prefab like this work is ensuring that the movement restriction sphere is perfectly aligned with the welded prefab on the axis that is to be restricted, and that it's enclosed very tightly so that the sphere cannot move in any unwanted directions.
{% endhint %}

#### Massless Children

Welded Prefabs have a setting called "Massless Children" found in the Object Properties of the prefab. This setting makes the welded prefab not take into account the mass it's child objects when calculating physics.

<figure><img src="../../../.gitbook/assets/weld-massless-children-setting.jpg" alt=""><figcaption><p>Massless Children setting in the Object Properties of a Welded Prefab</p></figcaption></figure>

<div>

<figure><img src="../../../.gitbook/assets/weld-massless-children-false.jpg" alt=""><figcaption><p>Massless Children OFF</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/weld-massless-children-true.jpg" alt=""><figcaption><p>Massless Children ON</p></figcaption></figure>

</div>

#### Weld Bugs

Although welds can be used as useful gameplay elements, there are a ton of bugs surrounding them, which makes working with welded prefabs extremely annoying, sometimes to the point of having to scrap the idea that would have worked if there weren't some obscure issues happening to them.

Learn more about [Welded Prefab Bugs](../../../guides-and-knowledge/forge-know-how/forge-bugs/welded-prefab-bugs.md).

### Save Prefab

The **Save Prefab** tab is located on the bottom of the radial Actions Menu and is used to save a selected Prefab to [My Files](#user-content-fn-8)[^8]. After selecting, an interface to enter the name of the prefab will be shown. A quirk of this interface is that a prefab name up to 40 characters can be entered, unlike the 32-character limit of renaming a file through the [File Name](../../../ugc/metadata-and-file-management/working-with-files/file-name.md) interface. This also works for naming Forge Modes by saving Mode Prefabs.

<div>

<figure><img src="../../../.gitbook/assets/prefab-save-name.jpg" alt=""><figcaption><p>40-character limit when saving a prefab and entering a name</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/file-name-edit.jpg" alt=""><figcaption><p>32-character limit when editing the name of an asset</p></figcaption></figure>

</div>

### Unweld

The **Unweld** tab is located on the bottom left of the radial Actions Menu and is used to break the weld from a group of welded Dynamic objects, making the object group into a prefab.

After unwelding, the group of objects will turn into a prefab.

Be aware of the [Welded Prefab Bugs](../../../guides-and-knowledge/forge-know-how/forge-bugs/welded-prefab-bugs.md) that may occur when unwelding a welded prefab.

### Ungroup

The **Ungroup** tab is located on the left of the radial Actions Menu and is used to disconnect a group of prefabbed objects or a group of welded Dynamic objects.

After ungrouping, the group of objects that made up the prefab will stay selected. If the prefab included more than 150 objects, only the first 150 objects will stay in the selection. If the remaining objects are Static, they will keep a green outline until a temporary hover-over selection is performed on them.

Learn more about: [Bypassing 150-Object Prefab Limit](../../../guides-and-knowledge/forge-know-how/forge-exploits/bypassing-150-object-prefab-limit.md).

<div>

<figure><img src="../../../.gitbook/assets/prefab-over150-prefabbed.jpg" alt=""><figcaption><p>A 206-object prefab</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/prefab-over150-ungrouped.jpg" alt=""><figcaption><p>Prefab ungrouped, 150 objects left in the selection</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/prefab-over150-deselected.jpg" alt=""><figcaption><p>Objects deselected, leaving the remaining 56 objects with a green outline </p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/prefab-over150-hover.jpg" alt="" width="563"><figcaption><p>The green outline will disappear once the object is hovered over with a cursor selection</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/prefab-over150-playmode.jpg" alt="" width="563"><figcaption><p>The green outline will stay on the objects in Play Mode; outline does not stay after a session restart</p></figcaption></figure>

</div>

> Prefab: [Halo 3 Elephant (2 of 2)](https://www.halowaypoint.com/halo-infinite/ugc/prefabs/85670a93-f8ff-40fd-9874-0c33a5461b12)

### Object Browser

The **Object Browser** tab is located on the top left of the radial Actions Menu and is used to open the Object Browser menu to see a list of available objects to spawn in Forge.

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Object Browser</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-browser.md">object-browser.md</a></td></tr></tbody></table>



## Tools Menu

Holding <img src="../../../.gitbook/assets/keyboard-q.png" alt="Key icon" data-size="line"> (keyboard) or <img src="../../../.gitbook/assets/controller-y.png" alt="Key icon" data-size="line"> (controller) at any time while in Monitor Mode will open the radial Tools Menu:

<figure><img src="../../../.gitbook/assets/forge-interface-tools-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#node-graph">Node Graph</a></td><td>Open the Node Graph to create scripts.</td></tr><tr><td>2</td><td><a href="./#build-menu">Build Menu</a></td><td>Build data for various map elements.</td></tr><tr><td>3</td><td><a href="./#quicksave">Quicksave</a></td><td>Save the current map version with no custom version note added.</td></tr></tbody></table>

### Node Graph

The **Node Graph** tab is located on the top of the radial Tools Menu and is used to open the Node Graph to create scripts. The Node Graph Interface can also be opened with <img src="../../../.gitbook/assets/keyboard-n.png" alt="Key icon" data-size="line"> (keyboard).

Learn more about [Node Graph Interface and Controls](../../../scripting/scripting-basics-and-ui/node-graph-interface/).

### Build Menu

The **Build Menu** tab is located on the right of the radial Tools Menu and is used to build data for various map elements. The available map data to build are:

* [Lighting](../../lighting/building-lighting/)
* [Nav Mesh](../../nav-mesh/nav-mesh-generation/building-nav-mesh/)
* [Audio](../../gameplay/audio/building-audio/)
* [Reflection Volumes](../../lighting/lighting-modifiers/reflections/reflection-volumes/building-reflection-volumes.md)

Yellow warning symbols are displayed on the elements that aren't up-to-date with the current state of the map. While these do convey a real problem, the map can still be played and published even if some build data has a warning symbol next to it.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-build-menu-warning.jpg" alt=""><figcaption><p>Outstanding elements left to build after map modifications</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-build-menu-complete.jpg" alt=""><figcaption><p>All build data up-to-date with the current state of the map</p></figcaption></figure>

</div>

Due to all the warning symbols appearing right after even a single object's position is altered on the map, it is not recommended to constantly keep building map element data just because there is a warning symbol next to it. Instead, learn when map data should be built and build it only when necessary.

{% content-ref url="../../lighting/building-lighting/" %}
[building-lighting](../../lighting/building-lighting/)
{% endcontent-ref %}

{% content-ref url="../../nav-mesh/nav-mesh-generation/building-nav-mesh/" %}
[building-nav-mesh](../../nav-mesh/nav-mesh-generation/building-nav-mesh/)
{% endcontent-ref %}

{% content-ref url="../../gameplay/audio/building-audio/" %}
[building-audio](../../gameplay/audio/building-audio/)
{% endcontent-ref %}

{% content-ref url="../../lighting/lighting-modifiers/reflections/reflection-volumes/building-reflection-volumes.md" %}
[building-reflection-volumes.md](../../lighting/lighting-modifiers/reflections/reflection-volumes/building-reflection-volumes.md)
{% endcontent-ref %}

### Quicksave

The **Quicksave** tab is located on the bottom of the radial Tools Menu and is used to save the current map version with no custom version note added. After activation, a message will show in the killfeed indicating that the map version has been saved successfully. A quicksave can also be done with <img src="../../../.gitbook/assets/keyboard-ctrl-left.png" alt="Key icon" data-size="line"> + <img src="../../../.gitbook/assets/keyboard-s.png" alt="Key icon" data-size="line"> (keyboard).

<figure><img src="../../../.gitbook/assets/forge-interface-quicksave.jpg" alt=""><figcaption><p>Message "{Gamertag} Map saved successfully." displaying in the killfeed after a quicksave</p></figcaption></figure>

A quicksave will not prompt for a version note to be added to the saved version. Instead, the string "Quicksave" will be automatically added as the note for the version.

Learn more about: [Saving Assets](../saving-assets.md).

<figure><img src="../../../.gitbook/assets/forge-interface-quicksave-versionhistory.jpg" alt=""><figcaption><p>Automatic edit note "Quicksave" seen on some versions in a map's version history</p></figcaption></figure>

## Play Mode

If Play Mode is entered with <img src="../../../.gitbook/assets/keyboard-f6.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-view.png" alt="Key icon" data-size="line"> (controller), the Forge interface changes to show information relevant to gameplay:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-play-mode.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#runtime-budget-meter">Runtime Budget Meter</a></td><td>Displays the runtime budget which is the most full based on the current state of the map.</td></tr><tr><td>2</td><td><a href="./#score-and-timer">Score and Timer</a></td><td>Displays the score of two teams and an unlimited timer that counts upwards.</td></tr><tr><td>3</td><td><a href="./#global-log">Global Log</a></td><td>Displays the runtime state of the Node Graph including potential errors and warnings.</td></tr><tr><td>4</td><td><a href="./#controls-helper-1">Controls Helper</a></td><td>Displays controls and shortcuts for various actions</td></tr></tbody></table>

### Runtime Budget Meter

The **Runtime Budget Meter** is located in the bottom left of the screen, and displays the runtime budget which is the most full based on the current state of the map. The different budgets that can be displayed are:

* Runtime Objects
* Navpoints
* Objectives
* AI Units

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-runtime-objects.jpg" alt=""><figcaption><p>Runtime Objects usage display</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-navpoints.jpg" alt=""><figcaption><p>Navpoints usage display</p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-objectives.jpg" alt=""><figcaption><p>Objectives usage display</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-ai-units.jpg" alt=""><figcaption><p>AI Units usage display</p></figcaption></figure>

</div>

A yellow warning symbol appears on the Runtime Budget Meter if the displayed budget of the map reaches 80%, and at 100% the progress bar turns red.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-warning.jpg" alt=""><figcaption><p>Warning symbol shows up at 80%</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-runtime-budget-full.jpg" alt=""><figcaption><p>Progress bar turns red at 100%</p></figcaption></figure>

</div>

The budget shown on the Runtime Budget Meter cannot manually be changed to display another budget. It only always displays the budget with the most usage at runtime. Visibility of the Runtime Budget Meter can be toggled from [Tool Settings](tool-settings/) > HUD > [Runtime Budget Meter](#user-content-fn-9)[^9].

### Score and Timer

The **Score and Timer** are located in the bottom middle of the screen, and display the score of two teams and an unlimited timer that counts upwards. The score in the Forge Play Mode can only be adjusted via scripting with the [Adjust Team Points](../../../scripting/nodes/game-mode/adjust-team-points.md) node.

The UI for the score display is built to support values up to 4 digits long before it starts to overflow. The score field can display values up to 2147483647 and down to -2147483647, which is the maximum value for a 32-bit signed binary integer. All values beyond those will display "EE".

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-score.jpg" alt=""><figcaption><p>Eagle: 123 / Cobra: 45678</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-score-max.jpg" alt=""><figcaption><p>Score 2147474816 on both teams</p></figcaption></figure>

</div>

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-score-min.jpg" alt=""><figcaption><p>Eagle: -2147474816 / Cobra: 0</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-score-ee.jpg" alt=""><figcaption><p>Eagle: EE / Cobra: 0</p></figcaption></figure>

</div>

### Global Log

The **Global Log** is located in the top right of the screen, and displays the runtime state of the Node Graph including potential errors and warnings.

The syntax for an error is as follows:

> <mark style="color:red;">**Warning**</mark>/<mark style="color:yellow;">**Caution**</mark> <{Script Brain Name}>  {error statement}\
> \--- Node Graph **failed to build**

<figure><img src="../../../.gitbook/assets/forge-interface-global-log-errors.jpg" alt=""><figcaption><p>The Global Log displaying Warning and Caution messages indicating a script that did not execute properly.</p></figcaption></figure>

Many scripters have despised the lack of detail in the error statements printed in the Global Log as they can often be too vague such as "node missing required property", which doesn't indicate which node is the cause, and which property is missing.

Visibility of the Play Mode Global Log can be toggled from [Tool Settings](tool-settings/) > [HUD > Global Log](#user-content-fn-10)[^10].

### Controls Helper

The **Controls Helper** is located in the top right of the screen, and displays controls and shortcuts for various actions. In Play Mode, it only displays the control to return to Monitor Mode, <img src="../../../.gitbook/assets/keyboard-f6.png" alt="Key icon" data-size="line"> (keyboard) or \[Hold] <img src="../../../.gitbook/assets/controller-view.png" alt="Key icon" data-size="line"> (controller).



## Trivia

At a glance, Halo Infinite's Forge is modeled heavily after Halo 5's. The default control scheme for controllers is also reminiscent of Halo 5's defaults. Users of previous titles have control schemes available to choose from to have an experience closer to those titles.

While the menus are similarly placed and handle very similarly to Halo 5's, there is the addition of radial menus that can be called for accessing functions like prefabbing, group welding, opening a Script Brain's node graph, etc., and the options available across the board are much deeper.

It is apparent via node graphs, the expanded lighting options, and more, that many cues have been taken from more fully-featured game dev IDEs and repackaged to work well and have parity between console and pc.

As with any tool of this complexity and depth, there is a learning curve present with the tool, but it remains that the surface-level is still accessible enough to build simple levels. The forger will just need to know the majority of the toolset in order to bring their level to a higher standard, which wasn't previously possible, and now is expected of the top performing levels.



***

#### <mark style="color:green;">Contributors</mark>

Okom\
Captain Punch\
Mr Greencastle\
Yolomcswag\
MikRips

[^1]: Add link when complete

[^2]: Add link when complete

[^3]: Add link when complete

[^4]: Add link when the article for it is written

[^5]: Add link when ready

[^6]: Add link when complete

[^7]: Add link when written

[^8]: Add link once done

[^9]: Add link when complete

[^10]: Add link when complete

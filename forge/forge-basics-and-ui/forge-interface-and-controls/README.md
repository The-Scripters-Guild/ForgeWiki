---
description: >-
  Topics about the controls and menu functionality of the Forge tool in Halo
  Infinite.
---

# Forge Interface and Controls

{% hint style="warning" %}
This article is a stub. You can help TSG Forge Wiki by expanding it.
{% endhint %}

{% content-ref url="../../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md" %}
[submitting-content-to-the-wiki.md](../../../community/contributing-to-tsg-forge-wiki/submitting-content-to-the-wiki.md)
{% endcontent-ref %}

This page describes the elements of the Halo Infinite Forge interface, what they do, and what controls and shortcuts are available in Forge. It also links to other pages where you can learn more about the topics.

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption><p>This is a cover image with the aspect ratio of 21:9. This is a custom cropped image just for this purpose, and one should be made for each article, if possible. In a real article, leave this text caption field blank for the cover image. Remember to change the alt text of the image.</p></figcaption></figure>

## Limitations

Halo Infinite's Forge interface has some quality-of-life limitations as it has quite a static interface. Keep these in mind while reading:

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

A decimal-accurate value of this budget can be seen in [Map Options](map-options.md) > Budget. The budget shown on the Budget Meter cannot be changed to display another budget. A yellow warning symbol appears on the Budget Meter if the Game Simulation Memory of the map reaches 80%, and at 100% the progress bar turns red.

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-budget-meter-warning.jpg" alt=""><figcaption><p>Warning symbol shows up at 80%</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-budget-meter-full.jpg" alt=""><figcaption><p>Progress bar turns red at 100%</p></figcaption></figure>

</div>

### Object Positional Data

The **Object Positional Data menu** is located at the bottom middle of the screen and displays axis values of the position, rotation and size of the last selected object. While the counterpart to this positional data interface in [Object Properties](object-properties/) > Transform can only display a maximum value of 9999.90 and a minimum of -9999.90, this on-screen menu can display values up to 2147483647.00 and down to -2147483647.00, which is the maximum value for a 32-bit signed binary integer. All values beyond that point will display "EE".

For more functionality of this menu, see [Isolated Object Positional Data](./#isolated-object-positional-data).

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-32int.jpg" alt=""><figcaption><p>Object with a Y scale of 20400212480.00</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-object-pos-ee.jpg" alt=""><figcaption><p>Object with a Y scale larger than 2147483647.00, displaying EE as the value</p></figcaption></figure>

</div>

How a scale of this size was achieved was with an exploit to [Bypass Object Scaling Limits](../../../guides-and-knowledge/forge-know-how/forge-exploits/bypassing-object-scaling-limits.md).

### Controls Helper

The Controls Helper menu is located at the top right of the screen and displays controls and shortcuts for various actions. The size of the menu will change depending on how many relevant controls and shortcuts can be done in the current state of manipulating objects or having different menus open.

While there are a lot of shortcuts shown in the helper menu, it does not display all shortcuts possible in Forge. These and more are explained in detail in [Controls and Shortcuts](controls-and-shortcuts.md).

<div>

<figure><img src="../../../.gitbook/assets/forge-interface-controls-helper1.png" alt=""><figcaption><p>Controls Helper menu while holding an item with the rotation widget selected</p></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/forge-interface-controls-helper2.png" alt=""><figcaption><p>Controls Helper menu when the Forge Menu is open with some categories expanded and while holding an item with the movement widget selected</p></figcaption></figure>

</div>

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Controls and Shortcuts</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="controls-and-shortcuts.md">controls-and-shortcuts.md</a></td></tr></tbody></table>

***

Pressing `R` or `(controller key)` opens up the Forge Menu, which houses more options:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-forge-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>5</td><td><a href="./#forge-menu">Forge Menu</a></td><td>Displays various properties related to Forge objects and map settings</td></tr></tbody></table>

### Forge Menu

The Forge Menu is located on the top left corner of the screen and it displays various properties related to Forge objects and map settings. The menu is divided into five unique tabs housing the most important information a Forger needs.

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

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#selected-object-count">Selected Object Count</a></td><td>Displays the amount of objects currently selected in a group. A maximum of 150 can be selected at the same time.</td></tr><tr><td>2</td><td><a href="./#object-information">Object Information</a></td><td>Displays the Object Mode, Physics and Name of the last selected object.</td></tr><tr><td>3</td><td><a href="./#isolated-object-positional-data">Isolated Object Positional Data</a></td><td>Highlights the positional data of the currently selected transform gizmo.</td></tr><tr><td>4</td><td><a href="./#transform-snap-and-space">Transform Snap and Space</a></td><td>Displays the snap values and coordinate space of the currently selected transform gizmo.</td></tr></tbody></table>

### Selected Object Count

\-

### Object Information

\-

### Isolated Object Positional Data

\-

### Transform Snap and Space

\-



## Actions Menu

Holding `E` or `(controller key)` at any time while in Monitor Mode will open the radial Actions Menu:

<figure><img src="../../../.gitbook/assets/forge-interface-actions-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#create-prefab-create-mode-prefab">Create Prefab / Create Mode Prefab</a></td><td>Creates a savable group of minimum two objects.</td></tr><tr><td>2</td><td><a href="./#object-properties">Object Properties</a></td><td>Modify the properties of the selected object(s).</td></tr><tr><td>3</td><td><a href="./#add-to-prefab">Add To Prefab</a></td><td>Combine the selected objects into an existing selected prefab.</td></tr><tr><td>4</td><td><a href="./#weld">Weld</a></td><td>Group together Dynamic objects. The origin object has to have Normal physics.</td></tr><tr><td>5</td><td><a href="./#save-prefab">Save Prefab</a></td><td>Save a selected Prefab to My Files.</td></tr><tr><td>6</td><td><a href="./#unweld">Unweld</a></td><td>Disconnect a group of welded Dynamic objects.</td></tr><tr><td>7</td><td><a href="./#ungroup">Ungroup</a></td><td>Disconnect a group of prefabbed objects or a group of welded Dynamic objects.</td></tr><tr><td>8</td><td><a href="./#object-browser">Object Browser</a></td><td>Open the Object Browser menu to see a list of available objects to spawn in Forge.</td></tr></tbody></table>

### Create Prefab / Create Mode Prefab

\-

### Object Properties

Modify the properties of the selected object(s).

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Object Properties</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-properties/">object-properties</a></td></tr></tbody></table>

### Add To Prefab

\-

### Weld

\-

### Save Prefab

\-

### Unweld

\-

### Ungroup

\-

### Object Browser

Open the Object Browser menu to see a list of available objects to spawn in Forge.

**Learn more about:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Object Browser</td><td><a href="../../../.gitbook/assets/cover-tsg-placeholder.jpg">cover-tsg-placeholder.jpg</a></td><td><a href="object-browser.md">object-browser.md</a></td></tr></tbody></table>



## Tools Menu

Holding `Q` or `(controller key)` at any time while in Monitor Mode will open the radial Tools Menu:

<figure><img src="../../../.gitbook/assets/forge-interface-tools-menu.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#node-graph">Node Graph</a></td><td>Open the Node Graph to create scripts.</td></tr><tr><td>2</td><td><a href="./#build-menu">Build Menu</a></td><td>Build data for various map elements.</td></tr><tr><td>3</td><td><a href="./#quicksave">Quicksave</a></td><td>Save the current map version with no custom version note added.</td></tr></tbody></table>

### Node Graph

\-

### Build Menu

\-

### Quicksave

\-



## Play Mode

If Play Mode is entered with `F6` or `(controller key)`, the Forge interface changes to show information relevant to gameplay:

<figure><img src="../../../.gitbook/assets/forge-interface-controls-play-mode.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th data-type="number">Number</th><th>Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td><a href="./#runtime-budget-meter">Runtime Budget Meter</a></td><td>Displays the runtime budget which is the most full based on the current state of the map.</td></tr><tr><td>2</td><td><a href="./#score-and-timer">Score and Timer</a></td><td>Displays the score of both teams and an unlimited timer that counts upwards.</td></tr><tr><td>3</td><td><a href="./#global-log">Global Log</a></td><td>Displays the runtime state of the Node Graph including potential errors and warnings.</td></tr></tbody></table>

### Runtime Budget Meter

\-

### Score and Timer

\-

### Global Log

\-



## Trivia

At a glance, Halo Infinite's Forge is modeled heavily after Halo 5's. The default control scheme for controllers is also reminiscent of Halo 5's defaults. Users of previous titles have control schemes available to choose from to have an experience closer to those titles.

While the menus are similarly placed and handle very similarly to Halo 5's, there is the addition of radial menus that can be called for accessing functions like prefabbing, group welding, opening a Script Brain's node graph, etc., and the options available across the board are much deeper.

It is apparent via node graphs, the expanded lighting options, and more, that many cues have been taken from more fully-featured game dev IDEs and repackaged to work well and have parity between console and pc.

As with any tool of this complexity and depth, there is a learning curve present with the tool, but it remains that the surface-level is still accessible enough to build simple levels. The forger will just need to know the majority of the toolset in order to bring their level to a higher standard, which wasn't previously possible, and now is expected of the top performing levels.

***

#### <mark style="color:green;">Contributors</mark>

Okom\
Captain Punch

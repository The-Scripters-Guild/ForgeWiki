---
description: >-
  Explains the Cartesian coordinate system, axis conventions,
  transformation spaces, and snapping mechanics used in Halo Infinite
  Forge.
---

# Coordinate System and Spaces

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Halo Infinite Forge utilizes a three-dimensional Cartesian coordinate system to represent object transformations within the editor. This system defines how objects are positioned, rotated, and scaled using three perpendicular axes: X, Y, and Z.

## Transformation Gizmos and Axes

The transformation gizmos allow for precise manipulation of objects along specific dimensions. Each axis is represented by a unique color and rotation type:

* **X-axis (Red):** Represents the X dimension; rotation around this axis is referred to as **Roll**.
* **Y-axis (Green):** Represents the Y dimension; rotation around this axis is referred to as **Pitch**.
* **Z-axis (Blue):** Represents the Z dimension; rotation around this axis is referred to as **Yaw**.

These axes are utilized by the three primary transformation gizmos:

* **Position Gizmo:** Translates objects along the X, Y, and Z axes.
* **Rotation Gizmo:** Rotates objects around the X, Y, and Z axes.
* **Size Gizmo:** Scales objects along the X, Y, and Z axes.

### Shortcuts

Using keyboard modifiers and controller inputs allows for rapid switching between transformation modes:

| Mode | Keyboard | Controller |
| --- | --- | --- |
| Move | `Ctrl+W` | `LT` |
| Rotate | `Ctrl+E` | `RT` |
| Scale | `Ctrl+R` | `LT + RT` |

## Coordinate Spaces

Forge supports multiple coordinate spaces, which determine the reference frame used by the transformation gizmos. These settings are managed via the Movement Type and Rotation Type options.

### World Space

World Space uses the global coordinate system of the Forge environment as its reference frame. When using this mode:
* The transformation axes remain aligned with the world coordinate system regardless of object orientation.
* Transformations are applied relative to the global X, Y, and Z axes.
* This space is most effective when aligning objects in relation to the overall map layout.

### Object Space

Also known elsewhere as Local Space, this mode uses the object's own internal coordinate system as the reference frame:
* The transformation axes follow the object's rotation.
* Transformations are applied relative to the object's current orientation.
* Rotating an object will change the direction of its local transformation axes.

### Camera Space

Camera Space is a rotation mode that uses the editor camera's orientation as the reference frame:
* The rotation axes align with the viewing direction of the editor camera.
* The Rotation gizmo orientation changes dynamically based on the current camera view.
* This mode is useful for making rotation adjustments relative to your specific perspective.

## Rotation System

Object rotation in Forge is represented using Euler angles, where an object's orientation is defined by three separate rotations around the X (Roll), Y (Pitch), and Z (Yaw) axes. These values can be adjusted manually via the Rotation gizmo or through angular snapping.

{% hint style="info" %}
For most forging tasks, applying standard snap values facilitates easier manipulation: use a **1/8'** Movement Snap, **15°** Rotation Snap, and **1/8'** Scaling Snap. 
{% endhint %}

## Grid Snapping

The snapping system allows transformations to occur in predefined increments. Note that Forge snapping is relative; it applies changes from the object's current transformation rather than aligning to absolute world coordinates or fixed values.

### Position and Size Snapping

Both position and size scaling support several distance intervals:
* `<none>`
* `0.001'`
* `1/8'`
* `1/4'`
* `1/2'`
* `1'`
* `2'`
* `4'`
* `8'`
* `16'`

{% hint style="warning" %}
If you find that dragging the axes does not move, scale, or rotate your object as expected, it may be because the current snapping value is too high. You must drag the axis far enough to reach the next snap threshold before any change is visible.
{% endhint %}

### Rotation Snapping

Rotation increments can be adjusted using the following angular intervals:
* `<none>`
* `1/2°`
* `1°`
* `5°`
* `15°`
* `30°`
* `45°`
* `60°`
* `90°`
* `180°`

#### Relative Behavior
Because snapping is relative to the object's current state, position snaps move an object by increments from its *current* location, size snaps change dimensions based on *current* scale, and rotation snaps apply angular changes from the *current* orientation. Snapping does not automatically align objects to absolute world-space coordinates or specific fixed rotations.

***

## Source Data

* Discord thread: [Coordinate System and Spaces](https://discord.com/channels/220766496635224065/1534049250428715021/1534049250428715021)

#### <mark style="color:green;">Contributors</mark>

Okom

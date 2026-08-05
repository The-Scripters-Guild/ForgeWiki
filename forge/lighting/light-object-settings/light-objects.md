# Light Objects

## Light Properties

<figure><img src="../../../.gitbook/assets/light-object-properties-1.png" alt=""><figcaption><p>Light Properties</p></figcaption></figure>

| Property Name                     | Description                                                                                    |
| --------------------------------- | ---------------------------------------------------------------------------------------------- |
| Type                              | Sets the light to be "Spot" (directional) or "Point" (omnidirectional).                        |
| Color                             | Changes the color of light source.                                                             |
| Brightness                        | How bright the light is.                                                                       |
| Outer Cone Angle (Only Spot Type) | Angle/Frustum of the outer spotlight cone. (Reference Image Light Source Outer-Inner Cone)     |
| Inner Cone Angle (Only Spot Type) | Angle/Frustum of the inner spotlight cone.                                                     |
| Source Size                       | Modifies the softness of the light source. (Reference Image Light Source Outer-Inner Cone)     |
| Light Range                       | Distance at which the light falls off.                                                         |
| Cast Static Shadows               | Enables shadows for static objects.                                                            |
| Cast Dynamic Shadows              | Enables shadows for dynamic objects, adds additional expense.                                  |
| Shadow Start Distance             | Distance from source at which the shadows start. (Reference Image Light Shadow Start Distance) |

<figure><img src="../../../.gitbook/assets/light-cone-diagram.png" alt=""><figcaption><p>Light Source Outer-Inner Cone</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/light-cone-diagram-2.png" alt=""><figcaption><p>Light Shadow Start Distance</p></figcaption></figure>

## Animation

{% hint style="info" %}
Animations are used to create Flickering lights
{% endhint %}

<figure><img src="../../../.gitbook/assets/light-animation-settings.png" alt=""><figcaption><p>Animation Properties</p></figcaption></figure>

| Property Name | Description                                                     |
| ------------- | --------------------------------------------------------------- |
| Type          | Applies an animation to the light.                              |
| Rate          | Changes the Light animation Speed (Higher faster, lower slower) |

## Cone

{% hint style="info" %}
Light cones are versatile, cheap to render billboard objects. Used to create fake lighting effects, such as, light rays, fog, mist, smoke. Also used to create depth and pathing.
{% endhint %}

<figure><img src="../../../.gitbook/assets/light-cone-settings.png" alt=""><figcaption><p>Cone Properties</p></figcaption></figure>

| Property Name       | Description                                                                                                                                                              |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Type                | The light cone attached to the object. (Reference Image Types of Light Cones)                                                                                            |
| Intensity           | How bright the light cone is.                                                                                                                                            |
| Length              | Changes the length of the light cone; Stacking multiple light cones over one another, or the larger the light cone takes up on screen, the more performance cost it has. |
| Width               | Changes the width of the light cone; Stacking multiple light cones over one another, or the larger the light cone takes up on screen, the more performance cost it has.  |
| Fade Start          | Distance from player when the light cone starts to fade.                                                                                                                 |
| Fade End            | Distance from player when the light come completely fades.                                                                                                               |
| Enable Parent Light | Toggles the light to be on/off; used when only a light cone is desired.                                                                                                  |

<figure><img src="../../../.gitbook/assets/light-cones.png" alt=""><figcaption><p>Types of Light Cones</p></figcaption></figure>

![Fade Start/End Example](../../../.gitbook/assets/fade-start-end.gif)

![Enable Parent Light Example](../../../.gitbook/assets/enable-parent-light.gif)

## Gobo

{% hint style="info" %}
Gobos are patterns projected from lights to give different lighting results. Examples being water caustics, faking shadows, or placing a Banished logo.
{% endhint %}

<figure><img src="../../../.gitbook/assets/gobo-settings-none.png" alt=""><figcaption><p>Gobo Properties</p></figcaption></figure>

| Property Name    | Description                                                                                                                                                                                           |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gobo Information | There can only be a limit of 4 Unique gobos rendering at the same time. Duplicates work fine, but 5+ gobos in close proximity still rendering will cause the gobos to flicker or not render correctly |
| Type             | Applies a stencil (pattern) projected from the light (Only works on "Spot" lights). (Reference Image Types of Gobos                                                                                   |



<figure><img src="../../../.gitbook/assets/types-of-gobos.png" alt=""><figcaption><p>Types of Gobos</p></figcaption></figure>

## OBB

{% hint style="info" %}
OBB's (Oriented Bounding Box) are used Primarily as a performance tool, clamping light pixels to have more performant heatmaps (Use the Light/Shadow Heatmaps to see light pixel influence)
{% endhint %}

<figure><img src="../../../.gitbook/assets/obb-settings.png" alt=""><figcaption><p>OBB Properties</p></figcaption></figure>

| Property Name          | Description                                                                    |
| ---------------------- | ------------------------------------------------------------------------------ |
| Enable OBB             | Toggles on/off OBB (Reference Images below )                                   |
| Scale with Light Range | Automatically scales the bounds if ""Light Range" changes                      |
| Lower X Bound          | Moves 1 side of the bounding box, setting can not be higher than Upper X Bound |
| Upper X Bound          | Moves 1 side of the bounding box, setting can not be higher than Lower X Bound |
| Lower Y Bound          | Moves 1 side of the bounding box, setting can not be higher than Upper Y Bound |
| Upper Y Bound          | Moves 1 side of the bounding box, setting can not be higher than Lower Y Bound |
| Bottom                 | Moves the Bottom of the Volume                                                 |
| Top                    | Moves the Bottom of the Volume                                                 |
| Show                   | Always render OBB Volume                                                       |

<figure><img src="../../../.gitbook/assets/obb-adjusted.png" alt=""><figcaption><p>OBB Adjusted</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/obb-default.png" alt=""><figcaption><p>OBB Default</p></figcaption></figure>

![Debug On/Off](../../../.gitbook/assets/debug-on-off.gif)

#### Contributors

Nitro\
Tyler | Lighting Artist\
Captain Punch

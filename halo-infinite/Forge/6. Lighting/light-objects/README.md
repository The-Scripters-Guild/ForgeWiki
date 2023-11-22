# Light Objects

## Light Properties

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Light Properties</p></figcaption></figure>

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

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption><p>Light Source Outer-Inner Cone</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Light Shadow Start Distance</p></figcaption></figure>

## Animation

{% hint style="info" %}
Animations are used to create Flickering lights
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Animation Properties</p></figcaption></figure>

| Property Name | Description                                                     |
| ------------- | --------------------------------------------------------------- |
| Type          | Applies an animation to the light.                              |
| Rate          | Changes the Light animation Speed (Higher faster, lower slower) |

## Cone

{% hint style="info" %}
Light cones are versatile, cheap to render billboard objects. Used to create fake lighting effects, such as, light rays, fog, mist, smoke. Also used to create depth and pathing.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Cone Properties</p></figcaption></figure>

| Property Name       | Description                                                                                                                                                              |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Type                | The light cone attached to the object. (Reference Image Types of Light Cones)                                                                                            |
| Intensity           | How bright the light cone is.                                                                                                                                            |
| Length              | Changes the length of the light cone; Stacking multiple light cones over one another, or the larger the light cone takes up on screen, the more performance cost it has. |
| Width               | Changes the width of the light cone; Stacking multiple light cones over one another, or the larger the light cone takes up on screen, the more performance cost it has.  |
| Fade Start          | Distance from player when the light cone starts to fade.                                                                                                                 |
| Fade End            | Distance from player when the light come completely fades.                                                                                                               |
| Enable Parent Light | Toggles the light to be on/off; used when only a light cone is desired.                                                                                                  |

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Types of Light Cones</p></figcaption></figure>

Types of Light Cones

![Fade Start/End Example](https://imgur.com/r24sdoX.gif)

![Enable Parent Light Example](https://imgur.com/vnxpPHU.gif)

#### Contributors

Nitro\
Tyler | Lighting Artist\
Captain Punch

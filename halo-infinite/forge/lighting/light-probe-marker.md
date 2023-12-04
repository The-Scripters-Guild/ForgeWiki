# Light Probe Marker

## Light Probe Marker

A manually placed Light probe volume. Within this volume will be air probes which will contribute to your indirect lighting. A good example to use this is for Caves, Interiors, Bunkers or to get high density probes in a small location. This can be used in combination with the Level Bound Volume (which is just an automatic volume placed).

{% hint style="info" %}
Only 1 can be manually placed
{% endhint %}

<figure><img src="../../../.gitbook/assets/light-probe-volume-settings.png" alt=""><figcaption><p>Light Probe Marker Properties</p></figcaption></figure>

| Property Name         | Description                                                                                                                                                                                                                                           |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Width                 | Adjusts Width                                                                                                                                                                                                                                         |
| Length                | Adjusts Length                                                                                                                                                                                                                                        |
| Height                | Adjusts Height                                                                                                                                                                                                                                        |
| Probe Spacing         | The Horizontal and Vertical distance between generated probes. Smaller spacing will have more accurate bounce results but longer build times.                                                                                                         |
| Show                  | Display's the volumes objects boundary.                                                                                                                                                                                                               |
| Predicted Probe Count | The amount of probes that will be generated when building lighting. This is shared between the Light probe Marker object and the Level Bound Probes. More probes mean longer build time and exceeding the budget will prevent lighting from building. |

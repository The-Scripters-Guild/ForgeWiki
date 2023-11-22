# Level Bound Probes

## Level Bound Probes

Level bound probes to rendering your indirect for the map. Level stretching across the whole map, object scaling based on player placed objects, or none. (No level volume)

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>Level Bound Probes Properties</p></figcaption></figure>

| Property Name | Description                                                                                                                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bounding Type | <p>2 sets of bounding probes: (Reference Image Bounding Type Level &#x26; Object)</p><ul><li>Level: Will encompass the entire gameplay canvas</li><li>Object: Will automatically encompass all player placed objects in the scene</li></ul> |
| Probe Spacing | Sets distance between probes; Lower spacing will result in more accurate indirect lighting, but increased build times. Higher spacing will result in less accurate but faster build times.                                                  |
| Probe Count   | Estimates the number of probes based on probe spacing. This is shared between the "Level Bound Probes" and "Light Probe Marker" object. More probes will result in longer build times.                                                      |

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Bounding Type Level</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption><p>Bounding Type Object</p></figcaption></figure>

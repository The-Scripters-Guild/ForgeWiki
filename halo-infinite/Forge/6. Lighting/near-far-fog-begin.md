# Near/Far Fog Begin

Near/Far Begin is a versatile optimization tool used in lighting to enhance visual quality and improve performance, especially in scenarios involving unmotivated lights or complex environments.

**Functionality:**

* **Near Begin:** This parameter determines where the light rendering begins, originating from the Light object. It serves a crucial role in optimization by stopping the rendering of pixels, effectively minimizing computational load. Near Begin acts as a boundary for rendering, preventing unnecessary pixel calculations.
* **Far Begin:** Also starting from the light source, Far Begin softens the edge created by Near Begin. By defining the boundary between illuminated and non-illuminated areas, Far Begin ensures a smooth transition. Without this parameter, a harsh seam akin to an Oriented Bounding Box (OBB) would be visible.

**Usage Scenarios:**

1. _Faking Light:_ Near/Far Begin can be used to simulate natural light sources, such as sunlight or smaller fixtures, by spreading light effectively. By adjusting Near and Far Begin values, one can conceal artificial lighting, avoiding noticeable specular highlights.
2. _Large Forerunner Rooms:_ In expansive environments, especially Forerunner-style rooms, point lights with tweaked Near and Far Begin values create hollow centers while generating lights at the outer bounds. This technique enables the creation of rim lights and specular hits without cluttering the space with additional light sources.
3. _Optimizations:_ Applying Near/Far Begin settings to all lights can significantly optimize rendering. By excluding the top portions of spotlights from calculations, fewer pixels are processed, enhancing overall performance. Utilizing this optimization across all lights collectively improves performance, contributing to a more efficient rendering pipeline.
4. _Organic Maps:_ In organic environments like caves, where curved surfaces complicate the use of Oriented Bounding Boxes (OBBs), Near/Far Begin settings prove invaluable. These parameters minimize overlap and optimize lighting calculations in intricate, curved spaces, ensuring a visually appealing result without sacrificing performance.

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-1 (5).png" alt=""><figcaption></figcaption></figure>

Here is an example of default lights and their heatmaps. Notice how the more pixels are being affected near the source of the lights.

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-1 (6).png" alt=""><figcaption></figcaption></figure>

And lastly here is an example of Far begin, Where is softens the edges but it doesn't contribute to cutting off Pixels. Only Near begin does that.

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-1 (7).png" alt=""><figcaption></figcaption></figure>

**Contributors** \
Tyler | Lighting Artist\
Captain Punch

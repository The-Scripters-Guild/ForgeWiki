# Oriented Bounding Box (OBB)

Oriented Bounding Box, commonly referred to as OBB, is a crucial feature in lighting that allows precise adjustment of the area affected by light pixels. This tool is invaluable for resolving issues related to shadow overlaps and light bleeding, enhancing both visual quality and performance optimization.

**Key Features:**

* **Enable OBB:** This option toggles the OBB feature on or off.
* **Scale with Light Range:** Automatically adjusts the bounding box as the light range changes, ensuring it stays within defined bounds.
* **Bounding Box Faces (Lower X, Y, Upper XY, Top, Bottom):** These parameters enable adjustment of the faces of the OBB, determining the exact boundaries of the affected area.
* **Orientation (Yaw, Pitch, Roll):** Allows rotation of the OBB, providing flexibility in aligning the bounding box with the scene's geometry.
* **Show:** Activates a visual representation of the OBB, aiding in visualization without selecting or highlighting objects.

**Usage Guidelines:**

* When rotating the OBB, utilize the Yaw, Pitch, Roll options. Note that the rotation occurs independently from the light source, requiring careful consideration during adjustments. It's advisable to finalize lighting placement before fine-tuning the OBB to avoid unnecessary rework.

**Practical Applications:**

1. _Optimizations:_ OBB plays a pivotal role in optimizing the lighting pass. By precisely defining the affected area, unnecessary computations are minimized, leading to substantial performance improvements while preserving the desired visual outcome.
2. _Fog-Only Lights:_ For scenarios requiring fog-only illumination (with volumetric fog enabled), configuring the light's OBB with minimal parameters (e.g., -.1 and .1) restricts the light emission to a confined area, generating fog without casting extensive illumination. This method optimizes volumetric fog usage efficiently.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image-1 (8).png" alt=""><figcaption></figcaption></figure>

**Issues:**&#x20;

This does create a harsh seam where you clamp the OBB. This can be seen in the environment and characters.Try to avoid this as best as possible and put the seam on edges or seams to be less noticeable.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



**Contributors** \
Tyler | Lighting Artist\
Captain Punch

---
description: >-
  A method for detecting player proximity to dynamically spawned
  objects in mode-only environments by cycling a limited pool of
  Generic Zones through object positions.
---

# Mode-Based Player Proximity Detection to Objects via Spawned Generic Zones

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

In certain game modes, such as Battle Royale, all game elements must be loaded directly from the mode script without on-level modifications. In these environments, `Area Monitors` attached to objects spawned via `Spawn Mode Object` are non-functional. This makes standard proximity detection difficult without performing heavy loops through all players and objects, which can cause significant tick rate drops. This article describes a method to achieve efficient proximity detection by using a cycling pool of `Generic Zones` attached to the Mode Brain.

## Detection Methodology

To circumvent the limitations of `Area Monitors` on spawned objects, `Generic Zones` can be used as proxies for proximity detection. These zones are attached to the Mode Brain script and are positioned at the locations of target objects using the `Spawn Mode Object` node.

### Implementation via Mode Script

The detection workflow follows these steps:

* Attach multiple `Generic Zones` to the Mode Brain.
* Spawn these zones at the specific positions of the objects requiring proximity detection (e.g., loot boxes).
* Utilize the `On Capture Zone Entered` event to trigger detection logic.
* Upon entry, detect the position of the player who entered the zone.
* Compare the player's position against a list of target objects to find the closest one.
* Execute the intended action, such as opening or interacting with the object.

This approach maintains a stable 60 tick rate because the logic only loops through the object list once per zone entry, rather than constantly checking every player against every object.

## Performance Optimization and Scaling

To manage a large number of objects without spawning an equal number of zones, a "zone cycling" method can be implemented. Instead of a static 1:1 ratio of zones to objects, a smaller pool of zones can be moved between object positions every tick.

### Preventing Overlap and Double Detection

To prevent a single player from triggering proximity detection multiple times, the number of active zones can be limited. A suggested formula to prevent overlapping zones is:

`Total Zones = Total Objects / 4`

By using this ratio and staggering the initialization of each zone by a delay of 0.0666 seconds (approximately 4 ticks), the system ensures that zones do not overlap on the same or adjacent ticks. This ensures that proximity detection is triggered reliably, with a detection occurring roughly every 4 ticks.

### Maintaining Consistency via Object Management

When an object is interacted with (e.g., a loot box is opened), deleting the object can change the total object count. If the object count decreases, the calculated number of zones required for the cycling logic also changes, which can cause the delay between zone movements to become inconsistent.

To maintain a constant delay between zone updates, objects can be moved under the map instead of being deleted. This keeps the total number of objects in the loop consistent, ensuring the cycling timing remains stable.

{% hint style="success" %}
Using a staggered initialization approach (e.g., a 4-tick delay between zone updates) prevents the risk of multiple proximity detections being triggered by overlapping zones.
{% endhint %}

## Technical Constraints

While effective, this method has specific requirements and observed behaviors that must be accounted for during implementation.

#### Requirement for Separate Zone Objects

It is not possible to use a single `Generic Zone` object to detect multiple areas simultaneously. Attempting to use one zone for multiple detections results in a behavior where, despite multiple zones being present, only the last one fires the `On Capture Zone Entered` event. Therefore, a unique zone object must be used for each active detection area.

#### Capacity Limits

The capacity of this method is limited by the number of `Generic Zones` that can be attached to the Mode Brain. For example, if 70 zones are attached, the system can reliably support up to 280 proximity-requiring objects (70 zones * 4) without noticeable detection delays.

***

## Source Data

* Discord thread: [https://discord.com/channels/220766496635224065/1474057592236933282/1474057592236933282](https://discord.com/channels/220766496635224065/1474057592236933282/1474057592236933282)

#### <mark style="color:green;">Contributors</mark>

Okom\
Toast\
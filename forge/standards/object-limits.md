---
description: >-
  An analysis of Forge object limits, focusing on the Forge Simulation
  and Static Geometry budgets and the impact of telescoping objects.
---

# Object Limits

<figure><img src="../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Forge maps are constrained by several different budgets. The total number of objects allowed depends on which specific budget is exhausted first, with the Forge Simulation budget and the Static Geometry budget being the most common limiting factors.

## Forge Budgets

The object limit in a Forge map is not a single fixed number but changes based on the resource usage of the objects placed.

### Forge Simulation Budget

The Forge Simulation budget is frequently the first limit encountered. Research using highly efficient, primitive pieces—such as `Primitive Block`, `Primitive Sphere`, and `Floor Angled Standard A`—has shown limits in the range of approximately 5658 to 5664 objects.

As updates to the Forge tool introduce more object properties and adjustments, the Forge Simulation budget can be reached more quickly. A common symptom of reaching this limit is that item spawners, such as Weapon Racks or Vehicle Spawners, may reset to their default properties.

<figure><img src="../../.gitbook/assets/HaloInfinite_ThOLSt2Zlj.jpg" alt="Primitive blocks and spheres"><figcaption><p>Primitive objects like blocks and spheres are used to test Forge Simulation limits.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/HaloInfinite_ln0SksJmQq.jpg" alt="Primitive spheres"><figcaption><p>Primitive spheres represent highly efficient objects for budget testing.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/HaloInfinite_RiAP7j2jet.jpg" alt="Floor Angled Standard A"><figcaption><p>Standard angled floors are among the simplest objects used in budget analysis.</p></figcaption></figure>

### Static Geometry Budget

The Static Geometry budget is determined by the number of static meshes contained within an object. "Telescoping" objects, such as specific floor and wall pieces, are particularly resource-intensive because they are composed of multiple individual static meshes.

The capacity for these objects varies depending on their complexity:

* **UNSC Stairs:** Approximately 5461 objects (3 telescoping parts)
* **Covenant Pyramids:** Approximately 810 objects (~7 telescoping parts)
* **UNSC Walls:** Approximately 630 objects (~8 telescoping parts)

<figure><img src="../../.gitbook/assets/HaloInfinite_EBQi16ckkJ.jpg" alt="UNSC Stairs"><figcaption><p>UNSC Stairs consist of multiple telescoping parts that impact the Static Geometry budget.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/HaloInfinite_5FeqeLFKtg.jpg" alt="Covenant Pyramids"><figcaption><p>Covenant Pyramids utilize several telescoping parts, increasing their mesh count.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/HaloInfinite_IUgn0PCII8.jpg" alt="UNSC Walls"><figcaption><p>UNSC Walls have a high number of telescoping pieces, making them expensive for Static Geometry.</p></figcaption></figure>

## Telescoping Object Research

Research has been conducted to determine if telescoping objects impact budgets differently than standard primitive objects. In a test where 500 worst-case telescoping objects (UNSC Floors) were compared against 500 `Primitive Spheres`, the usage for the Forge Simulation and Objects budgets remained exactly the same. 

This indicates that telescoping objects primarily affect the Static Geometry budget.

<figure><img src="../../.gitbook/assets/HaloInfinite_UbKcFWcfnl.jpg" alt="UNSC Floors test"><figcaption><p>Placing 500 UNSC Floors can cause the Static Geometry budget to reach its limit first.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/HaloInfinite_df22yZg6T2.jpg" alt="Primitive Spheres comparison"><figcaption><p>Replacing telescoping objects with primitive spheres shows identical usage for Forge Simulation and Objects budgets.</p></figcaption></figure>

{% hint style="warning" %}
Telescoping objects are only a major concern if your map is constructed primarily out of expensive telescoping pieces, which may cause the Static Geometry budget to be hit before other limits.
{% endhint %}

## Additional Data

* **Terminals:** All terminals, including Worn Forerunner variants, occupy the same amount of space.
* **Custom Events:** There is a negligible difference in space usage between Custom Events, Global Custom Events, and Async types.

***

## Source Data

* Discord thread: [Object Limit and Telescoping Object Research](https://discord.com/channels/220766496635224065/1434256456345059328/1434256456345059328)

#### <mark style="color:green;">Contributors</mark>

Okom\
Runic
---
description: >-
  Because there is no dedicated "Get All Vehicles" node, managing
  vehicles—such as clearing cloned objects or deleting specific
  AI-driven vehicles while preserving others—requires custom logic.
  There are two primary approaches: identifying vehicles by scanning
  spawned objects or manually tracking them via a global list.
---

# How To Get All Vehicles on Map

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Because there is no dedicated "Get All Vehicles" node, managing vehicles—such as clearing cloned objects or deleting specific AI-driven vehicles while preserving others—requires custom logic. There are two primary approaches: identifying vehicles by scanning spawned objects or manually tracking them via a global list.

## Identifying Vehicles via Spawn Order

One method to find vehicles is to iterate through objects based on their spawn order. All cloned objects are automatically assigned a `Spawn Order (0)`.

### Detection Logic

To differentiate a vehicle from a standard object, you can use a comparison logic. By utilizing the `Are Same Vehicle Type` node (or potentially `Get Is Vehicle Type`), you can test an object against a known non-vehicle object.

* **Process:** Use `Get Objects With Spawn Order (0)` to retrieve a list of dynamic objects.
* **Comparison:** Feed the object from the list and a non-vehicle object into the `Are Same Vehicle Type` node.
* **Identification:** If the node returns a `False` output, the object is identified as a vehicle.

#### Performance Considerations

Using this method requires caution regarding script performance. Iterating through a list of all objects with `Spawn Order (0)` can cause momentary lag, as this list typically contains most dynamic objects currently active on the map. It is recommended to avoid running this check too frequently.

## Manual Vehicle Tracking

A more performance-efficient method involves maintaining your own record of vehicles. This avoids the need to scan all dynamic objects on the map.

### Using Global Object Lists

Instead of searching for vehicles after they appear, you can track them at the moment of creation.

* **Initialization:** Create a global variable that functions as an object list.
* **Adding Objects:** Every time an object is cloned or a specific vehicle (such as a Wraith or a Spawner) is added to the map, add that object to your global list.
* **Management:** When you need to perform an action, such as deleting excess vehicles or applying markers, you can iterate through your specific list rather than the entire map's object pool.

{% hint style="success" %}
For complex scripts or maps with many dynamic objects, use a manual global list to prevent performance drops caused by scanning all spawned objects.
{% endhint %}

***

## Source Data

* Discord thread: [Get All Vehicles?](https://discord.com/channels/220766496635224065/1446920516123365529/1446920516123365529)

#### <mark style="color:green;">Contributors</mark>

Runic\
Okom
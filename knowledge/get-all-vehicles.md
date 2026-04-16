---
description: >-
  Methods for identifying and managing vehicles on a map when a
  dedicated "Get All Vehicles" node is unavailable.
---

# Get All Vehicles?

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

Because there is no direct node to retrieve a list of all vehicles currently on a map, developers must use logical filtering or custom tracking systems to identify, manage, or delete vehicles.

## Identifying Vehicles via Spawn Order

One method for identifying vehicles involves iterating through dynamic objects using their spawn order. This approach allows you to filter through objects on the map to find specific types.

### Type Comparison Logic

To differentiate vehicles from other objects, you can use the `Are Same Vehicle Type` node (or `Get Is Vehicle Type`). The comparison process typically follows these steps:

* Use `Get Objects With Spawn Order (0)` to retrieve a list of dynamic objects.
* Pass the object from the list and a known non-vehicle object into the `Are Same Vehicle Type` node.
* A `False` output indicates that the object is a vehicle.

#### Performance Considerations

Using `Get Objects With Spawn Order (0)` frequently can result in momentary lag. This is because the process requires iterating through most dynamic objects currently active on the map.

## Manual Tracking via Global Lists

A more performance-efficient alternative to scanning the map is to maintain a custom list of vehicles using a global variable. This method avoids the need to iterate through all dynamic objects.

* Create a global variable that holds an object list.
* Every time an object is cloned, add that object to the list.
* When a vehicle (such as a Wraith or Spawner) is added to the map, manually add it to this list.
* Use this list to perform actions, such as deleting specific vehicles, when needed.

{% hint style="success" %}
Using a global list to track spawned vehicles is generally more efficient and produces less lag than scanning all objects with Spawn Order 0.
{% endhint %}

***

## Source Data

* Discord thread: [Get All Vehicles?](https://discord.com/channels/220766496635224065/1446920516123365529/1446920516123365529)

#### <mark style="color:green;">Contributors</mark>

Runic\
Okom
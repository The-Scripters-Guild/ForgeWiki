---
description: >-
  A script module that assigns custom weapons to vehicles, including
  automatic turret assignment for Warthogs and Rockethogs.
---

# tsg grantVehicleWeapon

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

`tsg grantVehicleWeapon` is a script module designed to equip vehicles with custom weaponry. It functions by assigning a demonstration weapon, sourced from a designated "yellow brain," to a target vehicle via a ping.

## Weapon Assignment and Turret Logic

The module facilitates the assignment of specialized weapons to vehicles. When the script is triggered, it assigns the demonstration weapon from the yellow brain to the selected vehicle.

### Turret Compatibility

The script includes logic to handle specific vehicle configurations for mounting weaponry. For vehicles such as the Warthog and Rockethog, the assigned weapons are automatically routed to their respective turrets.

## Implementation and Customization

To provide the weapon, the script clones the weapon held by a Rockethog or Wasp to extract its Base Weapon. This Base Weapon is then added to a [Weapon Type](../../../scripting/nodes/variables-basic/weapon-type.md) Configuration that is provided to the vehicle.

### Networking Constraints

{% hint style="warning" %}
In networked environments, vehicles seem to only accept weapon types that are specifically flagged as vehicle weapons. Attempting to grant a standard weapon that lacks this flag may not work.
{% endhint %}

### Combat Tuning

The module offers several options for adjusting how the vehicle performs in combat:

* **Damage Adjustment:** An optional feature allows for the modification of the assigned vehicle weapon's damage.
* **Shot Cadence:** As of version 1.1.0, the `vehicleShotCadence` variable can be used to adjust the delay between shots of the assigned vehicle weapon.

[tsg grantVehicleWeapons (mode prefab)](https://www.halowaypoint.com/halo-infinite/ugc/modes/08eec092-a5b0-4c1d-9a18-61e13c0d58df)
[Custom Vehicle Weapons demo (map)](https://www.halowaypoint.com/halo-infinite/ugc/maps/c9082ec4-0632-4ff8-9867-b43991ff6222)

***

## Source Data

* Discord thread: [tsg grantVehicleWeapon](https://discord.com/channels/220766496635224065/1422405275591376946/1422405275591376946)

#### <mark style="color:green;">Contributors</mark>

Okom
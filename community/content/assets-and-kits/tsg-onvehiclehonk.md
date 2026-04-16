---
description: >-
  A script module for detecting vehicle honks or firing actions
  without causing unintended weapon side effects.
---

# tsg onVehicleHonk

<figure><img src="../../../.gitbook/assets/cover-tsg-placeholder.jpg" alt="Cover image"><figcaption></figcaption></figure>

`tsg onVehicleHonk` is a script module designed to detect when a vehicle driver honks or fires. This module provides a more reliable alternative to previous methods that required nullifying weapon damage, which could lead to unintended consequences for the driver.

## Detection Mechanism

The module avoids the side effects of traditional weapon-based detection by utilizing the `Spawn Mode Object` node's capabilities. Instead of providing a weapon that might accidentally deal damage, the system duplicates a pre-placed weapon that has been configured with a nearly empty magazine that actually fires no projectile, but still processes the `On Weapon No Ammo` node.

### Weapon Configuration

A specific weapon, such as a Plasma Cannon, is placed in the map with its Spare Energy set to 0.001. This configuration ensures the weapon has a single "blank" shot remaining. When the driver fires, the `On Weapon No Ammo` node is triggered, which the script uses to detect the action. The logic then filters these events to ensure the trigger is specifically linked to a weapon held by a vehicle. The script also handles the cleanup of this weapon if the vehicle is destroyed.

## Vehicle Integration

To use this module, it must be marked to apply the honk detection to a vehicle. During the application process, the script nulls out the existing weapon in the vehicle's inventory.

### Tuning and Cadence

While the driver may still experience local visual and auditory feedback of the honk, the action is not visible or audible to other players. Users can adjust the delay between successive honk detections by utilizing the `vehicleShotCadence` variable.

{% hint style="success" %}
By using a low-energy duplicate weapon instead of a damage-disabled weapon, drivers can maintain their full damage potential while still allowing for reliable honk detection.
{% endhint %}

***

## Source Data

* Discord thread: [tsg onVehicleHonk](https://discord.com/channels/220766496635224065/1449844004077179025/1449844004077179025)

#### <mark style="color:green;">Contributors</mark>

Okom

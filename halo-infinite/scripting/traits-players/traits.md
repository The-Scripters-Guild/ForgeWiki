# Traits

## Traits

### Specific Traits

#### Prevent Weapon Firing

The Prevent Weapon Firing trait prevents players from firing weapons but also disables melee attacks, even if the player is using a non-melee weapon like a pistol.

#### Active Camo VFX

The active camo VFX trait can remove player outlines, with a minimum scalar of 0.5 needed for the effect to take place. However, at this scalar, players appear translucent and ghost-like. The scalar threshold for fully opaque appearance is dependent on lighting. Players must also be aware that there is a threshold of speed at which the active camo effect goes away and outlines will reappear. Furthermore, having the camo trait tells bots not to sprint.

### Non-Trait-Specific Notes

#### Duplicates of traits that use scalars will apply multiplicatively

When multiple trait sets are applied to a player and they contain the same trait that uses a scalar, the trait is applied multiplicatively. For example, if a player has a Movement Speed trait with a scalar of 2 and another with a scalar of 0.5, the total speed of the player will be scalar 1 (2 x 0.5 = 1). However, if a player has a Jump Height trait with a scalar of 4 and another with a scalar of 0, the total jump height of the player will be scalar 0 (4 x 0 = 0). In the case of a Damage Resistance scalar of 3 and another with a scalar of 4, the total damage resistance scalar of the player will be 12 (3 x 4 = 12).

**Contributors**\
Captain Punch \
DeceitfulEcho

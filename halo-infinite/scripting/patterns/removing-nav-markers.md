# Removing Nav Markers

## Steps to Hide a Nav Marker

1. Connect the "Set Nav Marker Enabled" node to your string.
2. Change the "Enabled" setting to `false`.
3. Connect a Nav Marker node to the "Set Nav Marker Enabled" node's nav marker slot.
4. Set the Nav Marker identifier to match the nav marker you want to remove.

This will hide the nav marker, making it invisible. However, the nav marker remains attached to the object.

## Removing Nav Markers from Specific Objects

There is no straightforward method to remove nav markers from specific objects without affecting others. To completely dissociate a nav marker from an object, you need to despawn the object.

### Despawning Objects to Detach Nav Markers

Despawning objects breaks nav marker attachments to them and can be used as a way to 'rinse' them off. This is the only way to dissociate objects from nav markers. After despawning an object, the nav marker will not be attached to the object when you re-enable it.

#### Contributors
Captain Punch
# Hiding Objects During Nav Mesh Generation

This wiki entry explains how to hide objects in the forge menu during navmesh generation to prevent interference.

### Using Folders to Hide Objects

<figure><img src="../../../../.gitbook/assets/hiding-objects-for-nav-mesh-generation.gif" alt=""><figcaption></figcaption></figure>

1. Access the "Folders" section in the forge menu, which contains a list of every placed object on your map.
2. Create subfolders for specific object categories (e.g., Foliage, Blockers).
3. Add relevant objects to their respective subfolders.
4. Click the "eye" button to hide all objects within the folder.

With objects hidden, you can safely generate navmesh.

### Managing Large Amounts of Objects

* It is possible to add up to 150 objects to a folder at a time.
* Adding too many objects at once can increase the risk of a crash.

**Recommendation**: Save before and between each large folder action to avoid potential crashes.

**Contributors**\
Scrubulba\
Captain Punch

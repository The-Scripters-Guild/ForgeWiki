# Object Forward and Up Vectors

In computer graphics and video game development, the Object Forward and Up vectors are unit vectors that describe the orientation of an object relative to its local coordinate system, also known as ObjSpace. These vectors have the following properties:

- They are unit vectors of length 1 with XYZ components each between 0 and 1.
- They are totally independent of object location.
- They match the world unit X and Z vectors after being given the object's rotation.
- The object LEFT vector matches the rotated world Y unit vector.
- They can be calculated with CrossProduct(UP, FORWARD).

In ObjSpace, FORWARD, LEFT, and UP are the XYZ unit vectors, which can work just like World Space but with the object position as the origin and XYZ coordinates as scalar displacements from the origin along the FORWARD, LEFT, and UP directions.

For instance, if an object has ObjSpace coordinates of {7, 8, 9}, then the relative world offset from the object is:

<offset> = 7<FORWARD> + 8<LEFT> + 9<UP>

The world coordinates are:

<objLocation> + <offset>

To get those ObjSpace {XYZ} scalars, you can get the world offset:

<offset> = <coords> - <objLocation>

Then, you can project the offset to ObjSpace units using DotProduct:

X = <offset>•<FORWARD>

Y = <offset>•<LEFT>

Z = <offset>•<UP>

It is important to note that the DotProduct maps the offset <Vec3> to each object <Vec3> and returns a scalar for X, Y, or Z.

#### Contributors
Captain Punch
Shambullz (Yumudas)
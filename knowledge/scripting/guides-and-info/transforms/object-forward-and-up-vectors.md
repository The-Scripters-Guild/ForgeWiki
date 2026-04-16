# Object Forward and Up Vectors

## Object Forward and Up Vectors

In computer graphics and video game development, the Object Forward and Up vectors are unit vectors that describe the orientation of an object relative to its local coordinate system, also known as ObjSpace. These vectors have the following properties:

* They are unit vectors of length 1 with XYZ components each between 0 and 1.
* They are totally independent of object location.
* They match the world unit X and Z vectors after being given the object's rotation.
* The object LEFT vector matches the rotated world Y unit vector.
* They can be calculated with CrossProduct(UP, FORWARD).

In ObjSpace, FORWARD, LEFT, and UP are the XYZ unit vectors, which can work just like World Space but with the object position as the origin and XYZ coordinates as scalar displacements from the origin along the FORWARD, LEFT, and UP directions.

For instance, if an object has ObjSpace coordinates of {7, 8, 9}, then the relative world offset from the object is:

\= 7 + 8 + 9

The world coordinates are:

\+

To get those ObjSpace {XYZ} scalars, you can get the world offset:

\= -

Then, you can project the offset to ObjSpace units using DotProduct:

X = •

Y = •

Z = •

It is important to note that the Dot Product maps the offset to each object and returns a scalar for X, Y, or Z.

**Contributors**\
Captain Punch\
Shambullz (Yumudas)

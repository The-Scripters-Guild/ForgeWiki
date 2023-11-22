# Object Pools

A Object pool is a list of objects that are used for the same thing. It is used when you need multiple instances of a single object.

## Why use a Object pool?

If you just have an object reference to a wall on the map and you spawn that, it will always try to spawn that specific wall. If you try to use the equipment multiple times, or if you have multiple players using their equipment you would only ever have one wall at a time. A Object pool could be used to make sure it spawns a different wall each time.

## How to create a Object pool

1. Create an object list variable and fill it with many object references. This is your Object pool.
2. Create a number variable with an initial value of 1. This is the current index of the Object pool.
3. To prevent objects from the pool from persisting on the map when the game starts, create an On Game Start trigger and call Delete Object on all the objects in the Object pool.

## How to use a Object pool

1. Retrieve your object list variable that is the Object pool and retrieve the number variable that is its current index.
2. Retrieve the object at the current index.
3. If your current code uses that object, increment the index, but make sure the index loops between 1 and the list length. (`index = (index % list_length) + 1`)
4. Now you can do whatever you want with the object.

### Limitations of Object pools

- Object pools cannot make true unique instances of an object. Eventually, your Object pool will loop back to the start and you will reuse objects.
- Be careful when using nodes that take time to finish running (e.g. Wait N Seconds, Move Object to Transform) as long-running triggers can cause issues where your script tries to use the wrong object from the Object pool.
- Consider setting a variable on the object from the Object pool when you use it to track if it's in use, so you can despawn it before reusing it.

## Example Scripts

### Object Pool Setup Script

Note that the object references in the object list are all different. The Object pool does not literally make copies of an object, you need to set up copies somewhere on the map to make hard references to. This means the objects could be different, but you don't usually want them to be much different.

IMAGE


### Using Object From Pool Script

In the above example, the trigger could be anything you want to do with the object from the spawning pool. You could spawn it or move it or whatever you want. If you want to use this within a trigger, link the trigger to the `Set Number Variable` node.


IMAGE


#### Contributors
Captain Punch
Deceitful Echo

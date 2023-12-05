# Get Random N Objects

### Function

Takes an input list and provides N objects from it, selected randomly and in a random order.

### Caveats

This node will only return up to X-1 objects, where X is the size of the input list. \
\
This is especially prevalent when the list being pulled from has a dynamic size and could potentially only have a single object in it, or if Get Random N Objects is being used to randomize the order of a list.\
\
To get around this issue, the solution is to take the input list and combine it with the output of the Get Random N Objects node. This will take the missing object and add it to the end of the list.

**Contributors**\
Captain Punch\
VidGamesPete

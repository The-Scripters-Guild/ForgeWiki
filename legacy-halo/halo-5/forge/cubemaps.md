# Cubemaps

Whenever I start a map nowadays, I build it with the location of the cube map in mind. It is a very useful piece of knowledge to have so I thought I'd spread the love and share what I know. In the spoiler below is a list of all the cube map locations.

<details>

<summary>Cube Map Locations</summary>

**PARALLAX**:\
Blue Planet = -700,\~2000,\~1750 (outside forgeable space)\
Exosphere = 0,0,0\
Ascendence = -700,\~2000,\~1750 (outside forgeable space)\
Halo Ring = 0,0,0

**TIDAL** Paradise = 0,0,120\
Stormy = 0,0,120\
Meteor Shower = 0,0,120\
Clear = 0,0,-248

**ALPINE**\
Cirrus = -200,-80,-30\
Sunset = -200,-80,-30\
Overcast = -200,-80,-30

**GLACIER**\
Midday = 50,-90,230\
Nighttime = 50,-90,230\
Sunrise = 50,-90,230

**BARRENS**\
Twilight = 0,0,0\
Dust Storm = 0,0,48\
Sunrise = 0,0,60

**DEPTHS**\
Depths = 0,0,24

</details>

I will try to revisit this list every once in a while to keep it up to date, I believe 343 has moved the cube map locations around before. If you think a location has moved, shoot me a message and I will update the list with the new one.

Don't have any idea what a cube map is or what I'm talking about?

<details>

<summary>What's a Cube Map and What Does It Do?</summary>

**What is a cube map?** Ripped from wikipedia: "In computer graphics, **cube mapping** is a method of environment **mapping** that uses the six faces of a **cube** as the **map** shape. The environment is projected onto the sides of a **cube** and stored as six square textures, or unfolded into six regions of a single texture."

<img src="https://upload.wikimedia.org/wikipedia/commons/e/e2/Panorama_cube_map.png" alt="Cube Map Example" data-size="original">

Example:

<img src="http://learnopengl.com/img/advanced/cubemaps_skybox.png" alt="Skybox Example" data-size="original">

This is part of how the skybox surrounding each forge space is created.

Often when a forger refers to the cube map, they are talking about a unique cube that the map creates and then uses to project surface reflections onto the forge pieces. Think of a 360° camera that snaps a picture of your map from a single point somewhere on the canvas. This picture is created every time the user generates lighting.

Another nice little picture I found on Google:

<img src="https://www.panda3d.org/manual/images/7/7c/Mapped_cube_map.png" alt="Mapped Cube Map" data-size="original">

So when the 360° camera looks up into the sky in the example above, it snaps a picture of the 4. And when players look down at a surface (the yellow surface in the picture) which is reflecting what's above it, they will see the 4.

</details>

<details>

<summary>What Can Be Done with a Cube Map?</summary>

**What can be done with a cube map?**

Now that we know the location of a cube map and how it works, we can control the reflections that are projected onto the forge pieces within the map!

For example, one could surround the cube map location in a box. If the box is dark, all reflections will be dark. This is one way I like to darken my maps. The box could also be colored. But for the cube map to see the color, there needs to be a light inside the box. A yellow box will add a yellow hue to your entire map.

<img src="http://i.imgur.com/5G4Adgu.jpg" alt="Example" data-size="original">

![Example 2](http://i.imgur.com/u4q7Ipw.png)\
&#xNAN;_&#x53;cripting not necessary ;)_

<img src="http://i.imgur.com/PfATR0P.jpg" alt="Example 3" data-size="original"> <img src="http://i.imgur.com/o8A6xlZ.png" alt="Example 4" data-size="original">

The map Reliquary is another good example. On it darkprince909 created a mini mountain scape around the camera so when players see a reflection, they see the "mountains" around them and not the outside boundaries of the map.

</details>

**Contributors**\
MythicFritz\
Captain Punch

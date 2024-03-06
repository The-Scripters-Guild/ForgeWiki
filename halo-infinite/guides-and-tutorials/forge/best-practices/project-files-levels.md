---
description: Best practices for handling your level files.
---

# Project Files - Levels

While it may not always be reasonable to adhere to all of these, the more that you do, the safer your project is from file corruption issues.

### Axioms

* Have a file with everything you need on it to test the technical aspects of the project, including minimum spawn requirements, this is your template file.
* Always build scripts on a copy of the test world, never use the original, this is your build file, this is where you write the code and do technical tests.
* Have a separate geometry build file for the actual level(s).
* Never put scripts on your geometry build file(s) -- if you do scripted environment elements, I would just add a layer where you have them added that also isn't the geo build file so you always keep a script free geo file.
* Save a copy of your geometry file for testing in actual gameplay and put scripts on that by pasting in prefabs, this is your beta file.
* After you've got a beta worthy of being a release, make a new fresh copy of the geometry file(s) and install scripts (test to confirm it works and release it).

This ensures you can't end up with a corrupt file from scripts on your geo and it's easier to deal with ghost scripts if you don't have to jump back a bunch of versions while you're testing. You just copy the scripts to a prefab and paste it on a copy of the template file. Once you know the script works at all on the most resource intensive target level, or at least on something as budget heavy as Argyle, I'd say you are safe to hand it off to the public to install on their own stuff.

You can roll back to get out of holes, but it isn't as fast as just copying to a clean build file and some holes aren't gonna get filled no matter what if the file corrupts or you have an ownership break, etc.\
\
\# Contributors\
Captain Punch

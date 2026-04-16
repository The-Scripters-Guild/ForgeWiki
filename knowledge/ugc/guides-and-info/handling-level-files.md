---
description: Best practices for handling your level files.
---

# Project Files - Levels

While it may not always be reasonable to adhere to all of these, the more that you do, the safer your project is from file corruption issues.

### Axioms

* Have a file with everything you need on it to test the technical aspects of the project, including minimum spawn requirements, this is your build file.
  * This is also what would become a template for building more levels for the same mode, etc, when you are complete.
* Have a separate geometry build file for the actual level(s) you are going to install the project on.
* Never put scripts on your geometry build file(s).
  * If you intend to add scripted environment elements, I would do that on a copy of the geo file so you always have a geo file that has never had scripts placed in any version.&#x20;
* Save a copy of your geometry file for testing in actual gameplay and put scripts on that by pasting in prefabs, this is your test file.
  * When you can, avoid making changes directly on the test file unless they would be easy to mirror back to the build and geo files.
  * Mirror any updates made on the test file on the build and geo files.

This ensures you can't end up with a corrupt file from scripts on your geo that you can't recover from and it's easier to deal with ghost scripts if you don't have to jump back a bunch of versions while you're testing. You just copy the scripts to a prefab and paste it on a copy of the template file. Once you know the script works at all on the most resource intensive target level, or at least on something as budget heavy as Argyle, I'd say you are safe to hand it off to the public to install on their own stuff.

You can roll back to get out of holes, but it isn't as fast as just copying to a clean build file and some holes aren't gonna get filled no matter what if the file corrupts or you have an ownership break, etc.\
\
\# Contributors\
Captain Punch

---
description: How to interact with the GitHub repo so that your pull requests make sense.
---

# Contributing via Pull Requests

## If you don't already understand Git/GitHub

Refer to this section on the Landing Zone page and submit via the Discord or Infodump Form:

{% embed url="https://wiki.thescriptersguild.com/main/#how-do-i-contribute" %}

## Repo Link

[https://github.com/The-Scripters-Guild/ForgeWiki](https://github.com/The-Scripters-Guild/ForgeWiki)

## Adding Content to the Wiki via Git

* Clone the repo to your local machine
* Create the file in markdown formatting
* Add the description boilerplate to the beginning of the document
* For standalone pages: -- Name the file with kebab-case and the .md extension
* For pages that will have sub-pages: -- Create a folder with the name of the page in kebab-case -- Put the file in that folder, name it README.md
* Add an entry for the new page in the SUMMARY.md in the root directory of the repo
* Submit a pull request with your changes, making sure to note which pages are being changed and why

Look at other pages' raw Markdown as examples for how to set up your document.

### Description Boilerplate

```
---
description: Description text.
---

# Page Title
```

### Adding Entry to SUMMARY.md

[https://github.com/The-Scripters-Guild/ForgeWiki/blob/main/SUMMARY.md](../../SUMMARY.md)

The SUMMARY.md file defines the structure of the wiki and the name of each page as displayed on the wiki.

Find the relevant location in the heirarchy and add an entry with the following syntax:

```
* [Page Name](folder-name/file-name.md)
```

Make sure to indent properly so that everything works as intended.

### Commit Guidelines

* Page names should be Title Case, this is achieved via the \[Page Name] in SUMMARY.md, rather than in the file for the page or its filename.
* Don't create blank pages, rather create an Issue on the repo describing the page and the addition you're planning to make.
  * If you're trying to workshop content, do so on the Discord in the [Wiki Discussion](https://discord.com/channels/220766496635224065/1032391999740969011) forum.
* Images should be added to the assets folder of the repo and linked from there.
  * Image formats should be PNG, GIF, or JPG/JPEG whenever possible.
  * Images should be named using kebab-case and be named semantically.
* External media links should be avoided whenever possible.

**Contributors**\
Captain Punch

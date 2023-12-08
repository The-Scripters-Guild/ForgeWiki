---
description: How to interact with the GitHub repo so that your pull requests make sense.
---

# Contributing via Pull Requests

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

[https://github.com/The-Scripters-Guild/ForgeWiki/blob/main/SUMMARY.md](../SUMMARY.md)

The SUMMARY.md file defines the structure of the wiki and the name of each page as displayed on the wiki.

Find the relevant location in the heirarchy and add an entry with the following syntax:

```
* [Page Name](folder-name/file-name.md)
```

Make sure to indent properly so that everything works as intended.

**Contributors**\
Captain Punch

---
title: "Contribute"
date: 2020-11-12T13:26:54+01:00
lastmod: 2020-11-12T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "wikihelp"
weight: 610
toc: true
---

### Rules for contributing

Before starting your contributions, ask yourself the following questions:

1. Is there already an existing page for the topic you have in mind? If so, make sure you review this page and consider contributing to it before creating a new page.
2. If you need to create a new page, is there an existing section in which this new page could already fit? if so, consider adding it to that section before creating a new section.
3. You think you need to create a new section? Submit an issue on GitHub beforehand to open the discussion on that topic.
4. **Be careful to contribute on a separate branch than main. Open a PR for review to merge your contributions into main.**

### Contributing to an existing page

To contribute to an existing page you have two options:

1. *Recommended:* Edit the file directly on Github. On the wiki, you can navigate to the page you wish to edit, scroll to the bottom and click on "edit this file on GitHub". This will bring you the location of the file on GitHub and allow you to edit the file directly. If you have a lot of edits to contribute, we recommend your work out your content outside of the GitHub editor (for example you can use a markdown editor like [StackEdit](http://stackedit.io/)).
2. Fork the repository, edit in your fork and submit a pull request to the main repo. To learn more about forks, see the [GitHub help on that topic](https://docs.github.com/en/get-started/quickstart/fork-a-repo).

### Creating a subsection (new page)

Creating a new page requires creating a new file. The easiest way to do so is to go on GitHub, navigate to the folder [`content/en/docs`](https://github.com/pedersen-fisheries-lab/pedersen-lab-wiki/tree/main/content/en/docs), and select the folder that corresponds to the section you want to add a page into (for example, `resources`). You can then click the button "add file => create new file".

Each new page requires a special header (see below).

```markdown
---
title: "New Page Title" <!-- The title of the page -->
draft: false <!-- Whether this is a draft page, leave as false -->
images: [] <!-- Leave blank -->
menu: 
  docs:
    parent: "resources" <!-- Must the name of the folder (section) the page is in -->
weight: 100 <!-- The weight in the sidebar (controls placement) -->
toc: true <!-- Whether to show the table of contents-->
---
```

### Creating a section (new folder and new page)

There are three steps for creating a new section:

1. Create a folder named for the new section within `content/en/docs/`. The name of that folder will be used in what follows as `folder-name`.
2. Edit the [menu file](https://github.com/pedersen-fisheries-lab/pedersen-lab-wiki/blob/main/config/_default/menus/menus.en.toml) by adding a `[[docs]]` entry of the type:
```markdown
[[docs]]
  name = "Resources" <!-- The name of the section -->
  weight = <!-- The weight in the sidebar (controls placement) -->
  identifier = "folder-name" <!-- The name of the folder you created -->
  url = "/docs/folder-name/" <!-- The path to the folder within content/en/ -->
```
3. Create an index file. This file must be named `_index.md` and be placed within the folder your created (`folder-name`). It must contain the following header but must remain empty of other content:
```markdown
---
title : "Resources" <!-- The name of the section -->
description: "Lab resources" <!-- The description of the section -->
draft: false <!-- Whether this is a draft section, leave as false -->
images: [] <!-- Leave blank -->
weight: 100 <!-- The weight in the sidebar (controls placement) -->
---
```

Once you have created a section, you can refer to the previous paragrapphs to create the first new page of that section.

### Things to look out for

- If you create a new section or page, you might have to play with the weigth values in order to get the placement you desire.

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
3. You think you need to create a new section? Submit an issue on GitHub before doing to open the discussion on that topic.

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

### Things to look out for

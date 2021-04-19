---
uid: files_and_folders
locale: en
title: Organization of repositories
description: 
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias
---

# Organization of repositories

Git is an open-source version control system. The files are stored in repositories. GitHub is a web-based hosting service for Git repositories.

## File names and file extensions

* Use a descriptive name based on the top-level heading in the file.
* Use single hyphens as word separators. Don't use underscores or camel-case.
* Use lower-case letters, numbers, and dashes only.
* Omit articles and the word *and*.

**Naming conventions:**

* \<feature/context>-overview.md
* \<feature/context>-get-started.md
* \<feature/context>-\<crud>-\<item>.md
* \<feature/context>-settings.md
* \<feature/context>-config.md
* \<feature/context>-nav.md or index.md (for landing pages)

If there are multiple features or contexts in a single folder, you need to specify that in the file names. Otherwise, the parent folder should make that clear.

**slugs:**

* auth
* config
* admin
* security

## Folder organization

We use sub-folders to group similar content, images, and reusable snippets. The organization on GitHub only loosely resembles the structure on `docs.superoffice.com`.

At the root of the repo, there is a folder named *docs*. In it, you can find general pages that relate to the overall website and a set of sub-folders that match the features/APIs or common scenarios.

## Media subfolder

All major folders have a */media* subfolder for the corresponding media files.

## Includes subfolder

All major folders have a */includes* subfolder for reusable content in that section. See [Markdown reference][1] for how to use includes.

## Markdown file template

We use the [Blueprint extension][2] for Visual Studio Code. Available templates are located in the *blueprint-templates* folder at the root of the repo.

<!-- Referenced links-->
[1]: markdown-guide/index.md
[2]: markdown-guide/using-blueprint-templates.md

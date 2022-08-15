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

* \<feature/context>-index.md (or index.yml for landing pages)
* \<feature/context>-overview.md (used when there is already an index file)
* \<feature/context>-getting-started.md
* \<feature/context>-\<crud>-\<item>.md
  * \<feature/context>-install.md
  * \<feature/context>-upgrade.md
  * \<feature/context>-config.md
  * \<feature/context>-debug.md
* \<feature/context>-faq.md
* \<feature/context>-options.md
* \<feature/context>-requirements.md
* \<feature/context>-scenarios.md
* \<feature/context>-security.md
* \<feature/context>-settings.md
* \<feature/context>-troubleshooting.md

If there are multiple features or contexts in a single folder, you need to specify that in the file names. Otherwise, the parent folder should make that clear.

### Example

<!-- markdownlint-disable MD044 -->
A file named *create-company* has UID **crmscript-create-company** and is located in the *superoffice-docs/docs/company/howto/crmscript* folder.

Here, the filename follows the \<crud>-\<item>.md pattern and the parent folders *company/howto/crmscript* provide the context.

We need to add 'crmscript' to the UID to make it unique. However, there is no need to repeat the word 'company' and that it is a how-to is implied by the verb.
<!-- markdownlint-restore -->

## Folder organization

We use sub-folders to group similar content, images, and reusable snippets. The organization on GitHub only loosely resembles the structure on `docs.superoffice.com`.

At the root of the repo, there is a folder named *docs*. In it, you can find general pages that relate to the overall website and a set of sub-folders that match the features/APIs or common scenarios.

## Media subfolder

All major folders have a */media* subfolder for the corresponding media files.

## Includes subfolder

All major folders have an */includes* subfolder for reusable content in that section. See [Markdown reference][1] for how to use includes.

## Markdown file template

We use the [Blueprint extension][2] for Visual Studio Code. Available templates are located in the *blueprint-templates* folder at the root of the repo.

<!-- Referenced links-->
[1]: markdown-guide/index.md
[2]: markdown-guide/using-blueprint-templates.md

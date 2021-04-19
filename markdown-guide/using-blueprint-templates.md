---
uid: using_blueprint_templates
locale: en
title: How to use Blueprint templates in Visual Studio Code
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias
---

# Using Blueprint templates in Visual Studio Code

## Pre-requisites

* A local clone of the [SuperOfficeDocs repo][1]
* Visual Studio Code

## Getting started

* Install the VS Code [Blueprint extension][2] by teamchilla.

## Create a new Markdown file with metadata header

This will create a single file with a standard metadata header and insert the name as the title.

1. Right-click the folder where you want to add the file.
2. Select **New File from Template**.
3. Select **metadata** from the list and enter a name without a file extension.
4. Edit and save the file as normal.

## Create a new sub-folder in DocFX content

This will create the folder and add file *index.md* to it.

1. Right-click the folder where you want to add the file.
2. Select **New File from Template**.
3. Select **docfx-subfolder** from the list and enter a folder name.
4. Optionally add additional Markdown files to the new folder.

<!-- Referenced links-->
[1]: https://github.com/SuperOfficeDocs
[2]: https://marketplace.visualstudio.com/items?itemName=teamchilla.blueprint
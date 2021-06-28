---
uid: landing_pages
locale: en
title: Landing pages
description: How to work with category files (index.yml) on SuperOfficeDocs
so.topic: concept
so.date: 06.28.2021
so.author: Bergfrid Dias
---

# Landing pages

We create landing pages in several locations. The most obvious one is `docs.superoffice.com`. The contents and layout of this page are set in our build templates in a private repository. If you have suggestions or want to request changes **main page**, you can [create a site feedback issue][1].

## Level 2: category pages

A **category page** is a landing page for a specific area, for example, SuperOffice APIs or onsite installation, to simplify navigation to the various topics within that area. The contents and layout of these pages are configured in files named *index.yml* and adhere to a custom schema. Unlike the main page, these YAML files are located in the corresponding folders in the content repositories and can thus be forked and edited.

The first line says `### YamlMime:Category`, followed by title, summary, and metadata.

Then you'll find various blocks of links:

* **highlightedContent** - holds several simple cards, each card points to a single piece of content.
* **productDirectory** (optional) - can have a section title and summary, it contains several cards, each one points to a product page.
* **conceptualContent** - can have a section title and section summary as well as several cards. The cards must have a title and contain at least one link.
* **tools** (optional) - may have a section title and a section summary, the section must consist of several cards. Each card is meant to point to a Language, Framework, CLI, Tool, or Extension.
* **additionalContent** - is the most flexible section. It allows for a section title, section summary, several cards, and a footer section

The URLs are relative to the YAML file and can be either external, point to a Markdown file of a specific page, or to another *index.yml*.

### Examples

```yml
highlightedContent:
  items:
    # Card
    - title: "System requirements"
      itemType: reference
      url: requirements/index.md
    # Card
    - title: "Customer Service"
      itemType: overview
      url: ../service/index.yml
    # Card
    - title: "Installation guide (Web)"
      itemType: overview
      url: install/index.yml
    # Card
    - title: "Release notes"
      itemType: whats-new
      url: ../../release-notes/index.md
```

```yml
conceptualContent:
  title: "Get SuperOffice up and running"
  summary: "Regardless of whether this is your first installation or an upgrade, security is essential."
  items:
    # Card
      - title: Migrate to CRM online
        summary: Take SuperOffice to the cloud
        links:
          - url: ../online/migrate/index.md
            itemType: how-to-guide
            text: "Migration guide"
          - url: ../service/mailboxes/migrate.md
            itemType: concept
            text: "Migrating Service mailboxes"
          - url: ../online/system-requirements.md
            itemType: reference
            text: System requirements for SuperOffice CRM Online
```

> [!NOTE]
> Yaml is **very picky** when it comes to whitespace and indentation.

## Level 3: sub-category pages

A **sub-category page** is similar to a category page but its focus is narrower. For example, while the SuperOffice API landing page is a category, authentication is a sub-category.

The first line will say `### YamlMime:SubCategory`, followed by title, summary, and metadata.

There's just one block: **landingContent**.

### Examples

```yml
title: CRM Onsite
summary: Welcome to the area where you can find relevant links to all things related to installation, upgrade, and migration.
metadata:
  title: Set up SuperOffice successfully
  description: SuperOffice Onsite installation, upgrade, and migration.
  so.product: onsite
  so.topic: hub-page
  # ...
landingContent:
# Card
- title: Onsite authentication
  linkLists:
    - linkListType: learn
      links:
      - text: Overview
        url: overview.md
    - linkListType: get-started
      links:
        - text: NetServer Core
          url: onsite/sosession/index.md
        - text: NetServer Custom Proxies
          url: onsite/custom-proxies/index.md
        - text: REST WebApi
          url: onsite/webapi/index.md
        - text: COM API
          url: onsite/com/index.md
```

```yml
# Card
- title: Feedback
  linkLists:
    - linkListType: how-to-guide
      links:
      - text: Create an issue
        url: https://github.com/SuperOfficeDocs/superoffice-docs/issues
# Card
- title: Editing and authoring
  linkLists:
    - linkListType: how-to-guide
      links:
      - text: How to edit an article in browser
        url: how-to-edit-an-article-in-browser.md
      - text: How to edit an article locally
        url: how-to-edit-an-article.md
    - linkListType: reference
      links:
      - text: Style guide
        url: style-guide/index.md
      - text: Guidelines for formatting
        url: style-guide/formatting.md
      - text: Our branch strategy
        url: branch-strategy.md
      - text: Git cheat-sheet
        url: git-cheat-sheet.md
```

## Common tasks

> [!TIP]
> You may click on the **Edit** button when viewing the page to suggest an improvement on the existing article content.

### Fix typo or change title, description, or link text

1. Locate the correct *index.yml*.
2. Edit the value of the `title`, `summary`, or `text` field.

### Fix broken link

1. Locate the correct *index.yml*.
2. Edit the value of the `url` field.

> [!TIP]
> To test that the path and file name are correct, Ctrl-click the link in VS Code. If the target file opens, you're good to go.

### Add a link to an existing card

1. Locate the correct *index.yml*.
2. Decide which entry you'll add it after.
3. Add a text-url pair at the appropriate level. You'll need minimum 2 lines:

    ```yml
    - text: REST WebApi
      url: onsite/webapi/index.md
    ```

    Some blocks require you to specify `itemType`, others `linkListType`. **Follow the established pattern.**

### Add a new card to the landing page

1. Locate the correct *index.yml*.
2. Decide which block you want to add it to, and where in the sequence.
3. Copy an existing card in that block and modify it. The simplest card is in the highlighted content:

    ```yml
      - title: "System requirements"
        itemType: reference
        url: requirements/index.md
    ```

<!-- Referenced links -->
[1]: https://github.com/SuperOfficeDocs/feedback/issues/new?assignees=&labels=&template=improve-the-site.md&title=

<!-- Referenced images -->

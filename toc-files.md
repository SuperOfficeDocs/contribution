---
uid: toc_on_docs
locale: en
title: Table of contents
description: How to work with table-of-content (TOC) files on SuperOfficeDocs
so.topic: concept
so.date: 06.24.2021
so.author: Bergfrid Dias
---

# Table-of-content (TOC) files

We use  [YAML format TOC files][1], which are named *toc.yml*.

Inside, you will find an array of TOC Item Objects:

```yml
- name: What is NetServer
  href: netserver/what-is-netserver.md
- name: Authentication
  href: authentication/index.yml
  items:
  - name: Overview
    href: authentication/overview.md
  - name: Terminology
    href: authentication/terminology.md
```

The `name` is what's shown in the table of content on the website.
The `href` is the path relative to the current *toc.yml*.

> [!NOTE]
> Yaml is **very picky** when it comes to whitespace and indentation.

## Nesting (linked TOCs)

Each repository has a top-level *toc.yml* in the *docs* folder. It will include links to local markdown files, a link to another TOC file, or a combination. The linked TOC files are placeholders - DocFx will extract the contents of the referenced file and insert it into the current *toc.yml* recursively.

Let's see how it is set up in the superoffice-docs repository.

**superoffice-docs/docs/toc.yml:**

```markdown
items:
- name: Docs
  href: 00-custom/toc.yml
  expanded: true
```

**superoffice-docs/docs/00-custom/toc.yml:**

```markdown
### YamlMime:ManagedReference
items:
- name: Admin
  href: ../admin/toc.yml
  topicHref: ../admin/overview.md
```

**superoffice-docs/docs/admin/toc.yml:**

```markdown
items:
- name: Admin
  href: overview.md
  expanded: true
  items:
  - name: License
    href: ../license/index.md
    expanded: true
    items:
    - name: User plans
      href: ../license/user-plans.md
    - name: Expander services
      href: ../license/expander-services/index.md
    # ...
```

## Common tasks

### Fix typo or change text shown in TOC

1. Locate the correct *toc.yml*.
2. Edit the **name**.

### Fix broken link in TOC

1. Locate the correct *toc.yml*.
2. Edit the **href**.

[!include[ALT](includes/tip-check-link.md)]

### Add a new file to the TOC

1. Locate the correct *toc.yml*.
2. Decide which entry you'll add it after.
3. Add a TOC item at the appropriate level. You'll need minimum 2 lines: `name` and `href`.

    ```markdown
    - name: Topic 1
      href: topic-1.md
    ```

    * If this is the **first child**, you need to also add `items:` and indent your new entry.

    ```markdown
    - name: Parent topic
      href: topic-1.md
      items:
      - name: New topic
        href: topic-2.md
    ```

<!-- Referenced links -->
[1]: https://dotnet.github.io/docfx/tutorial/intro_toc.html

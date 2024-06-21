---
uid: markdown-guide-markdownlint
language: en
title: Linting Markdown for docs.superoffice.com
description: Introduction to markdownlint and how we use it for SuperOfficeDocs.
topic: howto
date: 08.15.2022
author: Bergfrid Dias
---

# markdownlint

## What is markdownlint

**markdownlint** is an extension to VS Code that encourages standards and consistency for Markdown. It is available directly from the [VisualStudio marketplace][3] or via the **Docs Authoring Pack** extension.

## Rules

The rules have a number and an alias. For example MD029/ol-prefix.

* [List of all rules][4]
* [Description of each rule][5]

### Our custom rule-set

We have tailored the linting rules to align with our [Markdown style guide][2]. The custom configuration is located in *.markdownlint.yaml*.

> [!NOTE]
> Don't alter the rules without discussing it with the DX team.

## Use

When you edit a Markdown (.md) file in VS Code with this extension installed, you get visual warnings in the editor for lines that violate a rule.

**Example:**

![Warning from markdownlint in VS Code -screenshot][img1]

Here, the wavy underline indicates a problem with list numbering.

You can hover to find out more about the problem:

![Hovering warning from markdownlint in VS Code-screenshot][img2]

Here we see that it is rule MD029 that is violated and that the list prefix on line 27 should be 3 and not 4.

You now have a few options for how to proceed:

* Edit the Markdown manually.
* Select **Quick Fix** and then select to fix all violations in the file.

![Quick fix warning from markdownlint in VS Code-screebshot][img3]

> [!TIP]
> Click the first link in the **Quick Fix** dialog to read more about the rule.

### Special cases

In some cases, we deliberately deviate from the rules by manually turning a rule off for a single line, a group of lines, or an entire file.

You will see this as HTML comments inside the Markdown files like this:

```html
<!-- markdownlint-disable-next-line MD001 MD005 -->
```

Leave these comments as is. We need them to establish a valid baseline for the repo.

**Noteworthy exceptions:**

* Because all include files are fragments, the first line must be `<!-- markdownlint-disable-file MD041`

* Because tabbed content uses a specific syntax, rule MD051 must be disabled like this:

    ```markdown
    <!-- markdownlint-disable MD051 -->
    ### [NetServer Core](#tab/core)

    Contents of core tab

    ### [NetServer Web Services](#tab/ws)

    Contents of ws tab

    ***
    <!-- markdownlint-restore -->
    ```

* Excessively long headings that can't be shortened must be prefixed with `<!-- markdownlint-disable-next-line MD013 -->`

* When list numbering is part of an include, you might need to handle numbering before/after the included file yourself. `<!-- markdownlint-disable-file MD029 -->`

There are a few more, mostly pertaining to API documentation and code examples. If in doubt, search for the rule ID (such as MD029) in the repo source and you'll find examples of how to handle it. Ask if you have questions.

## Command-line linting

You can optionally install [markdownlint-cli][6], a command-line interface that allows you to do bulk linting. This is useful for bulk editing but it can also be added to a build pipeline as automatic testing.

**Install:**

```sh
npm install -g markdownlint-cli
```

**Use:**

```sh
markdownlint -f -i *.cs *.xml --disable MD013 MD041 -c  .markdownlint.yaml PATH
```

* -f will automatically fix problems that have a defined fix, for example, whitespace
* -i ignores whatever follows, in this case, all cs and XML files. To omit API from the run, add api/ to the path.
* --disable turns off the listed rules
* -c specifies the markdownlint config file. In this case, we use the one inside the `superoffice-docs` repo

See [GitHub issue 373][7] regarding why we exclude rules MD013 and MD041.

<!-- Referenced links -->
[2]: index.md
[3]: https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint
[4]: https://github.com/DavidAnson/markdownlint#rules--aliases
[5]: https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md
[6]: https://github.com/igorshubovych/markdownlint-cli
[7]: https://github.com/SuperOfficeDocs/superoffice-docs/issues/373

<!-- Referenced images -->
[img1]: media/mdlint-list-warning.png
[img2]: media/mdlint-list-hover.png
[img3]: media/mdlint-list-quickfix.png

---
uid: code-in-docs
locale: en
title: How to include code in docs
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias
---

# How to include code in docs

There are multiple ways to include code in a page published on `docs.superoffice.com`:

* Individual words within a line
* Code blocks in the current Markdown file

## Inline code

Wrap the code text in single backticks (\`).

For example, \`getDate()\`

> [!NOTE]
> Don't style links as code. It can obscure the fact that the text is a link.

### When to use it

Use `inline code` when referring to:

* Named parameters and variables in a nearby code block in your text
* Properties
* Methods and classes
* Language keywords
* Database table and column names
* SQL commands
* NuGet package names

It's not always obvious what qualifies as code. If in doubt, see [text formatting guidelines][1].

### Placeholders

To indicate that the user must replace something in the code with their own values, use placeholder text marked off by angle brackets.

## Fenced code blocks

* Use code fencing with triple backticks (\`\`\`) before and after.
* Place the programming language after the opening backticks for syntax highlighting.
* Don't use indentation only to indicate a code block.

**Markdown:**

```markdown
    ```crmscript
      for(Integer i = 1; i < 10; i++) {
        printLine(i.toString());
      }
    ```
```

**Rendered:**

```crmscript
for(Integer i = 1; i < 10; i++) {
  printLine(i.toString());
}
```

### Screenshots

Avoid IDE screenshots with code, unless you want to illustrate something specific about the IDE.

Fenced code blocks can be copied and pasted and they're indexed by search engines.

## Tabbed content

You can create tabbed content in markdown.

### Syntax

* Start a tab with a special markdown title (any level).
  * Title content should be a markdown link.
  * Link target is #tab/{tabid} or #tab/{tabid}/{condition}
* Continue by any other content.
* End by a markdown hr.

#### Example

Tab group 1:

```markdown
# [Tab Text 1](#tab/tabid-1)

Tab content-1-1.

# [Tab Text 2](#tab/tabid-2)

Tab content-2-1.

***
```

Read about it, and more advanced options, in the [DocFx specification][2].

<!-- Referenced links -->
[1]: ../stykle-guide/formatting.md
[2]: https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html?tabs=tabid-1%2Ctabid-a#tabbed-content
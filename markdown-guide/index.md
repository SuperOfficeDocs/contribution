---
uid: markdown-guide-to-docfx
locale: en
title: Markdown guide for docs.superoffice.com
description: This Markdown style guide is intended to ensure that the markup of SuperOfficeDocs has a consistent style, and is easy to navigate and maintain.
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias, Tony Yates
---

# Markdown guide

Once you start investigating the new SuperOfficeDocs files, you’ll notice a different style of syntax. This is something called **markdown** and it’s the commonly accepted format and syntax for tasks just like this. Markdown is simple and easy to use. You can find links to help you get started with Markdown at the bottom of this page.

For example, you’ll do things like `**A BOLDED WORD**` instead of typing `<strong>A BOLDED WORD</strong>` just to **bold some text**, which saves you multiple keystrokes.

This guide is intended to ensure that the markup of SuperOfficeDocs has a consistent style, and is easy to navigate and maintain.

Adopting these guidelines also limits variation, thereby eliminating confusion, guesswork, and debates.

Use the [style guide][1] as a companion guide.

One benefit to markdown is that the style and formatting of the content can be more simple and uniform across pages. The following examples of formatting and elements can help get you started with the basics. You can find the details in the subsequent alphabetic sections about layout, formatting, and structure.

1. Ordered list items
2. **bold list item**
3. *italic list item*

* Unordered list items
* [link example](https://community.superoffice.com/)

The examples above would look like this in Markdown:

```markdown
1. Ordered list items
2. **bold list item**
3. *italic list item*

* Unordered list items
* [link example](https://community.superoffice.com/)
```

## Angle brackets

Angle brackets are used for HTML and XML tags and to denote placeholders in code.

The opening angle bracket must be escaped in text. For example, type \\\<cust ID> to produce \<cust ID>.
You don't have to escape angle brackets in text formatted as inline code or in code blocks.

## Apostrophes and quotation marks

Use basic straight apostrophes and quotation marks. If copying into Markdown, use Ctrl+Shift+V.

## Blockquotes

Start the line with a \>

## Bold and italic

* Use a pair of **double stars for bold** emphasis.
* Don't use underscores to mark emphasis.
* Don't use uppercase for emphasis.
* Don't use quotes for emphasis.
* Use a pair of **single stars for italic** emphasis.

## Call-outs (alerts, admonitions)

One thing you may see in the documentation is the use of **call-outs**. These show up in the form of light-colored boxes with words such as **NOTE**, **IMPORTANT**, or **WARNING** in them.

They look like this:

> [!NOTE]
> This is important.

The call-out above would look like this in markdown:

```markdown
> [!NOTE]
> This is important.
```

If you want to include a call-out in your docs content, the following types are currently supported:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

And here is something to note about call-outs!

> [!NOTE]
> You cannot include a call-out inside a table.

## Columns

TBD

## Headings

* Start the line with 1 or more \#. The number of hashes determines the heading level. For example, \#\# means H2.
* Don't nest headings lower than H4.
* There must be a space between the last # and heading text.

## HTML

Even though Markdown supports inline HTML, we (generally) don't use it on `docs.superoffice.com`. It is likely to cause build errors or warnings.

**Exceptions:**

* Use `<br>` to break a line in table cells and alerts.

## Images

You can use either *.jpg* or *.png* images. Place images in the appropriate *media* folder.

**Format:**

\!\[Alt text\]\(path\)

**Example:**

```markdown
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
```

### Reference-style images

We use reference-style links for image paths to improve the readability of the Markdown and simplify maintenance.

Example: the above image of Yaktocat written as reference-style

Inline:

```markdown
![Image of Yaktocat][img1]
```

Reference section at the end of the file:

```markdown
<!-- Referenced images-->
[img1]: https://octodex.github.com/images/yaktocat.png
```

> [!NOTE]
> We prefix all labels referring to images with **img**.

### Icons

Reusable icons are placed in the repo's top-level *media/icons/* folder. Don't set alt text for icons.

## Included Markdown files

When the same content should be repeated on multiple pages, you can use includes.

Reusable content snippets are placed in their own Markdown files in the */includes* subfolder and referenced from where it should be inserted. The reference is replaced at build time by the extensions.

> [!NOTE]
> Includes are not rendered in the GitHub preview.

### Includes syntax

* \<title> is the name of the file
* \<filepath> is the relative path to the file
* INCLUDE must be capitalized
* there must be a space before the \<title>

**Block include (on a separate line):**

`[!INCLUDE [<title>](<filepath>)]`

**Inline include (within a line):**

Text before `[!INCLUDE [<title>](<filepath>)]` and after.

Here are requirements and considerations for include files:

### Guidelines

* Write all the text in an include file as complete sentences or phrases. Avoid creating a dependency on preceding text or following text on the page that references the include.

* Don't nest includes.

* Place images used by includes in a */includes/media* subfolder.

* Don't add metadata at the top of include files.

* Relative links within an include file are relative to that file, not where it is included.

* You can use reference-style links within the file, but not to set the path for the \[!INCLUDE\]

## Links

For information about the syntax for links, see [How to use links in docs][5].

## Lists

* Use numbers for ordered lists.
* Use stars for bulleted lists. Don't use dashes.

To include an image, a call-out, a new paragraph, or a child list, indent that content **4** spaces relative to the list item it belongs to.

## Metadata (front-matter)

We [use Yaml key-value front-matter syntax to embed metadata][6] in  Markdown files.

## Source code

For information about the syntax for source code, see [How to include code in docs][7].

## Special characters that need to be escaped

<dl>
<dt>\</dt><dd>backslash</dd>
<dt>`</dt><dd>backtick</dd>
<dt>*</dt><dd>asterisk (star)</dd>
<dt>_</dt><dd>underscore</dd>
<dt>{}</dt><dd>curly braces</dd>
<dt>[]</dt><dd>square brackjets</dd>
<dt>()</dt><dd>parentheses</dd>
<dt>#</dt><dd>hash mark</dd>
<dt>+</dt><dd>plus sign</dd>
<dt>-</dt><dd>minus sign</dd>
<dt>.</dt>
<dd>dot (period)</dd>
<dt>!</dt>
<dd>exclamation mark</dd>
</dl>

## Tables

* Separate columns with a pipe character (|). Use surrounding pipes too.
* Separate the header row from the body with a row of dashes (and pipes to match the columns).
* Put 1 space on either side of a pipe (except the left-most and right-most).
* You can align the columns by using colons.

| default (left) | centered | right |
|--------|:------:|-------:|
| corn | (winter) squash | beans |

The table above would look like this in markdown:

```markdown
| default (left) | centered | right |
|--------|:------:|-------:|
| corn | (winter) squash | beans |
```

## Whitespace and line breaks

* Put 1 space after a sentence (except if followed by a line break).
* Put 1 empty line before and after all block elements:
  * paragraphs
  * headings
  * lists
  * tables
  * images
* Press **Enter** once to break within a paragraph (\<br>). Press **Enter** twice to start a new paragraph.
* Use horizontal rulers sparingly if at all. Type 3 or more consecutive hyphens to produce an \<hr\>.

## Helpful links

Here are a few resources to help with Markdown to help get you started:

* [Markdown guide][2] with examples and formatting info
* [Dillinger.io][3] is an online Markdown tool that can help convert HTML to Markdown and to work with Markdown
* Here's a helpful [Markdown plugin for Visual Studio Code][4]

<!-- -->
[1]: ../style-guide/index.md
[2]: https://www.markdownguide.org/getting-started/
[3]: https://dillinger.io/
[4]: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one
[5]: metadata.md
[6]: links-in-docs.md
[7]: code-in-docs.md

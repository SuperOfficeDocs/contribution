---
uid: links-in-docs
locale: en
title: How to use links in docs
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias
---

# How to use links in docs

This section describes how to use links from pages hosted at `docs.superoffice.com`.

We differentiate between links to content on the same page, links to neighboring pages, and links to external websites and URLs.

## Format

Type the link text in square brackets directly followed by the URL in parentheses.

Format: \[Link text\]\(url\)

Example:

```markdown
[link to Google!](http://google.com)
```

## Link text

Use either the title of the page you are linking to or a friendly, descriptive label.

> [!NOTE]
> Don't use "click here". It is bad for SEO and blinds the reader.

## Links from one page to another

* Use file links when linking within the repository.
* Use forward-slash (`/`) in paths.

**Link to another page in the same folder:**

`[link text](page.md)`

**Link to a page in the parent folder:**

`[link text](../page.md)`

**Link to a page in a sub-folder:**

`[link text](folder/page.md)`

**Link to a page in a subfolder of the parent folder:**

`[link text](../folder/page.md)`

**Link to an absolute path beginning at the root of the repository:**

`[link text](/folder/page.md)`

## Reference-style links

We use reference-style links to make the source content easier to read and maintain. You move the (long) URLs to the end of the file and reference them by labels in square brackets.

**Before:**

```markdown
[link to Google!](http://google.com)
```

**After:**

Inline text:

```markdown
[link to Google!][1]
```

Link references at the end of the file:

```markdown
<!-- Referenced links -->
[1]: http://google.com/
```

Make sure that you include the space after the colon, before the link. Otherwise, the link will be broken.

## Bookmark links (anchors)

Bookmark links go to a specific heading on the current or another page.

**Link to heading in the *current* file:**

* Use a hash symbol (#) followed by the lowercase words of the heading.
* Remove any punctuation and replace spaces with dashes.

```markdown
[Integer datatype](#integer-datatype)
```

**Link to a heading on another page:**

* Use a relative link plus a hash symbol (#), followed by the lowercase words of the heading.
* Remove any punctuation and replace spaces with dashes.

```markdown
[Integer datatype](../datatypes.md#integer-datatype)
```

**Add anchor:**

You can use either the *id* or *name* attribute on the `<a>` tag. The anchor label must be lowercase and not contain spaces.

```markdown
## <a id="anchor-label" />Heading text
```

or

```markdown
## <a name="anchor-label" />Heading text
```

## xref (cross reference) links

Currently not supported for SuperOfficeDocs.

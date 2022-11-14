---
title: Review process in SuperOfficeDocs
uid: docs-review-process
description: Explanation of how to request a review, to handle feedback and suggested changes, and to review someone else's contributions on SuperOfficeDocs.
author: Bergfrid Dias
so.date: 11.14.2022
keywords: review
so.topic: concept
---

# Reviews on SuperOfficeDocs

## I'm a contributor, translator, or content author

To incorporate your changes, we'll merge your pull request (PR) with the main branch after approving the PR.

1. [Create the PR (request a review)][1].

## I'm a reviewer

As a reviewer, you'll do one or more of the following tasks:

* Comment on the changes proposed in PR.
* Approve the changes.
* Request further changes (blocks merge).

[How to comment or start a review][4]

## What to check

* [Markdown formatting][2] - no linting errors
* [Style guide][3]
* Automatic tests should pass.
* Local DocFX build should pass and not report broken links. Modified and new pages should look OK on localhost.
* Reference to deleted pages should be removed from toc and other content.
* Reference to moved or renamed pages should be updated so no links break.
* Images and other resources used only in a deleted file should also be deleted.

<!-- Referenced links -->
[1]: request-review.md
[2]: ../style-guide/index.md
[3]: ../markdown-guide/index.md
[4]: check-changes.md

<!-- Referenced images -->

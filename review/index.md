---
title: Review process in SuperOfficeDocs
uid: docs-review-process
description: Explanation of how to request a review, to handle feedback and suggested changes, and to review someone else's contributions on SuperOfficeDocs.
author: Bergfrid Dias
date: 11.14.2022
keywords: review
topic: concept
---

# Reviews on SuperOfficeDocs

Reviews can be many things. This article focuses on the required steps to get a proposed change accepted and published to `docs.superoffice.com`.

The main objectives of our mandatory pull request (PR) reviews and automatic tests are to ensure that content is easy to find, easy to understand, and easy to use and that changes don't cause the build pipeline to fail or the site to break.

## I'm a contributor, translator, or content author

To incorporate your proposed changes, we'll merge your pull request (PR) with the main branch after approving the PR.

1. [Create the PR (request a review)][1]. This signals that you consider your work done.

    > [!NOTE]
    > If you want intermittent input from a co-author or a subject matter expert (SME) before you're done, contact them directly or @ mention them in a comment on the GitHub issue.

1. When you receive GitHub notifications on the PR, study the comments and [incorporate the feedback][5].

    It is not uncommon for this step to involve several discussions and fixes.

## I'm a reviewer

As a reviewer, you'll do one or more of the following tasks:

* Comment on the changes proposed in PR.
* Approve the changes.
* Request further changes (blocks merge).

[How to comment or start a review][4]

## What to check

* [Markdown formatting][3] - no linting errors
* [Style guide][2]
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
[5]: incorporate-feedback.md

<!-- Referenced images -->

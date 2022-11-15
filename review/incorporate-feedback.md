---
title: View and incorporate feedback on PR
uid: docs-review-feedback
description: How to view and incorporate feedback on pull review at GitHub.
author: Bergfrid Dias
so.date: 11.14.2022
keywords: review, feedback, PR
so.topic: howto
---

# View and incorporate feedback on PR

## View feedback

1. Go to [the repository][1] and click **Pull requests**.
2. Select a PR from the list.
3. Select the **Conversation** tab.
4. Scroll to a review and click **View changes**.

    ![GitHub PR conversation view changes -screenshot][img1]

For each remark, you can choose to reply with a comment, commit the suggested changes, or edit the file directly.

## Commit suggested changes

1. On the **Files changed** tab, scroll to the first suggestion.

1. Click **Commit suggestion**.

    ![GitHub PR commit changes -screenshot][img2]

1. Enter a short message and click **Commit changes**.

> [!TIP]
> To apply multiple suggestions, optionally click **Add suggestion to batch** in step 2. This will group them into a single commit rather than one commit per accepted change.

## Edit file on GitHub

If you [edited a file on GitHub][2], a branch was created at the same time you created the PR.

![GitHub create patch -screenshot][img4]

To update this file again on that branch:

1. When viewing the PR, select the **Files changed** tab.

1. Click the three dots above the changed file and select **Edit file**.

    ![GitHub edit file in PR -screenshot][img6]

1. The branch name should match the patch you created.

    ![GitHub edit file in patch -screenshot][img7]

1. Revise the file as requested in the PR review.

1. Commit the file, selecting the option to commit directly to the **patch branch**.

    ![GitHub commit to patch -screenshot][img8]

### Alternatively, browse to the file manually

1. When viewing the PR, click the two squares below the PR header to copy the branch name:

    ![GitHub copy patch name -screenshot][img5]

1. Select the **Files changed** tab and note or copy the file path.

     ![GitHub copy path -screenshot][img9]

1. Select the **Code** tab on the main menu.

1. Select your PR branch.

    ![GitHub select branch -screenshot][img10]

1. Navigate the folders till you locate the file.

1. Click the pencil icon to edit and revise as necessary.

1. Commit the file, selecting the option to commit directly to the **patch branch**.

## Check out and edit PR branch locally

Note the issue number of the PR.

* If you already have the branch locally, pull to get the latest updates.
* If you have a clone of the repo, pull on main, then switch to the branch associated with the PR.
* Otherwise: On the **Conversation** tab, click **Code** and select how to check out the PR.

    ![GitHub PR checkout locally -screenshot][img3]

Then revise and commit the changes to the branch. After pushing, the PR on GitHub is updated with the changes.

<!-- Referenced links -->
[1]: https://github.com/SuperOfficeDocs/superoffice-docs
[2]: ../how-to-edit-an-article-in-browser.md

<!-- Referenced images -->
[img1]: media/conversation-view-changes.png
[img2]: media/commit-suggestion.png
[img3]: media/checkout-pr.png
[img4]: media/create-patch.png
[img5]: media/copy-branch-name.png
[img6]: media/edit-file-in-pr.png
[img7]: media/edit-in-patch.png
[img8]: media/commit-to-patch.png
[img9]: media/copy-path.png
[img10]: media/select-branch.png

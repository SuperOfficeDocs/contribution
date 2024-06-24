---
title: Reviewing a PR
uid: review-check-changes
description: How to check proposed changes in a PR
author: Bergfrid Dias
date: 11.14.2022
keywords: review, PR
topic: howto

---

# Reviewing a PR

Anyone with access can comment on a PR. The ability to request changes or submit reviews that approve a PR is limited to admins.

## Open the PR for viewing

1. Go to [the repository][1] and click **Pull requests**.
2. Select a PR from the list.

## Leave a general comment

1. Select the **Conversations** tab.

2. Scroll to the bottom of the page, write your feedback, and click **Comment**.

    ![GitHub PR comment field -screenshot][img1]

## Comment on a specific line

1. Select the **Files changed** tab.
2. Locate the file and specific line you want to comment on.
3. Put you mouse on the line and click the blue plus icon.

    ![GitHub PR line comment -screenshot][img2]

4. Type your comment.
5. Click **Add single comment**.

## Start and submit review

1. Add one or more line comments as described above.

1. Optionally, suggest a specific change that the author can accept and commit directly.

    Click ![icon][img5] and edit the text between the ` ``` `.

    ![GitHub PR suggest change write -screenshot][img4]

    ![GitHub PR suggest change preview -screenshot][img3]

1. When you're done, click **Start a review**. Alternatively, click **Add review comment** if you already started the review.

1. Finished reviewing all the files.

1. Click **Review changes** above the changes.

    ![GitHub PR Review changes button -screenshot][img6]

1. Enter a description of your feedback and select the type.

    ![GitHub PR Submit review -screenshot][img7]

1. Click **Submit review**.

## What happens now?

* Follow the discussion in the **Conversation** tab.
* If you requested changes, follow up on those.
* If you approved and all checks are green, you can merge the PR and delete the branch.

<!-- Referenced links -->
[1]: https://github.com/SuperOfficeDocs/superoffice-docs

<!-- Referenced images -->
[img1]: media/comment.png
[img2]: media/line-comment.png
[img3]: media/preview-suggestion.png
[img4]: media/enter-suggestion.png
[img5]: media/add-suggestion-icon.png
[img6]: media/review-changes.png
[img7]: media/submit-review.png

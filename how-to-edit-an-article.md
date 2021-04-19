---
uid: how-to-edit-an-article
locale: en
title: Edit an article
description: Edit an article
so.topic: howto
so.date: 04.19.2021
so.author: Tony Yates
---

# Edit an article

## Pre-requisites

  1. [Get SuperOfficeDocs running locally][1]: To edit an article, you need to get SuperOfficeDocs running locally on your machine.

  2. **Markdown**: Docs uses markdown syntax to format content. Markdown is simple to pick up on. Familiarize yourself with the [Markdown Guide to DocFx][2] before making updates to content.

Now that you've gotten SuperOfficeDocs running locally (congrats BTW!) we will talk through the steps for making an edit, previewing the edit, pushing it to your forked repo, then creating a pull request.

## How to edit and preview content

1. Fork the [SuperOfficeDocs repo][3] into your own repo.

    ![Fork SuperOfficeDocs screenshot][img1]

2. Set your remote repositories. We will use the terms **upstream** and **origin**. When you originally cloned the repo (in the pre-requisites), the `origin` was added for you implicitly.

    Type `git remote add upstream https://github.com/SuperOfficeDocs/superoffice-docs` to add the main SuperOffice Docs repo as your upstream repo.

    > [!NOTE]
    > Remotes can be named anything you like. Find out your remotes by typing `git remote -v`.

    Type `git remote -v` to list your remotes. If you are new to Git, you should have 2 remotes:

    * `origin` is your forked repo
    * `upstream` is the main SuperOfficeDocs repo

3. Create an [Issue][4] on GitHub that corresponds with the edit you're working on by clicking the **New Issue** button in the browser. Be sure to include relevant information providing context to the issue in the description or comment section. This helps reviewers understand what you're working on.

    Make note of the **issue number** that GitHub generates.

    ![GitHub issue screenshot][img2]

4. Create a new branch for your work. Typically branch names align with the issue number for ease of tracking.

   **Example branch name**: `issue-107`

   **Example Git command to create new branch**: `git checkout -b issue-107`

5. Make your edits.

6. Preview your work locally by invoking the `docfx --serve` in your terminal (in VS Code, Powershell, or similar). This will run SuperOfficeDocs locally on your machine at a URL similar to this `localhost:8080`. Click the link or copy and paste it into your browser.

When you are happy with your changes, you can move on to pushing it to your forked repo and creating a pull request.

## How to commit and share

1. Use `git status` to review the files you are working on and ensure the proper files are being tracked.

2. Use `git add [INSERT FILE NAME]` to stage a single file or `git add .` to stage **all** modified files to be committed.

3. Use `git commit -m [INSERT YOUR COMMIT MESSAGE HERE]` to commit your files. The `-m` stands for *message*. Replace the *INSERT YOUR COMMIT MESSAGE HERE* text with brief and relevant text summarizing your commit.

4. Use `git push origin [INSERT A NEW BRANCH NAME HERE]` to push your updated files to your repo. Replace the *INSERT A NEW BRANCH NAME HERE* with the name of your new branch

5. Go to your forked GitHub repo on GitHub.com. GitHub should detect the updated code and prompt you to make a pull request.

6. Create a pull request by clicking the **Compare and create pull request** button. In the description or comments section be sure to include the text "Resolves ```#[INSERT ISSUE NUMBER HERE]``` where your previously created issue number is associated with this pull request.

> [!TIP]
> Want more info on Git? Check out the free, online [GitBook][5].

<!-- Referenced links-->
[1]: get-superoffice-docs-running-locally.md
[2]: markdown-guide/index.md
[3]: https://github.com/SuperofficeDocs/superoffice-docs
[4]: https://github.com/SuperOfficeDocs/superoffice-docs/issues
[5]: https://git-scm.com/book/en/v2

<!-- Referenced images-->
[img1]: media/fork-repo-on-github.png
[img2]: media/create-issue-on-github.png

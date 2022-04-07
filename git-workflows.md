---
uid: git-workflows
title: Common Git workflows
description: A beginner's guide to Git - step-by-step instructions for daily tasks in different tools
locale: en
so.topic: howto
so.date: 04.07.2022
so.author: Bergfrid Dias
---

# A beginner's guide to Git

This tutorial walks you through the most common Git tasks on your **local computer**. We show the Git Bash command line and Visual Studio Code (VS Code) side-by-side.

**Other options:**

* [Work exclusively in the browser on github.com][1].

## Day 0

* Install software
* Fork/clone the repository

> [!TIP]
> If you don't have Git installed, you will need to install Git first. You can find instructions on installing Git in the free [Pro Git book][3], written by Scott Chacon and Ben Straub.

### Clone repo

**To clone** means to create a copy of the repo (files and folders) on your local machine so that you can work with them.

To find the URL:

1. Browse to the repo on GitHub.
2. Select the **Code** tab.
3. Click to expand the green **Code** button.

    ![GitHub clone repo -screenshot][img1]

4. Copy the HTTPS URL to the clipboard.

### [Git Bash command line](#tab/cmd-1)

1. Go to the folder you want to create the copy.

2. Run `git clone [INSERT REPO URL]`:

    ```bash
    git clone https://github.com/SuperOfficeDocs/contribute.git
    ```

    You can right-click to paste the URL to the command line.

3. Open the repo folder:

    ```bash
    cd contribute
    ```

### [VS Code](#tab/vscode-1)

1. Click the source control icon.
2. Expand **SOURCE CONTROL** and click the three dots to show more actions.
3. Select **Clone**.
4. Paste the repo URL you copied above.

![VS Code clone repo -screenshot][img2]

***

## Starting the workday

At the beginning of the workday, it is good practice to always get the latest updates from the branch you are going to work on. This is called **to pull**.

### [Git Bash command line](#tab/cmd-2)

1. Go to the repo folder.

2. Run `git pull`:

    ```bash
    git pull
    ```

![Git Bash pull -screenshot][img3]

### [VS Code](#tab/vscode-2)

1. Click the source control icon.
2. Expand **SOURCE CONTROL** and click the three dots to show more actions.
3. Select **Pull**.

    ![VS Code pull -screenshot][img4]

***

## Go to a branch to do work

If you are going to resume work where you left off the previous day, congratulations! You're already good-to-go with the latest updates.

To start something new, you need a **GitHub issue** and a **Git branch**.

Let's assume the issue is already on the backlog and assigned to you.

1. Go to GitHub.
2. Move the issue from **To do** to **In progress** to let your peers know what you are working on.
3. Note the **issue number**.

You can now **create a new branch:**

### [Git Bash command line](#tab/cmd-3)

1. Go to the repo folder.

2. Run `git switch`:

    ```bash
    git switch -c [INSERT NEW BRANCH NAME]
    ```

    The `-c` means *create*. Follow [branch naming conventions][4], starting with the issue number. For example, "256-release-notes-10.1.1".

### [VS Code](#tab/vscode-3)

**Option 1:**

1. Click the source control icon.
2. Expand **SOURCE CONTROL** and click the three dots to show more actions.
3. Point to **Branch** and then select **Create branch**.

    ![VS Code create branch -screenshot][img5]

4. Enter the name of your new branch.

    ![VS Code create branch -screenshot][img6]

**Option 2:**

1. Click the source control icon.
2. Expand **BRANCHES**
3. Click the + sign.

    ![VS Code create branch -screenshot][img7]

4. Enter the name of your new branch.

***

### Get new updates

During the workday, it might be a good idea to get additional updates from your colleagues. Simply **pull** on your current branch as you did earlier.

If your team is working on the same files, you might run into **merge conflicts**. More on handling these later. For now, here's a few tips to avoid conflicts:

* Commit before you pull (or switch branches)
* Pull before you push

If you're not ready to commit yet, you can **stash** the changes for later.

## Share your updates

Saving your changes is a three-step process:

1. Save the changes to your local disk (normal **Save file**).
2. Save the changes to your local Git repo (the clone). In Git terms, this is to **stage** and **commit**.
    * Stage (add) means to prepare the set of changes you want to add to Git version control.
    * Commit means to create a **snapshot** of those changes, adding a new version of those files to the Git history.
3. Publish the changes to GitHub (sync to cloud). In Git terms, **push**.

> [!TIP]
> Adding the issue number (for example #256) somewhere in the commit message automatically links your changes to the issue and lets others see what has been done.

### [Git Bash command line](#tab/cmd-4)

1. Go to the repo folder.

2. Run `git add`:

    ```bash
    git add .
    ```

    The dot means *add all changes*. See also this [how-to for more fine-grained staging][5].

3. Run `git commit`

    ```bash
    git commit -m "[INSERT MESSAGE]"
    ```

    The `-m` means *message follows*.

### [VS Code](#tab/vscode-4)

**Option 1:**

1. Click the source control icon.
2. Expand **SOURCE CONTROL** and click the three dots to show more actions.
3. Point to **Changes** and then select **Stage All Changes**.

    ![VS Code stage all changes -screenshot][img8]

4. Click the three dots again, point to **Commit**, and then select **Commit Staged**.

    ![VS Code commit -screenshot][img9]

5. Enter a commit message.

**Option 2:**

1. Click the source control icon.
2. Expand **SOURCE CONTROL**. Then expand **Changes**.
3. Click the **+ sign** on the heading to stage all changes. Click the + sign on individual files to stage just those.
4. Click the **checkmark** on the Source control heading to commit.
5. Enter a commit message.

***

## Finish an issue

* PR
* reviewer notifications

## Switch context - work on something else

## Done for the day - share all updates

<!-- Referenced links -->
[1]: how-to-edit-an-article-in-browser.md
[2]: how-to-edit-an-article.md
[3]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[4]: branch-strategy.md
[5]: git-cheat-sheet.md#saving-changes-to-your-repository

<!-- Referenced images -->
[img1]: media/github-clone.png
[img2]: media/vscode-clone.png
[img3]: media/gitbash-pull.png
[img4]: media/vscode-source-control-menu.png
[img5]: media/vscode-branch-menu.png
[img6]: media/vscode-create-branch.png
[img7]: media/vscode-branches.png
[img8]: media/vscode-stage-all-changes.png
[img9]: media/vscode-commit-menu.png

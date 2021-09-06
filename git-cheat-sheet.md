---
uid: git_commands
title: How to include code in docs
locale: en
so.topic: reference
so.date: 04.19.2021
so.author: Bergfrid Dias
---

# Git commands

Here we are using the Git Bash command line.

> [!NOTE]
> Paths are relative to your current directory

## Get the latest updates from GitHub

```sh
git pull
```

Unless you are working on your fork, make it a habit to pull:

* before you start every morning
* frequent during the day
* before you start a commit

Resolve any merge conflicts.

## Check local changes

```sh
git status
```

Checking status "all the time"? Create a convenient shorthand:

```sh
git config --global alias.st status
```

The next time you can just type `git st`. (Don't worry, `git status` will still work.)

## Inspect commit log

```sh
git log
```

## Saving changes to your repository

1. Tell Git what you want to save.

    * Everything:

    ```sh
    git add --all
    ```

    or

    ```sh
    git add .
    ```

    * A specific folder (recursive):

    ```sh
    git add docs/onsite
    ```

    * A specific file:

    ```sh
    git add docs/index.md
    ```

    > [!NOTE]
    > If you have moved or renamed a file without using `git mv`, you must add both the old and the new file or folder name!

2. Commit your saved changes to your local repository.

    ```sh
    git commit -m "#[ISSUE ID] Short description of changes"
    ```

3. Send your changes to GitHub.

    ```sh
    git push
    ```

    * If you didn't set the upstream when you created the branch, you need to do it now:

    ```sh
    git push --set-upstream origin <branchname>
    ```

You've done it! Your code is now up in your GitHub repository!

> [!TIP]
> Need to fix something you submitted? No problem! Just make your changes in the same branch and then commit and push again.

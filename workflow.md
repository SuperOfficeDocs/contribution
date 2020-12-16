---
title: Git workflows for SuperOffice Docs
---

# Workflows

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

## Saving changes to your repository

1. Tell Git what you want to save.

  * Everything:

```sh
git add --all
```

  * A specific folder (recursive):

```sh
git add docs/onsite
```

* A specific file:

```sh
git add docs/index.md
```

2. Commit your saved changes to your local repository.

```sh
git commit -m "Short description of changes"
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

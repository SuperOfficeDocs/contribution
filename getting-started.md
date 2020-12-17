---
title: Getting started
---

# Getting started with SuperOffice Docs

## Set up your GitHub account

To contribute to SuperOffice Docs content, you need to set up your own GitHub account.

If you don't already have a GitHub account, [create one](https://github.com/join) now.

## Install content authoring tools

### Install Git client tools

Install the latest version of Git client tools for your platform. Follow the instructions for your chosen client for installation and configuration.

* [Git for Windows](https://git-scm.com/download/win). Includes the Git version control system and Git Bash, the command-line app. We recommend also installing the Git Credential Manager (included in the default installation).
* [Git for Mac](https://git-scm.com/download/mac): Run `git` from the command line. You will be prompted to install the command line tools if needed.
* [Git for Linux and Unix](https://git-scm.com/download/linux)

If you prefer a graphical user interface (GUI) over a command-line interface, consider [GitHub's GitHub Desktop](https://desktop.github.com/).

**Additional Git resources:** [Git terminology](https://help.github.com/articles/github-glossary) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## Install Markdown editor

Markdown is a lightweight markup language. [Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at SuperOffice.

Markdown text is saved into files with .md extension. Learn more in our [Markdown reference](markdown-reference.md).

### Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac. It includes git integration, and support for extensions.

Download and install [VS Code](https://code.visualstudio.com/).

Next, we will install some extensions recommended for SuperOffice Docs.

### Docs Authoring Pack

Install the Docs Authoring Pack for Visual Studio Code. It includes basic authoring assistance for help when writing Markdown.

Search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window, or [go to the marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**.

### Blueprint - New Files and Folders of Files from Templates

Install the Blueprint extension for VS Code.

Search for `teamchilla.blueprint` in your extensions list in the VS Code window, or [go to the marketplace page](https://marketplace.visualstudio.com/items?itemName=teamchilla.blueprint) and select **Install**.

### GitLens — Git supercharged

Install the GitLens extension for VS Code.

Search for `gitlens` in your extensions list in the VS Code window, or [go to the marketplace page](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) and select **Install**.

### Markdown Kit

Install the Markdown Kit extension for VS Code. We use it primarily to paste HTML as Markdown.

Search for `markdown-kit` in your extensions list in the VS Code window, or [go to the marketplace page](https://marketplace.visualstudio.com/items?itemName=svsool.markdown-kit) and select **Install**.

### Other relevant extensions

* [Sort lines](https://marketplace.visualstudio.com/items?itemName=Tyriar.sort-lines)
* [Markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
* [LinkCheckMD](https://marketplace.visualstudio.com/items?itemName=blackmist.LinkCheckMD)
* [Code spell checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

## Set up Git repository locally for documentation

To contribute to SuperOffice Docs, you can make and edit Markdown files locally by cloning the corresponding documentation repository.

* SuperOffice employees and members of the SuperOffice Docs GitHub organization may clone and commit to the repositories directly.
* All other contributors must fork the repo to their own GitHub account, clone the fork, and submit changes as pull requests back to us.

### Determine the repo (all)

Documentation hosted at [docs.superoffice.com](https://docs.superoffice.com/) resides in several different repositories at [github.com](https://www.github.com/).

As a starting point, you can use the *superoffice-docs* repo.

> [!TIP]
> Not sure  which repository to use? Visit the article on `docs.superoffice.com` using your web browser. Select the **Edit** link (pencil icon). That link takes you to the GitHub location for the corresponding Markdown file in the appropriate repo.

### Choose a local folder (all)

Make a local folder to hold a copy of the repository locally.

1. Create the root folder for SuperOffice docs, for example, `C:/code/docs/`. The name should be easy for you to remember and type.

> [!CAUTION]
> Don't use a local folder path that is nested inside of another git repository. That would mess up the file tracking.

2. Launch Git Bash. Type `pwd` at the $ prompt to determine the current directory.

3. Change directory (cd) into the folder that you created for hosting the repository locally. For example, `cd /c/code/docs/`.

### Fork the repository (external)

Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.

1. Go to the main repository's GitHub page and click the **Fork** button on the upper right.
2. If you are prompted, select your GitHub account tile as the destination where the fork should be created.

Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.

### Create a local clone (all)

Using Git Bash, prepare to run the **clone** command to pull a copy of a repository down to your device on the current directory. This will create a new folder within the current folder.

#### Find the GitHub URL for the clone command

**SuperOffice employee:** From the main repo, click **Code** and copy the HTTPS URL: `https://github.com/SuperOfficeDocs/<repo>.git`

**Contributor:** Copy the URL from the **Clone or download** button in the GitHub UI using *your fork*: `https://github.com/<github-username>/<repo>.git`

#### Clone

1. Run the **clone** command, by providing the repository name. Cloning downloads (clone) the repository on your local computer.

  Using a fork:
```sh
git clone https://github.com/<github-username>/<repo>.git
```

  Directly:
```sh
https://github.com/SuperOfficeDocs/<repo>.git
```

2. When you're prompted, enter your GitHub credentials.

3. When you're prompted, enter your two-factor authentication code.

4. The clone command runs and downloads a copy of the repository files from GitHub into a new folder on the local disk. This may take a few minutes, depending on the repository size.

You can now explore the folder to see the structure.

Continue reading our [GitHub fundamentals](github-fundamentals.md) and explore the other guidelines in the contribution guide.

Want to dive right in? Check out the [workflows](workflows.md).

---
uid: branch_strategy
locale: en
title: Branch strategy for SuperOfficeDocs
description: We use feature branches to isolate work in progress from the completed work in the main branch.
so.topic: tutorial
so.date: 04.19.2021
so.author: Bergfrid Dias
---

## Branch strategy

Our main branch is **main**, which the live SuperOfficeDocs is built from.

We use feature branches to isolate work in progress from the completed work in the main branch. Even small fixes and changes should have their own branch. This simplifies the review process and creates an accurate history of changes.

* Create a feature branch for all new features and bug fixes.
* Base the feature branch on the main branch.
* Create pull requests to merge feature branches into the main branch.
* Use lowercase letters, numbers, and hyphens only.

**Naming conventions:**

* \<docs issue>-feature-name
* \<docs issue>-description
* bugfix-description

**Create a new local branch with Git Bash:**

```sh
git checkout -b "branchname"
git push -u origin "branchname"
```

Each Git client is different, so consult the help for your preferred client.

### Pull requests

* Require a pull request to merge code.
* Code merged into the main branch should build cleanly.
* Squash merge.

### Release branches (versioning)

Release branches are long-lived and not merged back into the main branch.

TBD

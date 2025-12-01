---
sidebar_position: 12
---

# Stash

The git stash command is used to store uncommited changes made in a branch so they can be moved to another branch or to allow context switching between branches when uncommited changes are not ready to be commited.

## Store changes

To store uncommited changes use `git stash` which will stash all changes in the branch:

```
$ git stash
Saved working directory and index state WIP on new-branch: 740d33d feat: initial github guidelines gpg key documentation
```

## Pop changes

To recover the stashed uncommited changes first change to the desired branch for the changes with [checkout](./checkout.md) and then use the `pop` sub-command:

```
$ git stash pop
Auto-merging docs/git-commands/checkout.md
On branch 02-git-commands
Your branch is ahead of 'origin/02-git-commands' by 5 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   docs/git-commands/checkout.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (bf039cd4b9b81184d343400d5ab9ab73856931bc)
```
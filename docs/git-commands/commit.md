---
sidebar_position: 8
---

# Commit

The git commit command is used to save changes that are staged in the local repository with a description of what the changes are accomplishing.

## Create a new commit

To create a new commit containing currently staged changes added with the [add](./add.md) command in the local repository use:

`git commit -m "<message>"`

Where `<message>` is the message that you want to include describing the commit.

## Create a new commit without first staging

To create a new commit including all tracked file changes in the local repository without first using [add](./add.md) use the `-a` flag:

`git commit -a -m "<message>"`

Where `<message>` is the message that you want to include describing the commit.

## See a log of commits on the local repository

To see a log of the current commits history on the local the local repository use:

`git log`
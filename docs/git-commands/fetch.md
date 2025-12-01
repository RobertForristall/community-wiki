---
sidebar_position: 5
---

# Fetch

The git fetch command allows you to check for any changes made to a remote repository that the local repository is linked to using `git fetch <remote-name>`

NOTE: This will not pull those changes to your local machine; all that fetch does is checks if there are changes available in the remote repository that are not already known about by the local repository. To actually pull those changes you must use the git [pull](./pull.md) command

```
$ git remote -v
origin  git@github.com:RobertForristall/community-wiki.git (fetch)
origin  git@github.com:RobertForristall/community-wiki.git (push)
upstream        git@github.com:Code-after-Coffee/community-wiki.git (fetch)
upstream        git@github.com:Code-after-Coffee/community-wiki.git (push)

$ git fetch upstream
Enter passphrase for key '/c/Users/rober/.ssh/id_ed25519': 
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 906 bytes | 453.00 KiB/s, done.
From github.com:Code-after-Coffee/community-wiki
 * [new branch]      main       -> upstream/main
```
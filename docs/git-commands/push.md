---
sidebar_position: 9
---

# Push

The git push command pushes commits and new branches that have been made in the local repository that are not yet present in a linked remote repository.

## Push new commits

To push new commits made in the active branch of the local repository to a linked remote repository use:

`git push <remote-name> <remote-branch-name>`

Where `<remote-name>` is the name of the linked remote repository found using the [remote](./remote.md) command and `<remote-branch-name>` is the name of the branch on the remote repository you want to push to.

```
$ git push origin 02-git-commands
Enter passphrase for key '/c/Users/rober/.ssh/id_ed25519': 
Enumerating objects: 96, done.
Counting objects: 100% (96/96), done.
Delta compression using up to 16 threads
Compressing objects: 100% (63/63), done.
Writing objects: 100% (82/82), 74.11 KiB | 4.63 MiB/s, done.
Total 82 (delta 39), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (39/39), completed with 4 local objects.
To github.com:RobertForristall/community-wiki.git
   96432c2..4db2fed  02-git-commands -> 02-git-commands
```

## Push a new branch with its commits

To push a new branch along with its commits first switch to the branch using [checkout](./checkout.md) then use the `-u` flag:

`git push -u <remote-name> <remote-branch-name>`

Where `<remote-name>` is the name of the linked remote repository found using the [remote](./remote.md) command and `<remote-branch-name>` is the name of the branch on the remote repository you want to push to.

The `-u` flag tells the local repository to track its commit history against the remote repository branch that you made during the push.

## Force pushing commits

IMPORTANT NOTE: This flag should only be used in very special circumstances like after performing a [rebase](./rebase.md) as it will fully overwrite the commit history and changes of the remote repository with what is currently in the local repository.

To overwrite the commit history and changes of the remote repository with what is currently in the local respository use the `--force` flag:

`git push --force <remote-name> <remote-branch-name>`

Where `<remote-name>` is the name of the linked remote repository found using the [remote](./remote.md) command and `<remote-branch-name>` is the name of the branch on the remote repository you want to push to.
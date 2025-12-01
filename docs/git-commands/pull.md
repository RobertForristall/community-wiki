---
sidebar_position: 6
---

# Pull

The git pull command pulls changes made in a remote repository branch to the local repository active branch of your machine.

This should be done anytime changes are detected in the main branch of a repository and there are no conflicts with trying to pull those changes.

NOTE: You need to [fetch](./fetch.md) changes first from the remote repository that you plan to pull from.

```
$ git branch
  01-github-guidelines
  02-git-commands
* main

$ git fetch upstream
Enter passphrase for key '/c/Users/rober/.ssh/id_ed25519': 
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 906 bytes | 453.00 KiB/s, done.
From github.com:Code-after-Coffee/community-wiki
 * [new branch]      main       -> upstream/main

$ git pull upstream main
Enter passphrase for key '/c/Users/rober/.ssh/id_ed25519': 
From github.com:Code-after-Coffee/community-wiki
 * branch            main       -> FETCH_HEAD
Updating c4ccc24..96432c2
Fast-forward
 docs/git-commands/checkout.md                     |   5 ++
 docs/git-commands/cherry-pick.md                  |   2 +-
 docs/git-commands/fetch.md                        |   2 +-
 docs/git-commands/pull.md                         |   2 +-
 docs/git-commands/push.md                         |   2 +-
 docs/git-commands/rebase.md                       |   2 +-
 docs/github-guidelines/actions.md                 |  79 +++++++++++++++++++++-
 docs/github-guidelines/branches.md                |  20 +++++-
 docs/github-guidelines/fork.md                    |  23 ++++++-
 docs/github-guidelines/gpg-keys.md                |  33 ++++++++-
 docs/github-guidelines/issues.md                  |  32 ++++++++-
 docs/github-guidelines/organization.md            |  19 +++++-
 docs/github-guidelines/projects.md                |  39 ++++++++++-
 docs/github-guidelines/pull-requests.md           |  45 +++++++++++-
 docs/github-guidelines/rulesets.md                |  41 ++++++++++-
 docs/github-guidelines/ssh-keys.md                |  35 +++++++++-
 docs/intro.md                                     |  12 ++--
 static/img/github-guidelines-fork-01.png          | Bin 0 -> 104866 bytes
 static/img/github-guidelines-fork-02.png          | Bin 0 -> 55923 bytes
 static/img/github-guidelines-issues-01.png        | Bin 0 -> 128768 bytes
 static/img/github-guidelines-projects-01.png      | Bin 0 -> 56807 bytes
 static/img/github-guidelines-projects-02.png      | Bin 0 -> 64961 bytes
 static/img/github-guidelines-projects-03.png      | Bin 0 -> 53598 bytes
 static/img/github-guidelines-pull-requests-01.png | Bin 0 -> 66712 bytes
 static/img/github-guidelines-pull-requests-02.png | Bin 0 -> 78024 bytes
 static/img/github-guidelines-pull-requests-03.png | Bin 0 -> 15315 bytes
 static/img/github-guidelines-rulesets-01.png      | Bin 0 -> 47113 bytes
 static/img/github-guidelines-rulesets-02.png      | Bin 0 -> 53731 bytes
 static/img/github-guidelines-rulesets-03.png      | Bin 0 -> 52313 bytes
 static/img/github-guidelines-rulesets-04.png      | Bin 0 -> 65043 bytes
 30 files changed, 373 insertions(+), 20 deletions(-)
 create mode 100644 docs/git-commands/checkout.md
 create mode 100644 static/img/github-guidelines-fork-01.png
 create mode 100644 static/img/github-guidelines-fork-02.png
 create mode 100644 static/img/github-guidelines-issues-01.png
 create mode 100644 static/img/github-guidelines-projects-01.png
 create mode 100644 static/img/github-guidelines-projects-02.png
 create mode 100644 static/img/github-guidelines-projects-03.png
 create mode 100644 static/img/github-guidelines-pull-requests-01.png
 create mode 100644 static/img/github-guidelines-pull-requests-02.png
 create mode 100644 static/img/github-guidelines-pull-requests-03.png
 create mode 100644 static/img/github-guidelines-rulesets-01.png
 create mode 100644 static/img/github-guidelines-rulesets-02.png
 create mode 100644 static/img/github-guidelines-rulesets-03.png
 create mode 100644 static/img/github-guidelines-rulesets-04.png
```
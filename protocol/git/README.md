# Git Protocols

A guide for programming with version control.

## Maintain a Repo

* Avoid including files in source control that are specific to your
  development machine or process.
* Delete local and remote feature branches after merging.
* Perform work in a feature branch.
* `Master` should always be the currently released version.
* `Develop` is the branch receiving current development.

## Write a Feature

Create a local feature branch based off `develop`.

```shell
$ git checkout develop
$ git pull
$ git checkout -b feature/<feature_name>
```

Rebase frequently to incorporate upstream changes.

```shell
$ git fetch origin
$ git rebase origin/master
```

Resolve conflicts!

When the feature is complete and tests pass, stage the changes.

```shell
$ git add --all
```

When you've staged the changes, commit them.

```shell
$ git status
$ git commit --verbose
```

Write a [good commit message][tpope]. Example format:

```
Present-tense summary under 50 characters

* More info about commit (under 72 characters)
* More info about commit (under 72 characters)

closes/references #123
```

If you've created more than one commit, use a rebase to squash them into
cohesive commits with *good* messages.

```shell
$ git rebase -i origin/master
```

Share your branch.

  $ git push origin <branch-name>

Ask for a code review in the IRC room.

## Review Code

A team member other than the authoer reviews the code before it is
merged in to the `develop` branch. Please follow the [Code Review
Guidelins][code review].

Code reviewers make comments and ask questions directly on lines of code
in the GitHub web interface or the project's chat room.

Code reviewers can checkout the appropriate branch, test the feature on
their machine, run tests, commit, and push to `origin`.

## Merge

When both the feature author and reviewer are statisfied, rebase the
code interactively and squash commits like "Fix whitespace" into one (or
a small) number of commits. Edit commit messages to reveal intent. **Rerun
tests**.

  $ git fetch origin
  $ git rebase -i origin/develop

Push your branch and view a list of new commits.

```shell
$ git push origin <branch_name>
$ git log origin/develop..<branch_name>
$ git diff --stat origin/develop
$ git checkout develop
$ git merge <branch-name> --ff-only
$ git push
```

Delete your remote feature branch.

  $ git push origin --delete <branch_name>

Delete your local feature branch.

  $ git branch --delete <branch_name>

[code review]: ../../code-review
[tpope]: http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html

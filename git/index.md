# Tips and Best Practices of using Git

## Only show changes for pom.xml files

We could use patterns for the most of git command.
For example:

```bash
# check difference,
git diff pom.xml **/pom.xml

# check status.
git status pom.xml **/pom.xml
```

Find all `pom.xml` files and check status:
```bash
find . -name pom.xml -exec git status {} +
```

## Name only log output

```bash
git log --name-only
```

## Branch uptream

Some tips:

```bash
# remove a branch
git branch -d BRANCH_NAME

# show branch details:
git branch -avv
```

## Sync fork with upstream.

```bash
# add upstream
git remote add upstream git...

# fetch upstream
git fetch upstream

# checkout the branch
git checkout B_NAME

# merge the upstream branch
git merge upstream/B_NAME

# if B_NAME is a new branch from upstream,
# we just need push it to origin (fork repo).
# option -u will set the upstream
git push -u origin B_NAME
```

## Git commit reset author.

This command is also very useful to update the comments for the most recent commit.

```bash
git commit --amend --reset-author
```

## How to change commit message in romte?

There 2 options:
* git commit --amend
* git rebase -i HEAD~1

Good reference:
* [How to Change a Git Commit Message](https://linuxize.com/post/change-git-commit-message/)

## Combine (squash) commits into one

References:
* [Squash commits into one with Git](https://www.internalpointers.com/post/squash-commits-into-one-git)

## Errors and troubleshooting

For error **fatal: Not possible to fast-forward, aborting**:
The simple fix is pull with rebase option:

```bash
git pull --rebase
```

## Create pull request for a sepcific commit

The basic steps:

* create a new branch from the upsteam remote
* push the new branch to origin
* cherry pick the commit
* create pull request from the new branch

Here is good reference page: [How to create a pull request with a specific commits?](https://poanchen.github.io/blog/2017/11/12/How-to-create-a-GitHub-pull-request-with-a-specific-commits)

## Git stash

Reference post:
* [Git stash](https://opensource.com/article/21/4/git-stash)

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

Sync fork with upstream.

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
git push -u origin B_NAME
```

Git commit reset author.
This command is also very useful to update the comments for the most recent commit.

```bash
git commit --amend --reset-author
```

## Errors and troubleshooting

For error **fatal: Not possible to fast-forward, aborting**:
The simple fix is pull with rebase option:

```bash
git pull --rebase
```

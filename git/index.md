# Tips and Best Practices of using Git

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

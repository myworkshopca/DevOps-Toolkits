# Tips and best practices for Vim

Vim is the best editor for DevOps.
This page will provide a list of tips, tricks, and best practices for using vim.

## search and replace

Search and replace within current buffer.

```vim
# Search replace in multiple lines:
:%s/abc\_.*def/af/gc
```

The *\\_.* will match any character including the new line.

Reference page:

* [Search across multiple lines](https://vim.fandom.com/wiki/Search_across_multiple_lines)

### bufdo to search replace in multifiles

```vim
:bufdo %s/from/to/g | update
```

The **update** command will save all updated fuffers.


## Open multiple files at once

```bash
# open all java files using javax.ws package.
vim `grep -lr --include=*.java --exclude=*/target/* 'javax.ws' .`
```

## args and argdo

Check the post:

* [vim search replace all files in current folder](https://vi.stackexchange.com/questions/2776/vim-search-replace-all-files-in-current-project-folder#:~:text=If%20you%20want%20to%20perform,multiple%20filenames%20or%20even%20globs.&text=You%20can%20view%20the%20current,by%20running%20%3Aargs%20by%20itself.)

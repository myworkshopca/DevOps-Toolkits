# Tips and best practices for Vim

Vim is the best editor for DevOps.
This page will provide a list of tips, tricks, and best practices for using vim.

## search and replace

Search and replace within current buffer.

```vim
# Search replace in multiple lines:
:%s/abc\_.*def/af/gc
```

The *\_.* will match any character including the new line.

Reference page:
* [Search across multiple lines](https://vim.fandom.com/wiki/Search_across_multiple_lines)

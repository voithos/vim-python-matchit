vim-python-matchit
==================

This is a modified clone of the
[Python matchit](http://www.vim.org/scripts/script.php?script_id=386) plugin
from vim.org, based on script version `0.5`.

This is originally cloned from https://github.com/voithos/vim-python-matchit as
https://github.com/osamuaoki/vim-python-matchit and modified.

In python, 'for'/'while'-block can take 'else' which was not supported in the
original 0.5.  This mod, 0.5.1, addresses this situation.

## Originally created by
Benji Fisher

## Modified by
Osamu Aoki

## script type
ftplugin

## description
This script redefines the % motion so that (in addition to its usual behavior)
it cycles through if/elif/else, try/except/catch/else, for/continue/break/else,
and while/continue/break/else structures.  The script also
defines g% to cycle in the opposite direction.  Two other motions, [% and ]%,
go to the start and end of the current block, respectively.

All of these motions should work in Normal, Visual, and Operator-pending
modes.  For example, d]% should delete (characterwise) until the end of the
current block; v]%d should do the same, going through Visual mode so that
you can see what is being deleted; and V]%d makes it linewise.

## install details
Copy the file to your ftplugin/ directory.  If, for some reason, you want to
change the name of the file, copy it to ftplugin/python/ or :source it from
ftplugin/python.vim .

If you use the native Vim package management and use `git` and `git submodule`
to manage `~/.vim/` contents like me, install this under `~/.vim/pack/*/opt/`.
(`*` can be any name)

Then in your vimrc (`~/.vim/vimrc`), add

```
packadd! vim-python-matchit
```

Osamu

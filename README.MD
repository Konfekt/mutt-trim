# mutt-trim

This script removes any clutter of the quoted text when responding.
To be used with mutt by adding

```
set editor          = "mutt-trim %s; $EDITOR %s"
```

to your `~/.muttrc` file.

To fold quotation levels in Vim, add the lines

```vim
setlocal foldexpr=strlen(substitute(matchstr(getline(v:lnum),'\\v^\\s*%(\\>\\s*)+'),'\\s','','g')) 
setlocal foldmethod=expr foldlevel=1 foldminlines=2
```

to a file `~/.vim/after/ftplugin/mail.vim`.

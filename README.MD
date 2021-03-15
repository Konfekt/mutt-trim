# mutt-trim

This script removes any clutter of the quoted text when responding.
To be used with mutt by adding

```
  set editor          = "mutt-trim %s; $EDITOR %s"
```

to your `~/.muttrc`.

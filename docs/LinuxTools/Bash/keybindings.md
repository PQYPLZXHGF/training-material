# Keybindings in the termial

## Default: Emacs-style keybindings

By default, the terminal running bash support the Emacs keybindings, e.g.,
  * `ctrl-a` to move to the start of the input,
  * `ctrl-e` to move to the end of the input,
  * `alt-b` to move back a word,
  * `alt-f` to move forward a word, and so on.

A nice [cheat sheet](https://github.com/fliptheweb/bash-shortcuts-cheat-sheet) for the default keybindings can be helpful.


## vi-style keybindings

However, this default behavior can be changed to vi keybindings, including
a command and an insert mode.  To get this to work, you need a file
named `.inputrc` in your home directory with the following contents.
```
set editing-mode vi
set keymap vi-command
```

The prompt starts in insert mode, so you can type as usual.  To switch to
command mode, hit `ESC`. Now many of the vi commands work, e.g.,
  * `^` to move to the start of the input,
  * `$` to move to the end of the input,
  * `b` to move backward a word,
  * `w` to move forward a word,
  * `\<search-string>` to search your history backward, and so on.

The main time savers are of course vi's movement operators in
command mode, e.g., `3f/` would move the cursor to the third slash,
starting to count from its current location.

A convenient [cheat sheet](http://www.catonmat.net/download/bash-vi-editing-mode-cheat-sheet.pdf) in PDF format is available.

It takes some time getting used to, but will save you quite some keystrokes
at the end of the day.

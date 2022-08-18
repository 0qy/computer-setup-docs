# Key Remap

To execute key remap: use the `key` command in your zsh shell.
Remap `Caps Lock` key to `Escape` in order to easily exit insert mode in vim.
Created `./scripts/key.sh/`

```
#!/bin/bash

xmodmap -e "keycode 66 = Escape"

```

### Two ways to find out keyCode and keySum

1. `xmodmap -pk`
   This prints all the key mappings in your terminal

2. `xev`
   Logs the event in terminal when key is pressed

### To make your script executable

`sudo chmod 774 key.sh`

### Add line to .zshrc

`alias key='./scripts/key.sh'`

# VIM editor

## Websites

- https://vim-cheat-sheet.now.sh
- [Colours in terminal](https://gist.github.com/XVilka/8346728)

## Commands

- `q/` - opens search history window
- `q:` - opens command history window
- `:g!/dont/d` - delete all lines not containing the string `dont`
  - `g` - is the global command
  - `d` - stands for delete
  - `!` - inverts the matching
- `:g/delete-me/d` - delete all lines containing the string `delete-me`
- `:!command` - executes an external command.
- `:r` or `:read` - read command
  - `:r FILENAME` - retrieves disk file FILENAME and puts it below the cursor position.
  - `:r !ls` - reads the output of the dir command and puts it below the cursor position.
- `R` - replace mode. Like insert mode but deletes existing characters
- When typing a  `:` command, press `Ctrl-d` to see possible completions. Press `<TAB>` to use one completion.

### Substitute cmds

`:s` is just shortcut for `:substitute`

- `:s/old/new` - to substitute `new` for the first `old` in a line    
- `:s/old/new/g` - to substitute `new` for all `old's` on a line
- `:#,#s/old/new/g` - to substitute phrases between two line #'s
- `:%s/old/new/g` - to substitute all occurrences in the file
- `:%s/old/new/gc` - to ask for confirmation each time add `c`


## Search

- `/\ccase insensitive search` - use `\c` switch
- `/\Ccase sensitive search` - use `\C` switch

## Text editing

- `daw` deletes the whole word wherever the cursor is
- `dip` `d`elete `i`nside `p`aragraph
- `di{` `d`elete `i`nside `{` curly braces
- `vip` `v`isual select `i`nside `p`aragraph
- `cip` `c`hange `i`nside `p`aragraph
- `gU` - change text to UPPERCASE
- `gu` - change text to lowercase

## Navigation

- `Ctrl+o` - back
- `Ctrl+i` - forward
  - `:jumps` - displays jumps for current window
- `<number> + G` go to line <number>
- `Ctrl+g` shows info about current position within the file in the bottom line
- `H` - Highest line on the screen
- `M` - Middle line on the screen
- `L` - Lowest line on the screen
- `zt` - scroll view so that cursor is aligned to the `t`op
- `zz` - scroll view so thet cursor is aligned in the middle
- `zb` - scroll view so that cursor is aligned to the `b`ottom

  
### Tabs

- `gt` (or `:tabn`) - to go to next tab
- `gT` (or `:tabp` or `:tabN`) - to go to previous tab
- `#gt` (or `:tabn #`) - to go to #th tab
  
### Splits

- `Ctrl+w` followed by capital `H`,`J`,`K` or `L` will move the current window to the far left, bottom, top or right respectively like normal cursor navigation

## Motions

- `g;` - go to most recent modification in the document
  - press again and you go to most recent - 1
- `` `.`` go to most recent modification
- `` `^`` go to last insertion
- `0` go to the start of the line
- `^` go to the first character on the line
- 

## Spell checking

- `:setlocal spell` enable spell checking
- `:set nospell` disable spell check
- `]s` move to next misspelled word
- `[s` move to previous misspeled word
- `zg` mark word as a good word
- `zG` mark good just for current instance (will be lost after restart)
- `zw` mark word as wrong word
- `zW` mark word as wrong word for current instance
- `z=` suggest correction

## Registers (a.k.a. clipboard)

- `"byy` copy to `b` register
- `"bp` paster from `b` register
- `"bdd` delete to `b` register

## Insert mode

- `Ctrl+w` delete back one word
- `Ctrl+u` delete all entered characters before the cursor
- `Ctrl+h` delete one character (backspace)
- `Ctrl+o` enters Insert Normal Mode -> You can execute one command (e.g.: `zz`) and then return back to Insert mode

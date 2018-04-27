# VIM editor

## Websites

- https://vim-cheat-sheet.now.sh

## Commands
- `q/` - opens search history window
- `q:` - opens command history window
- `:g!/dont/d` - delete all lines not containing the string `dont`
  - `g` - is the global command
  - `d` - stands for delete
  - `!` - inverts the matching
- `:g/delete-me/d` - delete all lines containing the string `delete-me`

## Search

- `/\ccase insensitive search` - use `\c` switch
- `/\Ccase sensitive search` - use `\C` switch

## Text editing

- `daw` deletes the whole word wherever the cursor is
- `dip` `d`elete `i`nside `p`aragraph
- `di{` `d`elete `i`nside `{` curly braces

## Navigation

- `Ctrl+o` - back
- `Ctrl+i` - forward
  - `:jumps` - displays jumps for current window
  
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

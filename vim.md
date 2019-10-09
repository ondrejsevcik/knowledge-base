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
- `q/` - opens a command window with history of searches
- `q:` - opens a command window with history of Ex commands
- `2,$!sort -k2` - execute `sort` cmd in terminal on lines `2-end` with `-k2` arg to sort by items in second column
- `edit %:h` - edit active file directory

#### Copy & move

`:copy` or `:co` or `:t`
`:move` or `:m`

- `:copy $` - copy current line to the end
- `:t6` - copy current line below line 6
- `:6t.` - copy line 6 below current line
- `:m$` - move current line at the end of the file

#### Normal cmd

- `:.,$normal A;` - append `;` at the end of each line from the current one till the last one


### Under the hood

- `:{start},{end}{command}`
  - `.` - current line
  - `$` - last line
  - `1` - first line
  - `0` - zero line (used when you move test to beginning for example `:move 0`)
  - `%` - all lines in the file
  - `<` - start of visual selection
  - `>` - end of visual selection
- `:1,10d` - delete lines 1-10
  - `:.,$copy` - copy from current line `.` till the end `$`


### Substitute cmds

`:s` is just shortcut for `:substitute`

- `:s/old/new` - to substitute `new` for the first `old` in a line    
- `:s/old/new/g` - to substitute `new` for all `old's` on a line
- `:#,#s/old/new/g` - to substitute phrases between two line #'s
- `:%s/old/new/g` - to substitute all occurrences in the file
- `:%s/old/new/gc` - to ask for confirmation each time add `c`

#### Project-wide search and replace

```shell
/Rg "old" # will populate quick-fix list
:cfdo %s/old/new/gc # will ask you if you want to replace 'old' with 'new' for each occurence in quick-fix list
:wa #write all to disk
```


## Search

- `/\ccase insensitive search` - use `\c` switch
- `/\Ccase sensitive search` - use `\C` switch
- `g*` search for word under cursor with partial word matching

## Text editing

- `daw` deletes the whole word wherever the cursor is
- `dip` `d`elete `i`nside `p`aragraph
- `das` `d`elete `a`round `s`entence
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
  
### Automatic Marks

- `"` position before the last jump within current file
- `'.` location of last change
- `'^` location of last insertion
- `'[` start of last change or yank
- `']` end of last change or yank
- `'<` start of last visual selection
- `'>` end of last visual selection

  
### Tabs

- `gt` (or `:tabn`) - to go to next tab
- `gT` (or `:tabp` or `:tabN`) - to go to previous tab
- `#gt` (or `:tabn #`) - to go to #th tab


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

## Netrw explorer 

- `-` go one level up in direcotry tree
- `:Vex` vertical split
- `:Sex` horizontal split
- `%` create new file
- `R` rename file
- `D` delete file
- `d` create new dir
- `i` change view

## Registers (a.k.a. clipboard)

- `"{register-name}{y|p|d}`
- `"byy` copy to `b` register
- `"bp` paster from `b` register
- `"bdd` delete to `b` register
- `o` register holds what was `yank`ed most recently
- lowercase letter overwrites register, uppercase appends to it
- `"_` black hole register - a place from which nothing returns
- `*` register references system clipboard (`"*p`, `"*y`)


## Buffers

- `:buffers` or `:ls` to list all open buffers
- `:ball` opens all buffers in windows
- `:bd` close current buffer (buffer delete)
- `:bnext` or `:bn`
- `:bprev` or `:bp`
- `:only[!]` close all other buffers except this one (add ! to close even unsaved ones)

## Windows

- `Ctrl+w =` resize windows equally
- `Ctrl+w 10 >` change width to left by 10
- `Ctrl+w 10 <` change width to right by 10
- `Ctrl+w 10 +` incerease height by 10
- `Ctrl+w 10 -` decrease height by 10
- `:res[ize] +10` increase window height/width by 10
- `:res[ize] -10` decrease window height/width by 10
- `z10` set height/width to 10

### Splits

- `Ctrl+w` followed by capital `H`,`J`,`K` or `L` will move the current window to the far left, bottom, top or right respectively like normal cursor navigation
- `Ctrl+w` followed by `Shift+T` will move split to new tab

## Insert mode

- `Ctrl+w` delete back one word
- `Ctrl+u` delete all entered characters before the cursor
- `Ctrl+h` delete one character (backspace)
- `Ctrl+o` enters Insert Normal Mode -> You can execute one command (e.g.: `zz`) and then return back to Insert mode

## Visual mode

- `Ctrl+v` block-wise visual mode
- `gv` reselect the last visual selection
- `o` go to the other end of visual selection

## Folding

> Collapsing multiple lines of text into single line

- `zf{motion}` - fold (e.g.: `zf{` folds inside `{}` brackets)
- `za` - toggle fold
- `zR` - open all folds in current buffer
- `zM` - close all folds in current buffer
- `zc` - close fold
- `zo` - open fold
- `zd` - delete fold under cursor (not text, just fold)

## Macros

- `q{a-z}` to record
- `@{a-z}` to replay
- `@@` to replay the most recently replayed macro

## External commands

- `:%!<command>` - runs external command with current buffer content
- `:%!sort` will run `sort` with current buffer

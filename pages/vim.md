---
title: vim
---
## editing.txt
- `^^` edit the alternate file

## motion.txt






### operator
- `c` change
- `d` delete
- `y` yank
- `g~` swap case (`~` with `'tildeop'`)
- `gu` lowercase
- `gU` uppercase
- `!` filter through external program
- `=` indent
- `gq` format text
- `<` `>` shift

### left-right-motions
- `h`,  `l`: single steps
- `0`, `^`: first (non-blank)
- `$`: last
- `g0`, `g^`, `g$`: same for screen lines
- `f`, `t`: find in line (till)
- `F`, `T`: backwards
- `;`, `,`: repeat (backwards)

### up-down-motions
- `j`, `k`: single steps
- `gj`, `gk`: up/down display lines
- `G`: go to `[count]` (default last) line
- `gg`: go to first line
- `go`: go to `[count]` byte

### word-motions
- `w`, `e`, `b`, `ge`: forward/back start/end of word
- `W`, `E`, `B`, `gE`: same for WORD

### object-motions
- `(`, `)`: sentences
- `{`, `}`: paragraphs

### text-objects
- `aw`, `aW`: a word, WORD
- `iw`, `iW`: inner word, WORD
- `as`, `is`: a sentence, inner sentence
- `ap`, `ip`: a paragraph, inner paragraph
- `at`, `it`: a tag

### jump-motions
- `CTRL-O`, `CTRL-I`: back, forward in jump list
- `:ju[mps]`: show jumplist
- `g;`, `g,`: go to previous, next position in the changelist
- `:changes`: show changelist

### various-motions
- `H`, `M`, `L`: Home, Middle, Last line of window

## scroll.txt
- `zz`: center current line

## insert.txt
- `i`, `a`: insert, append
- `A`: append to end of line
- `o`, `O`: new line after/before

## pattern.txt
- `/`, `?`: search (backwards)

## windows.txt

### 1. windows-intro
Buffers can be active, hidden or inactive.

### 2. windows-starting
- `vim -o file1 file2` open in split
- `-O` vertical split
- `'laststatus'= 1` statusline only if there is more than one window

### 3. opening-window
- `^W s` or `:sp` split in two
- `^W v`or `^W ^V`  or `:vs` split vertically
- `^W n` or  `^W ^N` or `:new` new empty window
- `:vne[w]` vertical
- `:sv[iew]` split and view
- `:sf[ind]` split and `:find` in `'path'`
- `^W ^^` or `^W ^` `:split` and `^^` the alternate file

### 4. window-move-cursor
### 5. window-moving
### 6. window-resize
### 7. buffer-list
### 8. list-repeat
### 9. window-tag
### 10. preview-window
### 11. buffer-hidden
### 12. special-buffers


## pymode.txt
- `let g:pymode_lint_cwindow = 0`: don't open quickfix window automatically

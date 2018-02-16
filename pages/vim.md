---
title: vim
---
## motion.txt

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

## pymode.txt
- `let g:pymode_lint_cwindow = 0`: don't open quickfix window automatically

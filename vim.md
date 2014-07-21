---
title: vim
layout: cheatsheet
---
## motion

### operator
- `c` change
- `d` delete
- `y` yank
- `<` `>` shift

### horizontal
- `h`, `j`, `k`, `l`: single steps
- `f`, `t`: find in line (till)
- `F`, `T`: backwards
- `;`, `,`: repeat (backwards)
- `gj`, `gk`: up/down display lines
- `w`, `e`, `b`, `ge`: forward/back start/end of word
- `W`, `E`, `B`, `gE`: same for WORD

## pattern
- `/`, `?`: search (backwards)


# insert
- `i`, `a`: insert, append
- `A`: append to end of line
- `o`, `O`: new line after/before

# pymode
- `let g:pymode_lint_cwindow = 0`: don't open quickfix window automatically

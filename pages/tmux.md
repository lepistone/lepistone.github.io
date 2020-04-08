---
title: tmux
---
## References
All official documentation is in `man tmux`. It it a bit terse but good.

For a longer essay, see the Brian Hogan's [tmux 2](https://pragprog.com/book/bhtmux2/tmux-2).

## Pairing
If someone is connecting with `ssh` to your machine, make them attach with `tmux attach -E`. This should disable propagating their environment variables to the tmux session, which is preferrable if you still want to use your local SSH agent.

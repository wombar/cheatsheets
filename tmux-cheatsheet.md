# Tmux Cheatsheet

## Session Commands

`tmux list-sessions` | `tmux ls` - List-sessions

`tmux attach -t 0` | `tmux a -t 0` - Attach to session id


## Window Commands
### Run *Command* -> `ctrl+b` before these commands

`d` - Detach from session

`c` - Create window

`n` - Next window

`p` - Previous window

`x` - Kill window

`,` - Rename

## Window Splitting
### Run *Command* -> `ctrl+b` before these commands

`%` (`Shift + 5`) - Vertical Split

`"` (`Shift + 2`) - Horizontal Split

`o` - Toggle between windows

`z` - Toogle Full Screen Current Pane

`[` (then q to quit scroll mode) - Activate scrolling on history

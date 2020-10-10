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

`!` - Convert pane into window

`Ctrl + b -> Ctrl + --> / <-- (right/left arrow)` - Move divider left/right   

`Ctrl + b -> Ctrl + (up/down arrow)` - Move divider up/down
## Window Management

### Run *Command* -> `ctrl+b -> :` before these commands

`swap-window -t 0` - Swap current window with position 0

`swap-window -s 3 -t 1` - Swap window 3 with window 1

`move-window -t 0` - Move current window to 0 (if 0 does not exist). Useful for creating windows out of sequence if that's what you want

`move-window -r` - Re-index all windows sequentially

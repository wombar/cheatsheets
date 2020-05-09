# VIM Cheatsheet

### File Operations

`:wq` | `:x` | `ZZ` - Save and close file  

`:q` - Close file, prompt for save if necessary

`:q!` | `ZQ` - Close file, abandon changes


### Copy / Paste Operations

`shift + d` - Cut line

`shift + y` - Copy line (Yank)

`shift + p` - Paste

### Visual

`:set number` - Show line numbers

`:set nonumber` - Hide line numbers

### Find

`*` - Find next occurence of word (on your cursor)

`#` - Find previous occurence of word (on your cursor)

`/lookforme` - Find word `lookforme` -> Then use next/previous commands above


### Mode switching

`i` - Enter insert mode

`:` - Enter command mode

`R` - Enter replace mode (like hitting insert on your keyboard)

`v` - Enter visual mode (highlighting)

`V` - Enter visual line mode (highlighting lines)

`esc` - Return to normal mode from insert or replace mode

`esc+esc` - Return to normal mode from command or visual mode


### Show Special Characters

If you have suspected hidden/special characters

`:set listchars=eol:$,tab:>-,trail:~,extends:>,precedes:<`

`:set list`
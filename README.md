# vim-commands

## Navigation and Editing in Normal Mode
| Command | Description |
|---------|-------------|
| `h` | Move the cursor left |
| `j` | Move the cursor down |
| `k` | Move the cursor up |
| `l` | Move the cursor right |
| `w` | Move the cursor to the beginning of the next word |
| `b` | Move the cursor to the beginning of the previous word |
| `0` | Move the cursor to the beginning of the line |
| `$` | Move the cursor to the end of the line |
| `gg` | Move the cursor to the beginning of the file |
| `G` | Move the cursor to the end of the file |
| `dd` | Delete the current line |
| `yy` | Yank (copy) the current line |
| `p` | Paste the contents of the clipboard after the cursor |
| `u` | Undo the last change |
| `Ctrl + r` | Redo the last change |
| `:w` | Write (save) the current file |
| `:q` | Quit Vim |
| `:wq` | Write (save) the current file and quit Vim |


## Navigation and Editing in Insert Mode
| Command | Description |
|---------|-------------|
| `Ctrl + h` | Delete the character to the left of the cursor |
| `Ctrl + w` | Delete the word to the left of the cursor |
| `Ctrl + u` | Delete all text to the left of the cursor |
| `Ctrl + a` | Move the cursor to the beginning of the line |
| `Ctrl + e` | Move the cursor to the end of the line |
| `Ctrl + f` | Move forward one character |
| `Ctrl + b` | Move backward one character |
| `Ctrl + n` | Autocomplete the current word |
| `Ctrl + p` | Move to the previous line in the command-line history |
| `Ctrl + r` | Insert the contents of a register |
| `Ctrl + t` | Indent the current line |
| `Ctrl + d` | Unindent the current line |
| `Ctrl + k` | Insert a digraph |
| `Ctrl + g` | Show information about the current file |
| `Ctrl + x, Ctrl + l` | Insert a whole line from the completion list |
| `Ctrl + x, Ctrl + n` | Enable keyword completion |
| `Ctrl + x, Ctrl + k` | Insert a digraph |
| `Ctrl + x, Ctrl + f` | Insert a file name |
| `Ctrl + x, Ctrl + o` | Insert an omni completion list |
| `Ctrl + x, Ctrl + u` | Insert a user-defined completion list |
| `Ctrl + x, Ctrl + v` | Insert a Vim command-line completion list |


## Vim Modes

| Mode | Description |
|------|-------------|
| Normal | The default mode for Vim, used for navigation and editing commands |
| Insert | Used for entering text into the document |
| Visual | Used for selecting and manipulating blocks of text |
| Command-Line | Used for entering commands that modify the editor or perform operations on the document |
| Ex | A special mode within Command-Line mode, used for advanced editing tasks and file operations |


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


## 1. To replace the contents of a file with copied system text using Vim, follow these steps:

1. Copy the text you want to replace the contents of the file with using a system command, such as pbcopy on macOS or xclip on Linux.

2. Open the file you want to replace the contents of in Vim by typing vim file.txt in the terminal, replacing "file.txt" with the actual name of the file.

3. Press gg to move the cursor to the beginning of the file.

4. Press dG to delete all lines in the file.

5. Press :set paste to enable paste mode, which ensures that the pasted text is inserted as-is, without any unintended formatting changes.

6. Press i to enter insert mode.

7. Right-click to paste the copied text into the file.

8. Press Esc to exit insert mode.

9. Press :set nopaste to disable paste mode.

10. Press :wq to save the changes to the file and exit Vim.

A one-liner that replaces the contents of a file with copied system text using Vim:
```
vim -c "normal ggVGd:set paste<CR>i<C-R>*<Esc>:set nopaste<CR>:wq" file.txt
```
Here's how this command works:

* vim: Invokes Vim.
* -c: Tells Vim to execute the following command.
* "normal ggVGd:set paste<CR>i: Deletes all lines in the file (ggVGd), sets paste mode (:set paste<CR>), and enters insert mode (i).
* ggVGd is a Vim command that deletes all lines in the file. Here's what each part of the command does:
  - gg: Moves the cursor to the first line of the file.
  - VG: Selects all lines in the file.
  - d: Deletes the selected lines.
* <C-R>*: Pastes the contents of the system clipboard into the file (using the * register).
* <Esc>:set nopaste<CR>:wq: Exits insert mode (<Esc>), disables paste mode (:set nopaste<CR>), saves changes to the file (:w), and exits Vim (:q).
* file.txt: Specifies the name of the file to edit.

Note that this command assumes that the text in the system clipboard is plain text and does not contain any special characters that need to be escaped in Vim. If you encounter any issues, you may need to modify the command or use the step-by-step approach instead.



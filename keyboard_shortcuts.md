## Linux Keyboard Shortcuts

| **Key** | **Function** |
| :--: | :-- |
| **Cursor Movement** |
| Ctrl+B | Move cursor backward one character position |
| Ctrl+F | Move cursor forward one character position |
| Alt+F | Move cursor one word forward in line |
| Alt+B | Move cursor one word backward in line |
| Ctrl+A | Move cursor to beginning of text in line |
| Ctrl+E | Move cursor to end of text in line |
| **Text Editing** |
| Ctrl+D | Erase character forward from cursor left to right |
| Ctrl+H | Erase character backward from cursor right to left |
| Alt+D | Erase the next word from cursor left to right |
| Ctrl+W | Erase backwards to first non-alphanumeric character or empty space |
| Ctrl+U | Erase a line of input from cursor right to left |
| Ctrl+K | Erase a line of input from cursor left to right |
| Alt+R | Revert any changes to a previously executed command that's being edited |
| Alt+. | Fetch and paste the last word at end of a command from previous commands |
| Ctrl+T | Reverse the position of the character the cursor is on with the previous character |
| Alt+T | Reverse the position of the word the cursor is in with the previous word |
| Alt+U | Capitalize every character from cursor left to right to the end of one word |
| Alt+L | Uncapitalize every character from cursor left to right to the end of one word |
| Ctrl+Y | Paste (yank) text cut by Ctrl+U, Ctrl+K, or Ctrl+W |
| Ctrl+_ | Undo last change |
| **Command History** |
| Ctrl+P | Fetch previous command from history list |
| Ctrl+N | Fetch next command from history list |
| Ctrl+R | Reverse search commands from history list |
| **Process Control** |
| Ctrl+C | Break/Terminate a foreground job |
| Ctrl+Z | Suspend a foreground job |
| Ctrl+S | Suspend output to screen |
| Ctrl+Q | Resume output to screen |
| **Terminal Control** |
| Ctrl+L | Clear screen contents (command-line needs to be empty) |
| Ctrl+D | Log out from a shell (similar to exit) or send EOF |
| Ctrl+O | Accept the current line for execution and fetch the next command |
| Ctrl+X (twice) | Toggle cursor between current position and beginning of the line |
| **Text Editing (Terminal)** |
| Ctrl+Shift+C | Copy |
| Ctrl+Shift+V | Paste |
| Shift+Insert | Paste (alternative) |

<i>Some of these shortcuts may vary depending on your terminal and system.</i>

## Nano (text editor)

| **Key**       | **Function** |
| :--: | :-- |
| **Movement**  | |
| `Ctrl+Y`      | Scroll page **up** |
| `Ctrl+V`      | Scroll page **down** |
| `Alt+\`       | Go to the beginning of the file |
| `Alt+/`       | Go to the end of the file |
| **Editing**   | |
| `Ctrl+H`      | Delete the character before the cursor |
| `Ctrl+D`      | Delete the character under the cursor |
| `Alt+Backspace`| Delete the word to the left |
| `Ctrl+Del`    | Delete the word to the right |
| `Alt+Del`     | Delete the current line |
| `Alt+^`       | Copy selected text to the cut buffer |
| `Ctrl+K`      | Cut selected text to the cut buffer |
| `Ctrl+U`      | Paste text from the cut buffer (clipboard) |
| `Alt+A`       | Start text selection (can be used with Ctrl+K to cut specific text) |
| `Ctrl+J`      | Justify (wrap) the current paragraph |
| **Undo and Redo** | |
| `Alt+U`       | Undo the last action |
| `Alt+E`       | Redo the last undone action |
| **Search and Replace** | |
| `Ctrl+Q`      | Start backward search (press again to repeat) |
| `Ctrl+W`      | Start forward search (press Alt+W to search for the same term again) |
| `Ctrl+\`      | Replace a string or regular expression |
| **File Operations** | |
| `Ctrl+R`      | Insert a file at the current cursor position |
| `Ctrl+O`      | Write changes to the file ("Save as") |
| `Ctrl+S`      | Save the current file |
| `Ctrl+X`      | Exit Nano (prompts to save changes if needed) |
| **Miscellaneous** | |
| `Alt+3`       | Comment/uncomment the line/region |
| `Ctrl+G`      | Show help for all available commands |
| `Ctrl+T`      | Open the spell checker |

## Vim (text editor)

| **Key** | **Function** |
| :--: | :-- |
| **Movement** | |
| `h` | Move left |
| `j` | Move down |
| `k` | Move up |
| `l` | Move right |
| `w` | Move forward to the beginning of the next word |
| `b` | Move backward to the beginning of the previous word |
| `e` | Move to the end of the current word |
| `0` (zero) | Move to the beginning of the line |
| `$` | Move to the end of the line |
| `gg` | Go to the first line of the document |
| `G` | Go to the last line of the document |
| `:{number}` | Go to a specific line number |
| `Ctrl+f` | Page down |
| `Ctrl+b` | Page up |
| `%` | Move to matching parenthesis or bracket |
| `^` | Move to the first non-blank character of the line |
| `H` | Move to the top of the screen |
| `M` | Move to the middle of the screen |
| `L` | Move to the bottom of the screen |
| `*` | Search forward for the word under the cursor |
| `#` | Search backward for the word under the cursor |
| **Editing** | |
| `i` | Insert before the cursor |
| `I` | Insert at the beginning of the line |
| `a` | Append after the cursor |
| `A` | Append at the end of the line |
| `o` | Open a new line below the current line |
| `O` | Open a new line above the current line |
| `r` | Replace a single character |
| `R` | Enter replace mode |
| `x` | Delete the character under the cursor |
| `X` | Delete the character before the cursor |
| `dd` | Delete the current line |
| `D` | Delete from the cursor to the end of the line |
| `yy` | Yank (copy) the current line |
| `p` | Paste after the cursor |
| `P` | Paste before the cursor |
| `u` | Undo the last action |
| `Ctrl+r` | Redo the last undone action |
| **Visual Mode** | |
| `v` | Enter visual mode (character selection) |
| `V` | Enter visual line mode |
| `Ctrl+v` | Enter visual block mode |
| **Text Objects** | |
| `ciw` | Change the inner word |
| `diw` | Delete the inner word |
| `yaw` | Yank (copy) the entire word |
| `ci"` | Change text inside double quotes |
| `di(` | Delete text inside parentheses |
| **Search and Replace** | |
| `/pattern` | Search forward for 'pattern' |
| `?pattern` | Search backward for 'pattern' |
| `n` | Repeat the search in the same direction |
| `N` | Repeat the search in the opposite direction |
| `:%s/old/new/g` | Replace all occurrences of 'old' with 'new' in the file |
| `:%s/old/new/gc` | Replace all occurrences of 'old' with 'new' with confirmation |
| **File Operations** | |
| `:w` | Write (save) the file |
| `:w filename` | Write to a specific filename |
| `:q` | Quit Vim |
| `:q!` | Quit without saving changes |
| `:wq` | Write and quit |
| `:x` | Write and quit (same as `wq`) |
| **Multiple Files** | |
| `:e filename` | Edit a file in a new buffer |
| `:bnext` or `:bn` | Go to the next buffer |
| `:bprev` or `:bp` | Go to the previous buffer |
| `:bd` | Delete a buffer (close the file) |
| `:sp filename` | Open a file in a new buffer and split the window horizontally |
| `:vsp filename` | Open a file in a new buffer and split the window vertically |
| `Ctrl+ws` | Split the window horizontally |
| `Ctrl+wv` | Split the window vertically |
| `Ctrl+ww` | Switch between windows |
| `Ctrl+wq` | Quit the current window |
| **Macros** | |
| `qa` | Record macro in register 'a' |
| `q` | Stop recording macro |
| `@a` | Run macro from register 'a' |
| `@@` | Rerun the last executed macro |
| **Marking and Jumping** | |
| `m{a-z}` | Set a mark with a letter (a-z) in the current position |
| `'a` | Jump to the line with mark 'a' |
| `` `a `` | Jump to the exact position with mark 'a' |
| `:marks` | List all the marks |
| `Ctrl+o` | Jump to the previous location |
| `Ctrl+i` | Jump to the next location |
| **Tabs** | |
| `:tabnew` | Open a new tab |
| `gt` or `:tabnext` | Go to the next tab |
| `gT` or `:tabprev` | Go to the previous tab |
| `:tabclose` | Close the current tab |
| `:tabs` | List all open tabs |
| **Miscellaneous** | |
| `.` | Repeat the last command |
| `ZZ` | Write the current file (if modified) and quit |
| `ZQ` | Quit without checking for changes |
| `Ctrl+g` | Show the file name and status |
| `g Ctrl+g` | Show the cursor position (line, column, and character) |

[⬆ ʀᴇᴛᴜʀɴ ᴛᴏ ᴛᴏᴩ](#linux-keyboard-shortcuts)

# Vim Fundementals

## Terminology

### Buffer

A buffer is a file loaded into memory for editing. It is not the file itself, but a representation of the file in memory. A buffer can be associated with a file, but it is not the file itself.

### Window

A window is a viewport onto a buffer. A buffer can be displayed in multiple windows, and a window can display multiple buffers. A window can be split into multiple windows, each displaying a different buffer. Windows can be closed but the underlying buffers can remain in memory.

### Tab

A tab is a collection of windows. Each window can display a different buffer. Tabs can be used to organize windows into different workspaces.

### Split

A split is a window that is created by splitting an existing window. Each split can display a different buffer. A window can be split horizontally or vertically. A window can be split multiple times, creating a complex layout of windows. They can be resized and moved around.

### Other Terms

- **Cursor**: The position in the buffer where text will be inserted.
- **Line Number**: The line number of the cursor.
- **Sign Column**: The column to the left of the buffer where signs can be displayed.
- **Status Line**: The line at the bottom of the window that displays information about the buffer.
- **Tab Line**: The line at the top of the window that displays information about the tabs.
- **Command Line**: The line at the bottom of the window where commands can be entered.
- **Mode**: Vim has multiple modes, such as normal mode, insert mode, visual mode, and command-line mode.
- **Register**: A register is a place to store text. Registers can be used to copy and paste text between buffers.
- **Mark**: A mark is a position in a buffer. Marks can be used to jump to a specific position in a buffer.
- And many more...

## Motion

A motion is a command that moves the cursor.

## Modes

Vim has multiple modes, such as normal mode, insert mode, visual mode, and command-line mode.

### Normal Mode

Normal mode is the default mode. It is the mode where commands are entered. In normal mode, the keyboard is used to enter commands to move the cursor, delete text, copy text, paste text, and more.

## Basic Navigation

- `h`: left
- `j`: down
- `k`: up
- `l`: right
- `w`: next word
- `b`: previous word
- `e`: end of word
- `0`: beginning of line
- `$`: end of line
- `gg`: beginning of file
- `G`: end of file
- `H`: top of window
- `M`: middle of window
- `L`: bottom of window

## Basic Editing

- `i`: insert mode
- `a`: append mode
- `o`: open line below
- `O`: open line above
- `x`: delete character
- `dd`: delete line
- `yy`: yank line
- `p`: paste line
- `u`: undo
- `Ctrl-r`: redo
- `.`: repeat last command
- `dw`: delete word

## Customization

- `set scrolloff=8` - Set the number of lines to keep above and below the cursor when scrolling.
- `set number` - Show line numbers.
- `set relativenumber` - Show relative line numbers.
- `set rnu` - Short for `relativenumber`.


## Nvim

- `echo stdpath('config')` - Show the location of the configuration directory.

## Some things

- `ctrl-shift-v` - Paste from clipboard in insert mode.


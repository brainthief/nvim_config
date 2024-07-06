# Install nvim

```
sudo apt install snapd
sudo snap install nvim --classic
```

## Instal c compiler

```
sudo apt install gcc
```

## Install nvchad config

https://nvchad.com/docs/quickstart/install
```
git clone https://github.com/brainthief/nvim_config/ ~/.config/nvim && nvim
```

Run ```:MasonInstallAll``` command after lazy.nvim finishes downloading plugins.
Run ```:Lazy sync``` command 

## After install mising packages
```
sudo npm install -g eslint_d
sudo npm install -g typescript-language-server
```

# Neovim keybinds

 (from : https://gist.github.com/kashifulhaque/d84e407b239782d7f381cc921c31c2fe)

- Capital letters do the opposite of small letters in command (Press shift to trigger capital letters)
- `_` (underscore) to move the cursor at the beginning of line (doesn't switch to insert mode)
  - `0` (zero) moves the cursor to the zeroth position of the line (doesn't switch to insert mode)
- `$` (dollar) to move the cursor at the end of line (doesn't switch to insert mode)
- `d$` will delete from wherever your cursor is till the end of the line
- `f<character>` to move cursor to the first occurrence of `<character>`
  - `f(` to move cursor to first occurence of `(`
- `t<character>` to move cursor to upto but not on the first occurrence of `<character>`
  - `t(` to move cursor to first occurence of `(`
- To repeat it, use `,` (comma, goes backward) or `;` (semicolon, goes forward)
  - `fe` and then keep pressing `;` to walk through each `e`
- To indent lines, select them using the visual line mode `Shift + v` and then use `>` to indent them right and `<` to indent them left

# [NvChad](https://nvchad.com) keybinds
- [based on this video](https://youtu.be/Mtgo-nP_r8Y)
- `space + c + h` to open keybinds cheatsheet (same command to close the window)
- `space` is considered as the ***leader*** key (commands often start with this key)
- Press the leader key `space` and wait for a second, a window should appear suggesting potential commands.

## **Themes** 🖌️
`space + t + h`

## **Syntax Highlight** 🖊️
- [neovim](https://github.com/neovim/neovim) comes with [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
  - [To install a language](https://github.com/neovim/neovim) `:TSInstall <language_to_install>`
  - [A list of suupported languages](https://github.com/nvim-treesitter/nvim-treesitter#supported-languages)
  - To check which languages are installed `:TSInstallInfo`

## **File tree** 🌳
- `ctrl + n`
- Arrow keys to move cursor to a file and `return (enter)` to open a file
- `m` to mark a file
- `a` to create a new file and type the new file name
- `c` to copy a file
- `p` to paste the file
- `r` to rename a file
- `ctrl + w + h/l` or `larrow/rarrow` to switch between file tree and editor

## **Line numbers** 🔢
- `space + n` to toggle line numbers on/off
- `space + r + n` to toggle relative line numbers on/off
  - Once inside relative line number mode, can also press `space + n` to show current line as `0` (adjust as per your liking)

## **File navigation (Search)** 🕸️
- `space + f + f` to open file search menu (across the entire project)
- `space + f + b` to open file search menu (across the currently opened files)

## **Window navigation** 🕹️
- `:vsp` for vertical split
- `:sp` for horizontal split
- `ctrl + h/j/k/l` to toggle windows

## **Cycle through open tabs (buffers)** 📑
- `tab` to cycle left to right
- `shift + tab` to cycle right to left
- `space + x` to close current tab (buffer)

## **Open terminal** 🤖
- `space + v` to open terminal (vertically)
  - `alt + v` to toggle the terminal on/off
- `space + h` to open terminal (horizontally)
  - `alt + h` to toggle the terminal on/off

## **Other useful stuff** ✍🏻
- [Vim as your editor by Primeagen](https://youtu.be/X6AR2RMB5tE)
- [Cheatsheet](https://www.reddit.com/r/neovim/comments/12qku4w/nvchad_cheatsheet)

# VIM key binds

- `Normal Mode`: Default state for efficient movement, deletion, searching, and more.
- `Insert Mode`: Allows you to type text directly into your file.
- `Visual Mode`: Enables text selection for manipulation.

## Normal mode

```
h  --> move left
j  --> move down
k  --> move up
l  --> move right
gg  --> Move to the first line of the page
G   --> Move to the last line of the page
:number   --> Go to the line number
$  --> Go to the end of the line
0  --> Go to the start of the line
b  --> Go to the previous word
w  --> Go to the next word

editing in Normal mode:
x   --> Delete the character under the cursor
dd  --> Delete the entire line
yy  --> Copy (yank) the entire line
p   --> Paste the previously deleted or copied text after the cursor

u          --> Undo the last action
Ctrl + r   --> Redo the undone action

/              --> Start searching forward
?              --> Start searching backward
:s/old/new/g   --> Replace all occurrences of "old" with "new" in the entire file


```

## Insert mode

```
Esc   --> Return to Normal Mode
i     --> Start inserting text before the cursor
a     --> Start inserting text after the cursor
o     --> Open a new line below the current line and start inserting text
```


## Visual mode

```
v          --> Start character-wise visual mode
V          --> Start line-wise visual mode
Ctrl + v   --> Start block-wise visual mode
d          --> Delete the selected text
y          --> Copy (yank) the selected text
p          --> Paste the copied text after the cursor
```

## More navigation

```
Ctrl + u   --> Move half a screen up
Ctrl + d   --> Move half a screen down
Ctrl + b   --> Move one full screen up
Ctrl + f   --> Move one full screen down

(  --> Jump to the beginning of the previous sentence
)  --> Jump to the beginning of the next sentence
{  --> Jump to the beginning of the previous paragraph
}  --> Jump to the beginning of the next paragraph

]]  --> Move to the beginning of the next function
[[  --> Move to the beginning of the previous function
>>  --> Indent the current line to the right
<<  --> Indent the current line to the left
zf{motion}  --> Create a fold (replace {motion} with a movement command)
zo          --> Open a fold
zc          --> Close a fold
zr          --> Reduce folding level throughout the file
zm          --> Increase folding level throughout the file

gcc  --> Comment/uncomment the current line
gc{motion}  --> Comment/uncomment the lines covered by {motion}
%  --> Move to the matching parenthesis, bracket, or brace
```

From: https://www.freecodecamp.org/news/vim-key-bindings-reference/

# :g Global commands

    |:g/^$/d | Deletes all empty lines|
    |::g/^$/,/./-j | Reduce multiple blank lines to a single blank |
    |:g/pattern/y A | Copy lines with *pattern* to register A |
    |:g/^pattern/s/$/mytext | Add text to end of line that matches pattern |

# Text objects

* w - Words
* s - Sentences
* p - Paragraphs
* t - Tags (i.e. <a>)
* ' - Single quote
* " - Double quote
* { - Braces
* [ - Brackets
* ( - Parenthisis

## Inside and Around

Use ** ci" ** to change inside quotes

Use ** ca" ** to change quotes and text inside


# Motion commands

|Key | Movement | Notes |
|----|----------|------|
|w   | next word | W after whitepace |
|b   | start of previous word | B after whitespace |
|e   | end of next word | E after whitspace|
|ge  | end of previous word| |
|0   | start of current line| |
|^   | first word of current line| |
|$   | end of current line||
|<cr>| start of next line | |
|-   | start of previous line | 
|{   | start of current paragraph |  |
|}   | end of current paragraph | empty lines define paragraph |
|gg  | top of buffer | |
|G   | end of buffer | |
|ngg | line n of buffer | |
|%   | move to matching bracket| {} () [] |
| ^] | jump forward  |  |
| ^[ | jump backward |  |

# Search/Replace

* :%s/old/new/g search old, replace with new
* :%s/old//gn search and count
* :s<cr> repeat last search
* & = :s<cr>

# Windows

* <Ctrl-w>w - cycle between windows
* <ctrl-w>h j k l - movement between windows
* <ctrl-w><ctrl-w> - cycle between windows
* <ctrl-w>t move window to tab
* <ctrl-w>gf edit file under cursor in new tab
* <ctrl-w>= - equalize width * height
* <ctrl-w>_ maximize height
* <ctrl-w>| maximize width 
* :close <ctrl-w>c - close window
* :only - close all other windows

# Mark

* m[a-z] local mark
* m[A-Z] mark in another file
* <,> visual mode marks

# Registers

* "" - unnamed register (used for x, s, d, c, y)
* "0 - yank register
* "[a-z] 26 named registers (overwrite)
* "[A-Z] appends to named register
* "+ system clipboard
* "% filename
* ". last inserted text
* ": last ex command
* "/ last search pattern
* :delete b - cut into register b
* :put c - paste from register c
* can be used as macros using @a

# Indent

## Normal mode

* >> Indent current line
* 5>> Indent next 5 lines
* == Autoindent current line
* 5== Autoindent next 5 lines
* gg=G Autoindent entire file
* =i} Autoindent everything inside {}

## Insert mode

* ^t Indent current line
* ^d Delete indent on current line
* ^o Return to normal mode for 1 command

## Visual mode

* > Indent visual
* < Remove indent
* = Autoindent selected

# Folding

* zA - Toggle all folds recursively
* zC - Close all folds recursively
* za - toggle one fold
* zc - close one fold
* zO - open all folds at cursor
* zo - open one fold at cursor
* zR - open ALL folds, make foldlevel 0
* zr - decrease foldlevel by 1
* zm - increase foldlevel by 1
* [z - move to start of open fold
* ]z - move to end of opem fold
* zk - move to previous fold
* zj - move to next fold
* zi - toggle folding
* zMzv - Close all folds, open current

# Abbreviations

* :iabbrev shds Shared Host Detection Settings

# Mappings

* :nnoremap - Normal mode remap
* :inoremap - Insert mode remap
* :vnoremap - Visual mode remap
* :noremap  - All modes remap
* :nnoremap <leader>ev :vsplit $MYVIMRC<cr>

# Plugins

## vinegar.vim

* git://github.com/tpope/vim-vinegar.git
* - will go up a directory
* I will display header like netrw
* Press . to pre-populate filename/directory at end of : (i.e. grep)
* Press ! to pre-populate filename (!chmod +x = !chmod +x path/to/file)
* cg = :cd  cl = :lcd
* ~ go home

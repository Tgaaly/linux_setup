# vimrc (~/.vimrc)

  1 set expandtab           " enter spaces when tab is pressed
  2 set textwidth=100       " break lines when line length increases
  3 set tabstop=4           " use 4 spaces to represent tab
  4 set softtabstop=4
  5 set shiftwidth=4        " number of spaces to use for auto indent
  6 set autoindent          " copy indent from current line when starting a new line
  7
  8 " make backspaces more powerfull
  9 set backspace=indent,eol,start
 10
 11 set ruler               " show line and column number
 12 syntax on               " syntax highlighting
 13 set showcmd             " show (partial) command in status line
 14
 15 syntax on
 16 set showmatch
 17 set autoindent
 18 set smartindent

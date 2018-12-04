# vimrc (~/.vimrc)

```
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
```

# for git prompt showing branch status, add the followign to your bashrc

```
function parse_git_dirty {
  [[ $(git status --porcelain 2> /dev/null | tail -n1) != "" ]] && echo "*"
}

function parse_git_branch {
  git branch --no-color 2> /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/[\1]/"
}

export PS1="\[\033[36m\]\u@\h\[\033[32m\]:\w\[\033[33m\]\$(parse_git_branch)\[\033[31m\]\$(parse_git_dirty)\[\033[33m\]\[\033[00m\] $ "
```

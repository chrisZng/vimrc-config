```
color koehler

" Ensure we're using the latest Vim features
set nocompatible

" Use a better paste mode
set paste

" Set the encoding used for reading and writing files
set encoding=utf-8

" Set the terminal encoding
set termencoding=utf-8
set fileencodings=utf-8
set fileencoding=utf-8

" Enable syntax highlighting
syntax on

" Enable line numbering
set number

" Show the status line at the bottom of the window
set ruler

" Highlight search results
set hlsearch

" Use 4 spaces instead of tabs
set tabstop=4
set softtabstop=4
set shiftwidth=4
set expandtab

" Automatically indent lines according to the previous line
set autoindent

" Show commands as they are entered
set showcmd

" Do not create backup files
set nobackup
set nowritebackup

" Ignore case when searching
set ignorecase

" Use incremental search
set incsearch

" Enable mouse support in the terminal
set mouse=a

" Enable visual bell instead of audible bell
set visualbell

" Disable swap files
set noswapfile

" Enable color column for 80-character line length guideline
set colorcolumn=80

" Improve the way searching works
set smartcase
set wrapscan

" Highlight matching parentheses
set showmatch

" Improved command line completion
set wildmenu
set wildmode=longest:list,full

" Enable undo branches
set undofile
set undodir=~/.vim/undo

" Enable session management
set sessionoptions=blank,buffers,curdir,folds,help,options,tabpages,winsize

" Enable syntax highlighting for all file types
filetype plugin on

" Enable indentation for all file types
filetype indent on

function! PhpTemplate()
    call setline(1, "<?php")
    call setline(2, "")
    call setline(3, "")
    call cursor(3, 0)
endfunction

au BufNewFile *.php call PhpTemplate()

function! BinBashShTemplate()
    call setline(1, "#!/bin/bash")
    call setline(2, "")
    call setline(3, "")
    call cursor(3, 0)
endfunction

au BufNewFile *.sh call BinBashShTemplate()
```

# Vim
Vim personalitzat

1. Crear touch .vimrc

2. Instalar Plugins:
https://github.com/junegunn/vim-plug

3. Abrir .vimrc y escribir el siguiente texto:

syntax on
set nu
set mouse=a
set ruler
" Do not save backup files.
set nobackup

" Do not let cursor scroll below or above N number of lines when scrolling.
set scrolloff=10

" Do not wrap lines. Allow long lines to extend as far as the line goes.
set nowrap

" While searching though a file incrementally highlight matching characters as you type.
set incsearch

" Ignore capital letters during search.
set ignorecase

" Override the ignorecase option if searching for capital letters.
" This will allow you to search specifically for capital letters.
set smartcase

" Show partial command you type in the last line of the screen.
set showcmd

" Show the mode you are on the last line.
set showmode

" Show matching words during a search.
set showmatch

" Use highlighting when doing a search.
set hlsearch

" Enable auto completion menu after pressing TAB.
set wildmenu

" Make wildmenu behave like similar to Bash completion.
set wildmode=list:longest

" There are certain files that we would never want to edit with Vim.
" Wildmenu will ignore files with these extensions.
set wildignore=*.docx,*.jpg,*.png,*.gif,*.pdf,*.pyc,*.exe,*.flv,*.img,*.xlsx

call plug#begin('~/.vim/plugged')

Plug 'shinchu/lightline-gruvbox.vim'
Plug 'preservim/nerdtree'

call plug#end()

" Tanca automaticament els simbols.
inoremap " ""<left>
inoremap ' ''<left>
inoremap ( ()<left>
inoremap ) ();<left><left>
inoremap [ []<left>
inoremap { {}<left>

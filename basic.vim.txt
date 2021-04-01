syntax on

''makes vim more like an IDE''
set noerrorbells
set tabstop=4 softtabstop=4
set shiftwidth=4
set expandtab
set smartindent
set nu
set nowrap
set smartcase
set noswapfile
set nobackup
set undodir=~/.vim/undodir
set undofile
set incsearch

''customizing colors''
set colorcolumn=80
set background=dark
colorscheme gruvbox
highlight ColorColumn ctermbg=0 guibg=lightgrey

''general plugins''
call plug#begin('~/.vim/plugged')

Plug 'morhetz/gruvbox'
Plug 'jremmen/vim-ripgrep'
Plug 'tpope/vim-fugitive'
Plug 'leafgarland/typescript-vim'
Plug 'vim-utils/vim-man'
Plug 'lyuts/vim-rtags'
Plug 'mbbill/undotree'

call plug#end()

''ignore case when searching''
if executable('rg')
    let g:rg_derive_root='true'
endif

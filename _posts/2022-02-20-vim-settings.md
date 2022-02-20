---
title: "Настраиваем neo vim в шindows"
layout: def
categories: vim
impMath: false
excerpt: Checkout
---

# {{ page.title }}

Не знаю почему ловлю fun, когда к этому переодически возвращаюсь (при том, что есть github1s.com)

1. качаешь архив https://github.com/neovim/neovim/releases
2. разворачиваешь куда-нибудь
3. добавляешь в Path путь к `Neovim/bin` папке
4. копируешь этот файл https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim в `Neovim/share/nvim/runtime/autoload`
5. `Win + R`
6. `nvim-qt` + `Enter`
7. `:e $VIM/sysinit.vim`
8. ```
   set number
   set tabstop=4
   set expandtab
   set softtabstop=4
   set shiftwidth=4
   syntax on
   set encoding=utf-8
   set mouse=a
   source $VIMRUNTIME/mswin.vim

   call plug#begin('$VIM/plugged')
   Plug 'OmniSharp/omnisharp-vim'
   Plug 'neoclide/coc.nvim', {'branch': 'release'}
   Plug 'dense-analysis/ale'
   Plug 'junegunn/fzf.vim'
   Plug 'preservim/nerdtree', {'on': 'NERDTreeToggle'}
   Plug 'Xuyuanp/nerdtree-git-plugin'
   call plug#end()

   " tab autocompletion
   function! s:check_back_space() abort
     let col = col('.') - 1
     return !col || getline('.')[col - 1]  =~ '\s'
   endfunction

   inoremap <silent><expr> <Tab>
         \ pumvisible() ? "\<C-n>" :
         \ <SID>check_back_space() ? "\<Tab>" :
         \ coc#refresh()

   " Map Ctrl-Backspace to delete the previous word in insert mode.
   imap <C-BS> <C-W>

   set title

   augroup dirchange
       autocmd!
       autocmd DirChanged * let &titlestring=v:event['cwd']
   augroup END

   let g:ale_linters = { 'cs' : ['OmniSharp'] }
   let b:ale_linters = ['cs', 'flow-language-server']
   let mapleader=";"
   autocmd FileType cs nnoremap <silent> <C-w> :OmniSharpGotoDefinition<CR>
   autocmd FileType cs nnoremap <silent> <C-r> :OmniSharpRename<CR>
   inoremap { {<CR>}<Esc>ko
   nnoremap <silent> <Space> :NERDTreeToggle<CR>
   "inoremap ( ()<Esc>ha
   "inoremap [ []<Esc>ha
   nnoremap <silent> <C-p> :Files!<CR>
   set hlsearch
   nnoremap <silent> <C-L> :nohlsearch<CR><C-L>
   ```
8. `:w`
9. `:source $VIM/sysinit.vim`
10. `PlugInstall`
11. `:q`
12. ???
13. Profit 😎

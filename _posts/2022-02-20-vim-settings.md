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
   set tabstop=2
   set softtabstop=2
   set shiftwidth=2
   syntax on
   set encoding=utf-8
   set mouse=a
   source $VIMRUNTIME/mswin.vim
   call plug#begin('$VIM/plugged')
   Plug 'OmniSharp/omnisharp-vim'
   Plug 'drzel/vim-repo-edit'
   call plug#end()
   ```
8. `:w`
9. `:source $VIM/sysinit.vim`
10. `PlugInstall`
11. `:q`
12. ???
13. Profit 😎

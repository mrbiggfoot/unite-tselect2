# unite-tselect2

## Introduction

This is a fork of [unite-tselect](https://github.com/eiiches/unite-tselect).

`unite-tselect` is a [unite.vim](https://github.com/Shougo/unite.vim) source plugin
for selecting tags, which provides a similar functionality as :tselect command.


## Usage

To search tags for `<keyword>`, execute

    :Unite tselect:<keyword>

If you want to remap `g<C-]>` and `g]`, copy the following lines into your vimrc.

    nnoremap g<C-]> :<C-u>Unite -immediately tselect:<C-r>=expand('<cword>')<CR><CR>
    nnoremap g] :<C-u>Unite tselect:<C-r>=expand('<cword>')<CR><CR>

To make a command that behaves like `:tselect`:

    command! -nargs=* Tselect Unite tselect:<args>

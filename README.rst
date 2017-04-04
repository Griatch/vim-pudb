vim-pudb
========

Simple plugin allowing you to manage pudb breakpoint directly into vim. This
fork incorporates some fixes that were lingering in PRs on other
forks.

This plugin need vim to be compiled with +python. NeoVim works well too.

Installation
============

The recommended way of installing is to use `vim-pathogen`_. With
Pathogen installed, just clone this repo to ``~/.vim/bundle``.


How to use
==========

To add/remove a breakpoint, you just need to call the command ``:TogglePudbBreakPoint``. Make
sure no other vim plugin is deactivating the SignColumn. You can clear
all breakpoints with ``:ClearPudbBreakPoints``.

For easy access, you can for example bind the set command to the F8 key.


    ``nnoremap <F8> :TogglePudbBreakPoint<CR>``

    ``inoremap <F8> <ESC>:TogglePudbBreakPoint<CR>a``

    ``nmap <S-F8> <ESC>:!pudb %<CR>a``

.. _vim-pathogen: https://github.com/tpope/vim-pathogen#readme

Known problems
=============
Currently, the list of breakpoints is not reloaded automatically. 

There is also room for speed optimisations.

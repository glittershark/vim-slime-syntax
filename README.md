vim-slime
=========

[Slime][slime] syntax highlighting for vim, based off [vim-slim][vim-slim].

[slime]: https://github.com/slime-lang/slime
[vim-slim]: https://github.com/slim-template/vim-slim

Install with pathogen
---------------------

If you are already using pathogen, you can skip to step 3.

1. Install pathogen (if you haven't already)

        mkdir -p ~/.vim/autoload ~/.vim/bundle; \
        curl -so ~/.vim/autoload/pathogen.vim \
        https://raw.github.com/tpope/vim-pathogen/master/autoload/pathogen.vim

2. Edit `~/.vimrc` to run pathogen as the first line of the file (if you haven't already)

    ```vim
    call pathogen#infect()

    syntax enable
    filetype plugin indent on
    ```

3. Install slime-vim-syntax

        pushd ~/.vim/bundle; \
        git clone git@github.com:slime-lang/vim-slime-syntax.git;\
        popd


Install with vbundle
--------------------

1. [Install Vundle] into `~/.vim/bundle/`.

[Install Vundle]: https://github.com/gmarik/vundle#quick-start

        mkdir -p ~/.vim/bundle; pushd ~/.vim/bundle; \
        git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
        popd

2. Configure your vimrc for Vundle. Here's a bare-minimum vimrc that enables vim-slime-syntax :


    ```vim
    set rtp+=~/.vim/bundle/vundle/
    call vundle#rc()

    Bundle 'slime-lang/vim-slime-syntax.git'

    syntax enable
    filetype plugin indent on
    ```

If you're adding Vundle to a built-up vimrc, just make sure all these calls
   are in there and that they occur in this order.

3. Open vim and run `:BundleInstall`.

To update, open vim and run `:BundleInstall!` (notice the bang!)

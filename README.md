Creating it so that I don't have to configure it again &amp; again (like the 3 times I already did).

## Installing neovim

```
brew install neovim
```

## Configuring neovim

Configurations for neovim go in the `init.vim` file. We need to create it. 
This requires creating some directories.

```
mkdir -p ~/.config/nvim
```


```
nvim ~/.config/nvim/init.vim
```

## Installing vim-plug

We need to create some directories before installing vim-plug.

This is where the `plug.vim` goes.

```
mkdir -p ~/.config/nvim/autoload
```

This where all our plugins go.

```
mkdir -p ~/.config/nvim/plugged
```

### Downloading vim-plug

```
sh -c 'curl -fLo ~/.config/nvim/autoload/plug.vim --create-dirs  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

## Installing a new plugin


To install a plugin, we need to add a few lines to  `init.vim`. 

Add the plugin name between `plug#begin` & `plug#end`  in the same format as below.

For e.g. to add `morhetz/gruvbox`, add `Plug 'morhetz/gruvbox'`.


```
call plug#begin("~/.config/nvim/plugged")

Plug 'morhetz/gruvbox'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'


Plug 'preservim/nerdtree'
call plug#end()


```


After making changes to `init.vim`, save the changes (`:w`), and install the plugins `:PlugInstall`

Final step -  source (`:source %`) the file.

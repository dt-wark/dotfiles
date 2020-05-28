# warkentin's dotfiles

[TODO!:pic]

## First steps

We need to clone this repository to the temporary directory /tmp/

```
git clone https://github.com/dt-wark/dotfiles.git /tmp/ && cd /tmp/dotfiles
```

## Vim
- **Theme**: [**`Oceanic Next`**](https://github.com/mhartington/oceanic-next)
- **Plugin Manager**: [**`Vundle`**](https://github.com/VundleVim/Vundle.vim)
- **Installed plug-ins**: [**`nerdtree`**](https://github.com/preservim/nerdtree)

![vim screenshot](https://res.cloudinary.com/wark/image/upload/v1590686044/vim.png)

- **`Relative numbers are enabled`**
- **`Disabled automatic commenting on new line`**
- **`Backups and swap files are disabled`**
- **`Splits are opened at the bottom and right and the navigation keys are remapped`**
- **`The new tab is aliased to Ctrl+t`**
- **`Global replace is aliased to S`**
- **`System clipboard by default`**
- **`Spellchecker is aliased to F5`**
- **`UTF-8 by default`**

In general, my `.vimrc` is configured to work with Python: syntax is highlighted, indents are set to 4 spaces, smart indentation after keywords is enabled.

### Let's install Vundle, the color scheme and our configuration files

##### Step by step

```
mkdir ~/.vim
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
mv vim/vimrc ~/.vimrc
mv -v vim/colors/ vim/spell/ ~/.vim/
vim +PluginInstall +qall
```

##### Or one line

```
mkdir ~/.vim && git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim && mv vim/vimrc ~/.vimrc && mv -v vim/colors/ vim/spell/ ~/.vim/ && vim +PluginInstall +qall
```

And that's it!

